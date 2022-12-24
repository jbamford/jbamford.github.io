---
layout: post
title:  "A Second Brain"
date:   2022-12-24 12:31:56 -0400
categories: projects
---


## A Second Brain

<p align="center">
<img src="/images/knowledge-data.png" alt="drawing" width="350" style="center"/><br>
<i>Each dot represents a new note. Notes are clustered around topics in a hierarchy. 
<br>
297 Linked Edges across 927 Notes</i>
</p>

Jan 1, 2022, represents two and a half full years of using various markdown note-taking techniques in an effort to categorize and store both personal and work-related information. My note-taking routine went through various iterations. From Mac’s Note Pad, Evernote, Obsidian, Foam(vscode plugin), and Dendron(vscode plugin). 

A benefit of local storage text-based note-taking is that all the data is transferable between different note-taking applications. All of the “note” information is stored in basic text in a file on my computer. The various different note-taking software packages read these files(usually with their own custom decorators) and serve up your notes in a fancy (or not so fancy) user interface. 

Over the two and a half years my goals have been to:
* Quickly make a new note about topics and properly categorize them
* Easily Search notes
* Have notes for work-related meetings (a mini CRM)
* Keep track of TODOs

In 2022 I started using [Dendron.io](https://www.dendron.so/), and this has been my favorite application so far! Prior I was using Foam, but have found that Dendron takes ease of use, customization, and accessibility up another level. 

### Note-Taking Structure: 

My Vault, as Dendron describes it, is comprised mainly of my Journal, Personal, and Work-Related branches. In addition, I have branches for Technology, Tasks, and Meetings. 

The notes are structured in a hierarchy folder-like structure, however instead of actual folders on my computer all notes are single files, and their hierarchical path is created by using “.” as a seperator the file name. 
For example, my daily journal notes are stored in the hierarchy: Journal>Year>Month>Day.md. 
Real Example: journal.2022.12.22.md(its just one file at the top level).

Also, one of the best parts of a Roam Research/Zettelkasten note-taking system is you can link to other notes from a note. This creates a web of interlining information building up to your “Second Brain”. 

### Routine
Every day I run a custom python script that will pull in today’s event from my Google Calander(more on this another day). 

This script creates:
* One daily Journal File(with link references to the meeting files)
* Meeting files for each event in the day

An example journal Note journal.2022.12.22.md might constrain:

<p align="center">
<img src="/images/general-journal-note.png" alt="drawing" width="350" style="center"/><br>
</p>

For each event, there’s an easily accessible link to the meeting notes file. The meeting notes file has a space for me to input (meeting goals, agenda, meeting minutes, and next steps). This system has kept all my meetings very organized and fewer action items slip after meetings. Stay tuned for a deeper dive into the structure of the meeting notes in a future post. 

### General Notes
When something comes up during the day that isn’t meeting/task/work-related, maybe I learned something new or come across a neat fact, I quickly add it to an existing note on that topic or create a new one in the corresponding hierarchy. If the new bit of knowledge is related to something I've been working on I can add a reference to that note with a backlink.  
