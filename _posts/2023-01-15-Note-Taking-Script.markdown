---
layout: post
title:  "Automating My Meeting Notes"
date:   2023-01-15 12:31:56 -0400
categories: projects
---


## Automating My Meeting Notes with Google Calender

Each day I run a script([code here](https://github.com/jbamford/google-calander-dendron)) that fetches the events on my google calendar. For each event, the script creates a meeting note template that I can fill out during the meeting. In addition, the script creates one daily journal note that contains a link to each of the meeting notes. 

Each meeting note has the template:

—-
```
## Attendees

john[@example.com](mailto:jason@example.com), smith@example.com

## Questions to ask

## Goals

<!-- Main objectives of the meeting -->

## Agenda

<!-- Agenda to be covered in the meeting -->

## Minutes

<!-- Notes of discussion occurring during the meeting -->

## Action Items

- [ ] Goldfish Actions

- [ ] Client Actions
```
—-
