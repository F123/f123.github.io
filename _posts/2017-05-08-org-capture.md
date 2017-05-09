---
layout: post
title: org-capture
author: Rill
excerpt: Using org-capture for your todo list or journal
tags: [emacs, org]
permalink: /blog/org-capture/
---

You may want to keep a todo list or a daily journal. Often managing
such a list or file is troublesome and time-consuming. `org-capture`
helps make this possible without interrupting other work.
	
1.  Here's the text of my capture-prepare.el file:[^1]
    
        (setq org-default-notes-file (concat org-directory "/notes.org"))
        (define-key global-map "\C-cc" 'org-capture)
             (setq org-capture-templates
            '(("t" "Todo" entry (file+headline "~/org/notes.org" "Tasks")
                "\* TODO %?\n  %i\n  %a")
            ("j" "Journal" entry (file+datetree "~/org/journal.org")
                "\* %?\nEntered on %U\n  %i\n  %a")))

2.  `c-c c` gets you to a place where you can enter ""t for todo or
    "j" for journal. Todos are kept in one file and the journal in
    another.[^2]

3.  Just type. You're in orgmode.

4.  Press `c-c c-`c to finish. Your stuff is saved and you are back to
    where you were when you wanted to write something down.

Notes
-----

[^1]: You can change the file names and directories to fit your situation.

[^2]: You can modify the lines above to change the letters, file names
    and directory or add additional items.
