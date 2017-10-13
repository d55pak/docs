## Overview

This document covers our event definitions. Use this article to understand the events we track, what they mean, and how to add more events. If you want to implement these events, check the [implementation guide](https://docs.branch.io/pages/apps/v2event/).

## Pre-defined Events

These events are tracked automatically when you implement Branch.

### Impression

Loading of a user generated and placed impression pixel for the purpose of creating an attributing event from a marketing effort. By this definition, no automated renders from Branch (e.g. Journeys, Deepviews) are impressions, nor are views of content in the app.

### Click

A user initiated action of tapping on a Branch link or html element directly in front of a Branch link

### Web To App Auto Redirect

A web to app auto redirect works by simulating the action of a user clicking a link, but without user interaction. Technically this is implemented using "open_app=true" in our web to app products. Currently, this only exists on Journeys (+ banners + Web SDK Deepviews).

### Branch CTA View

The loading of a visual element or webpage that includes a Branch-created CTA, powered by a Branch link. Today, this includes loading Journeys and Deepviews.

### SMS Sent

An successfully triggered call to send an SMS (not necessarily receipt of the SMS)

### Open

A mobile app launch that is not an install (ie not a first time app launch for that persona). An "open" ends when an app is backgrounded or closed.

### Install

The first time an app launches for a given IDFA/AAID. (Excludes cases where the IDFA is reset with the app still installed.)

### Reinstall

When an app is deleted then re-installed on the same device (same device is defined as same IDFA/AAID).

### Web Session Start

A website launch (ie first page view). A session is considered to end after 30 minutes of inactivity (ie not launching a page or triggering an event).

### Pageview

A pageview is the loading of a single page for a given website which is triggered more specifically, by calling branch.init() or branch.track('pageview')

## Commerce events

Commerce events are pre-defined, as well, but fall into the higher level bucket of 'commerce events', where as events like 'install' don't have a pre-defined bucket.

These are events that relate to your customers interacting with commerce in your app, like adding payment information to their profiles, viewing items and adding them to your cart, and purchasing.

When you export events from the Branch dashboard, you won't be able to export individual commerce events like 'purchase', instead, you'll be able to export commerce events, which will consist of all individual purchase events.

The below events belong to the bucket of `commerce events`.

* Add to cart
* Add to wishlist
* View cart
* Initiate Purchase
* Add Payment info
* Purchase
* Spend Credits

## Associated Information With Events

### Always Present Information

All Branch events will have the following fields when exported:

| Name | Definition | Example
| --- | :-: | :-:
| id | ID of the event that occurred, unique. | 123456789
| name | Name of event that occurred. | pageview
| timestamp | Unix timestamp in milliseconds of when the event occurred | 1507929256
| origin | whether the event originated with a Branch SDK/API call, or third party | BRANCH
| os | os of the device where the event occurred. note that robots includes web and app robots | iOS
| os_version | os version of the device where the event occurred | 10.3.3
| environment| runtime environment where the event occurred, which can distinguish between e.g. full app vs instant app | FULL_WEB
| platform | convenience dimension that allows users to easily see web vs app, desktop vs mobile, and iOS vs Android vs other | IOS_WEB
| ip | IP address from which the API call tracking the event originated | 1.2.3.4

### Varied Data

The following Branch events will have the below fields.
