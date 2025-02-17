---
title: Adding primary navigation to the service
description: Helping users navigate parts of the service with primary navigation
date: 2022-03-25
screenshots:
  items:
    - text: Single organisation user - lead school
      src: primary-navigation--single-organisation-user-lead-school.png
    - text: Single organisation user - accredited body
      src: primary-navigation--single-organisation-user-accredited-body.png
    - text: Multiple organisation user - lead school
      src: primary-navigation--multiple-organisation-user-lead-school.png
    - text: Multiple organisation user - accredited body
      src: primary-navigation--multiple-organisation-user-accredited-body.png
    - text: Change organisation
      src: organisation-list.png
    - text: Your account
      src: your-account.png
eleventyComputed:
  eleventyNavigation:
    key: publish-adding-primary-navigation
---

We have observed that users find it hard to navigate the service.

We wanted to provide a way to navigate the service that was:

- clear - removes any doubt about what the section contains
- simple - uses plain English and familiar words
- obvious - avoided overlap between items, for example, ‘courses’ and ‘courses as an accredited body’
- consistent - available throughout the service

## Service home page

The service’s home page includes guidance and links to the following sections:

- About your organisation
- Locations
- Courses
- Courses as an accredited body - if the organisation is an accredited body
- View your PE allocations - if the organisation is an accredited body
- Users - shown in a grey sidebar

If the user goes to one of the sections, they can return to the home page by clicking on the service name in the header or using the backlink. They cannot move to another section without first going back to the home page.

## Data analysis

Using the Publish database, we looked at the:

- number of organisations per user
- length of organisation names

### Number of organisations per user

Understanding the relationship between users and organisations helps us make decisions about:

- when to show specific interface elements
- what content to show

For example, we show a way to change the organisation if the users belong to multiple organisations.

From the data, we found that:

- 82% of users belong to 1 organisation
- 11% belong to 2 organisations
- 7% belong to more than two organisations
- the average number of organisations per user is 1.5
- the maximum number of organisations per user is 16

This data suggests that a relatively small number of users must choose an organisation when managing their courses.

We need to make it possible for users who belong to multiple organisations to change their organisation easily.

### Length of organisation names

Understanding the length of organisation names helps us make decisions about:

- what interface elements we can use
- where to place the organisation name
- how the organisation name may look in different situations

For example, long organisation names will cause content to wrap, whilst short names may be lost amongst other content.

From the data, we found that the:

- average length of organisation name is 28 characters
- maximum length of organisation name is 95 characters
- minimum length of organisation name is 4 characters

For users who belong to multiple organisations, we need to make it easy to know which organisation they are currently viewing.

## What we changed

We have:

- added a primary navigation bar
- added a way for users to change their organisation - if the user belongs to multiple organisations
- updated breadcrumbs to better match the structure of the service
- updated backlinks
- updated heading captions

## How it works

### Signing in to the service

When signing in to the service, users see either:

- the list of courses - if they belong to one organisation
- a list of organisations - if they belong to multiple organisations

### Primary navigation

The primary navigation persists throughout the service, except when someone is viewing ‘Your account’.

We do not show the primary navigation in the ‘Your account’ section because the navigation relates to an organisation, not a user.

The primary navigation includes links to:

- courses
- locations
- users
- organisation details

If the user belongs to an accredited body, we also include links to:

- training providers
- PE allocation

We changed ‘courses as an accredited body’ to ‘training providers’ because the link takes the user to a list of training providers who run courses on behalf of the accredited body.

### Changing organisation

If the user belongs to multiple organisations, they can select which organisation they want to view and easily switch between them.

The organisation ‘switcher’ sits above the primary navigation. It includes the name of the current organisation and a ‘change organisation’ link.

Everything below the organisation switcher, for example, the primary navigation and the courses list, relates to the chosen organisation.

Changing an organisation shows a list of the user’s organisations. Choosing one of these organisations takes the user back to the courses page, with the selected organisation name displayed in the switcher.

### Breadcrumbs

We use breadcrumbs to help orientate the user within the ‘Your account’ section.

The breadcrumb includes a ‘home’ link to help users get back to:

- the list of courses - if they belong to one organisation
- a list of organisations - if they belong to multiple organisations

### Backlinks

We use backlinks within a flow, for example, when adding a course. Backlinks allow the user to navigate back through the flow without using the browser’s back button.

We do not use backlinks on the main section pages, for example, ‘courses’ or within a course, since users can use the primary navigation to get back to the start.

### Heading captions

We only show heading captions where the heading may be ambiguous or a duplicate of another page in the service.

Previously, we included the organisation name in some heading captions. We have removed these for users belonging to a single organisation and multiple organisations.

Users belonging to a single organisation will know the organisation’s name.

We show the organisation name in the switcher for users belonging to multiple organisations.

An exception is when a multi-organisation user views email notification settings. We need to replay the organisation’s name as it does not exist anywhere else.

## Further considerations

In future, we may consider:

- improving the way users can change the recruitment cycle during the rollover period
- what menu options are available to different types of users based on their permissions
- combining courses the organisation runs and courses the organisation’s partners run into one filterable list
