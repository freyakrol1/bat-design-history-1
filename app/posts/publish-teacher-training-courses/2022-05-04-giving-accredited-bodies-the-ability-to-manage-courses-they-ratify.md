---
title: Giving accredited bodies the ability to manage courses they ratify
description: We added a way for accredited bodies to manage their training partners’ courses
date: 2022-05-04
tags:
  - PN014
  - PN016
screenshots:
  items:
    - text: Training partner course list with permissions
      src: training-partner--course-list-with-permissions.png
    - text: Training partner course list without any permissions
      src: training-partner--course-list-no-permissions.png
    - text: Training partner - draft course with permissions
      src: training-partner--draft-course-with-permissions.png
    - text: Training partner - draft course without permissions
      src: training-partner--draft-course-no-permissions.png
    - text: Training partner - published course with permissions
      src: training-partner--published-course-with-permissions.png
    - text: Training partner - published course without permissions
      src: training-partner--published-course-no-permissions.png
---

This work builds upon the changes we introduced to:

- [allow lead schools to manage their accredited body relationships](/publish-teacher-training-courses/managing-accredited-bodies-if-youre-a-lead-school/)
- [give lead schools the ability to manage permissions for their accredited bodies](/publish-teacher-training-courses/giving-lead-schools-the-ability-to-manage-permissions-for-their-accredited-bodies).

## User needs

The user needs this work aims to address are:

{% from "user-needs/macro.njk" import appUserNeeds %}
{{ appUserNeeds({ items: collections['user-need'] | slugs(tags)}) }}

## What we changed

We have updated the ‘Training partner’ section to show the actions permitted by the training partner.

Permitted actions include:

- Adding courses - this also includes deleting courses
- Changing courses
- Publishing courses
- Updating course vacancies
- Withdrawing courses

We made these changes so that users of the accredited body:

- do not need to be members of their training partners to be able to manage courses they ratify
- can see which actions have been given to them by their training partners

## How it works

By default, users of an accredited body can only view their training partner’s courses in the service.

If their training partner has given the accredited body permission, they may also be able to manage the training partner’s courses.

### Courses list

On the courses list page, we show:

- an ‘Add course’ button - if the accredited body has the ‘Add courses’ permission
- change links for course vacancies - if the accredited body has the ‘Change course vacancies’ permission

### Course details

On the course details pages, if the course is in a ‘draft’ state, we show:

- a ‘Publish course’ button - if the accredited body has the ‘Publish course’ permission
- a ‘Delete course’ link - if the accredited body has the ‘Add courses’ permission

If the course is published, we show links for:

- View on find
- Change vacancies - if the accredited body has the ‘Change course vacancies’ permission
- Withdraw course - if the accredited body has the ‘Withdraw course’ permission
