---
title: Google Adwords Overview
description: An overview page of using Branch in your Google Adwords campaigns.
path: tree/master/src/pages/deep-linked-ads
source: google-ads-overview.md
---
# Google Adwords Overview

## Overview

With Branch, you can put deep links in every type of Google AdWords campaign, improving conversion rates and letting you measure the impact of your campaigns on mobile.  

The Google AdWords interface can be confusing so we've created a guide to help you find the right documentation. The new AdWords interface (released in beta in May 2017) still follows roughly the same campaign creation flow. We'll update this page as needed if the campaign creation flow is updated, or new ad types are supported.

## Connect AdWords Account

When you connect your AdWords account with Branch, we'll automatically collect relevant campaign information. We use the AdWords connection to *retrieve* campaign performance. We do not make any modifications or updates to campaigns once your AdWords account is connected.

When you connect, you'll select all the AdWords accounts to link. If you do not have a Manager (MCC) AdWords account, you will only see one option. If you have a Manager (MCC) account, you will see the Manager Account and the descendant accounts that stem from the Manager account.

### Collected Data

Once connected, we will automatically retrieve campaign performance for AdWords campaigns powered by Branch. The data we collect:

- Campaign ID
- Campaign Name
- Ad Group ID
- Ad Group Name
- Ad ID
- Impressions
- Clicks

We will automatically filter out any campaigns that do not have matching Branch data.

## Campaign Type Support

This documentation supports the following Google Campaign types:

Google Campaign | Campaign Type/Objective | Branch Documentation Link | Branch Ad Format
--- | --- | --- | ---
Search Network | Mobile app engagement | **[link](/pages/deep-linked-ads/google-search-engagement-ads)** | App Only: Engagement
Search Network | Standard  | **[link](/pages/deep-linked-ads/google-xplatform-search-ads/#standard-search-ads)** | Cross-platform Search
Search Network | Dynamic Search Ads  | **[link](/pages/deep-linked-ads/google-xplatform-search-ads/#dynamic-search-ads)** | Cross-platform Search
Display Network | Engage with your mobile app | **[link](/pages/deep-linked-ads/google-display-engagement-ads)** | App Only: Engagement
Display Network | Others (Visit your website, Influence, etc.)  | **[link](/pages/deep-linked-ads/google-xplatform-display-ads)** | Cross-platform Display
Video | Mobile App Installs | **[link](/pages/deep-linked-ads/google-video-ads/#video-app-install-ads)** | App Only: Install
Video | Standard | **[link](/pages/deep-linked-ads/google-video-ads/#video-standard-ads)** | Cross-platform Display
Universal App Campaigns | Universal App Campaigns | **[link](/pages/deep-linked-ads/google-uac)** | App Only: Install

For setup instructions for Adwords Conversion tracking with Branch check out **[Google Conversion Setup](https://docs.branch.io/pages/deep-linked-ads/google-conversions)**.
