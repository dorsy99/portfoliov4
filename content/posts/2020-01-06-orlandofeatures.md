---
title: It's Release Season for ServiceN(Orlando)w
type: post
tag: 
  - ServiceNow
summary: My hot tips for ServiceNow Orlando release
date: 2020/01/06
author: Andrew
---

Another half a year, another ServiceNow release notes to go through! Only two days ago the Release Testing Preview of the ServiceNow Orlando version was made live for non-production instances. I know it's a bit weird, but I love reading [release notes](https://docs.servicenow.com/bundle/orlando-rtp-release-notes/page/rtp-rn/family-release-notes.html)! I've had a quick squizz and here's my pick of cool features and things to get excited about in list form.

Just a note: My background is ITSM / Platform, so I may not see or highlight cool stuff from other modules I haven't used. 

<!-- more -->

## API Changes
- FlowAPI "cancel()" - I don't know why this wasn't included earlier? But yay, it's here now!

## Agent Workspace

Another big update for Workspace (as we suspected) - too much to list really, check the notes yourself :)

- Customization! 
  - Build a custom landing page
  - Add custom components to the ribbon
  - Branding with Colours and Logos!
- New form & list features
- URL Sharing
- Knowledge Management (woo!)

## ATF

- Ability to test Email notification with new email validations
- HEAPS of new Quick Start tests for all kinds of platform features

## [CSDM](https://community.servicenow.com/community?id=community_article&sys_id=f54be0f7db984c146064eeb5ca961941)

- New attributes for all items in the CMDB:
  - Environment (prod/dev etc)
  - Managed By group
  - Internal/External for DMZ

## CMDB
- A new "Principal Class" filter which can make life so much better for your agents. This applies to all your CMDB reference fields AFAIK. That's Awesome!

## Dashboards / PA
- New personalization to automate filtering to specific users. "My Jobs" rather than "All jobs" is how I read this one.

## Discovery
- Deprecation of WMI in preference of PSRemote. Very interesting!
- TLS certification discovery and management
- Microsoft JEA for Discovery via powershell
- new patterns and plugins in the Store

## Flow Designer
- Create a flow with an SLA Task trigger
- Manage files and directories with an SFTP step
- Run a flow or subflow dynamically
- Transform data pill values with transform functions
  - Transform data pill values without the need to write a script. Use transform functions to reformat text, perform mathematical calculations, sanitize potentially unsafe SQL statements, and serialize complex objects to raw XML.
  

## Imports and Exports
- REST (IntegrationHub) type data source
  - Import data into the ServiceNow Import Sets table using the REST type data source through the IntegrationHub. You can specify pagination to reduce processing overhead.
- Custom script data sources
- **Robust Import Set Transformation**
  - Use robust import set transformers instead of transform maps if you want to extract, transform, and load data to one or more target tables. Use ETL definitions to map source table columns to target table columns and to define operations and processing instructions. Very cool!


## IntegrationHub
- Dynamic outputs
  - Similar to Dynamic Inputs... New pill types and data gathering options
- Dashboards for subscriptions and usage
- Transform functions to reduce the reliance on script

## Studio
- Better integration with GitHub, allowing modification of files outside of platform (aiding in the VS Studio plugin usage, I believe)
- Commit change management
- Logpoints (like breakpoints, but for logging!)

## Virtual Agent
- Multiple brandings for a single instance
- Send notifications directly to Slack / messaging stuff

## Walk-up Experience
- Badge Reader integration 
  - I'm interested to see how this one plays out. Auto-sign-in is something WUX was missing.


I'm sure there's heaps more that will show up, so subscript to the #Orlando channel in SN Devs Slack - I know I have.

Lets all book our subprod upgrades ASAP! It's easy ;)

`Andrew`