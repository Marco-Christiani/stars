---
repo: gwenzek/llvm_inline_annotations
url: 'https://github.com/gwenzek/llvm_inline_annotations'
homepage: null
starredAt: '2026-10-30T20:56:04Z'
createdAt: '2026-10-26T10:42:08Z'
updatedAt: '2026-10-30T20:56:05Z'
language: Zig
license: NA
branch: main
stars: 2
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2026-11-01T01:15:52.663Z'
description: annotate your zig code based on LLVM (missed) optimization
tags: []
---

# LLVM inline annotations

Analyze the optimized LLVM IR produced by LLVM,
and annotate your code with annotations.

Following annotations are emitted:
- *memcpy*: memcpy emitted by Zig, but not removed by LLVM optimization passes
- *memset*: memset emitted by Zig, but not removed by LLVM optimization passes
- *not inlined*: function call that aren't inlined

Memory byte counts sum all operations of the same kind on a given source line,
within each generated function.
For generic functions, the maximum value is reported across all instantiations.

Apply annotations directly from optimized LLVM IR:

```sh
llvm-inline-annotations apply --ir input.ll
```

Alternatively, use `--report analysis.json`
to apply a saved report. Specify exactly one of `--ir` or `--report`.

## Zig build integration

Add this package as a dependency named `llvm_inline_annotations`, then:

```zig
const annotations = @import("llvm_inline_annotations");

// Inside build(b), after defining exe:
const dep = b.dependency("llvm_inline_annotations", .{});
const report = annotations.addAnalysis(dep.builder, exe);
b.step("analyze", "Summarize optimized LLVM IR")
    .dependOn(&b.addInstallFile(report, "analysis.json").step);
```

The helper returns a `std.Build.LazyPath` for `analysis.json`. Its only analysis
input is `exe.getEmittedLlvmIr()`.

The helper enables LLVM and debug information and upgrades Debug or unspecified
module optimization to ReleaseSafe. Other release modes are preserved. 
Shared modules inherit these settings. The analyzer runs on the host for cross builds.
