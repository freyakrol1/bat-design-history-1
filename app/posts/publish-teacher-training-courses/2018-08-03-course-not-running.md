---
title: Course statuses – 3 August iteration
description: A more indepth look at UCAS course status and how it will affect publishing
date: 2018-08-03
screenshots:
  items:
    - Courses with status column
    - A course that is not running
    - A course that is running
---

As a user looking at all of my courses imported from UCAS, I need to know which of those courses have been published, so that I know which courses applicants are seeing.

An iteration on the [first UCAS course status design](/publish-teacher-training-courses/ucas-course-status). Following that design we found that status in UCAS is per training location rather than per course. We need some logic to determine whether a course should be published based on the status of its training locations.

## Separating out UCAS status

The UCAS statuses are per location, not per course. Instead of repeating those statuses give an indication of the affect of those statuses on the course. State whether a course is running, not running, or not running because it is new.

Courses can have 1 of 3 statuses:

- Running - the course is published and applicants can see it on search
- Not running – the course is not published, it cannot be found on search
- New - not yet running – the course is not published yet because it has not been set to publish on UCAS

## Resolving course status from training location statuses

If any training location has the status ‘Running’, then the course is running and we publish it, otherwise we do not publish.

If no locations are running, but at least one is ‘New’, then the course is ‘New - not yet running’.

If all locations are ‘Discontinued’ or ‘Suspended’, then the course is ‘Not running’.

We hypothesise that a user needs to know the difference between a course that is not running because it was stopped and one that is not running because it’s not ready to go live yet.

## Courses that are not running

Courses that are not running cannot be edited. The fields and publish actions do not show.

[Trello ticket](https://trello.com/c/BOvg2Duh/46-design-workflow-for-courses-that-are-not-published-because-of-their-ucas-status)

*[UCAS]: Universities and colleges admissions service
