---
repo: dalenguyen/firebase-functions-snippets
url: 'https://github.com/dalenguyen/firebase-functions-snippets'
homepage: null
starredAt: '2023-06-04T04:15:18Z'
createdAt: '2018-02-28T20:28:58Z'
updatedAt: '2025-12-09T13:24:44Z'
language: JavaScript
license: NA
branch: master
stars: 72
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:58.591Z'
description: Awesome Firebase Functions snippets that cannot be ignored
tags:
  - firebase
  - firebase-functions
  - snippets
---

# Awesome Firebase Functions Snippets

Here contains all my works that involves with writing firebase functions

In order to use this, you should know how to create and deploy firebase functions. If you don't, please read [Get started](https://firebase.google.com/docs/functions/get-started)

## CI / CD

- [Google Cloud Build](/ci-cd/cloudbuild.md)
- [Github Actions](/ci-cd/github-actions.md)

## Others

- [Easy to test Firebase Functions locally](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/local-test-easy.js)
- [Export from Firebase Functions to CSV or JSON](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/csv-json-export.js)
- [Dealing with HTTP Request](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/http-request.js)
- [Send SMS with Twilio](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/send-sms-with-twilio.js)
- [Send Email with Sendgrid](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/send-email-with-sendgrid.js)
- [Send Email with Mailgun](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/send-email-with-mailgun.js)
- [Send notifications with Slack](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/send-notifications-with-slack.js)
- [Create a revison on every updates](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/revisions.ts)
- [Schedule a function](https://github.com/dalenguyen/firebase-functions-snippets/blob/master/schedule.ts)

The CSV or JSON code will get a HTTP request and return a JSON or CSV file that user wants. You can either call the request direction from your browser or you can user [cron-job.org](https://cron-job.org/en/members/jobs/details/?jobid=919859).
