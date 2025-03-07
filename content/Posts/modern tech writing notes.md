Title: Elans notes abt MTW
Date: 2014-12-03 10:20
Category: Notes




# Modern Tech Comm

## Chapter 1 Basics:

### *Common misconceptions cleared up:*

#### Tech writers produce *formal* documentation
>- FORMAL: not stuffy or repetitive, "induces skimming"
>- Writing SHOULD NOT call attention to itself by being too formal or casual (can adapt to audience, like if chill coders lmao)

#### Tech writers produce *comprehensive* documentation
>- COMPREHENSIVE: minimum possible length
>- huge blocks of writing look intimidating, excessive content waters down useful content. Include only what the audience needs to know

#### Tech writers DO NOT help protect companies from lawsuits
>- Collage legalse into their website AT MOST 

#### Tech writers DO NOT ALWAYS produce PRINT documentation
>- minimalist "Getting Started" guide that directs people to a www web-page

### *Don't Write*

#### Tech writers are testers and researchers
>- your job to know what people want, communicating knowledge is the last step of the process (>10% of your time)
>- engage yourself in the writing process
>- performing testing is really just for increasing personal knowledge (don't have to test any further to de-bug)
>- **Goal**: be mentally equipped to ask intelligent questions to anyone within the scope of the tech -> talk!
>- This is your research. After this, you have to tediously verify it, then you can move on.

### Define the Audience

>- Don't need to do hand-holding here, if your audience needs it they're beyond help. Assume your audience has the pre-reqs to use this tech.
>- DO NOT GET STUCK IN THE QUAGMIRE OF TRYING TO HELP THE HELPLESS

#### *Users* are people who want to achieve something with an application
>- Concerned with input and output

#### *Administrators* install and configure applications
>- e.g. w.r.t the app: Where are the logs? How much disk space? How to recover data? How to backup?

#### *Developers* extend applications or interfaces with code.
>- Improve aspects of existing app or build something new
>- NEED references materials, short tutorials, code samples
>- Prioritize this, but if needed conceptual intros can be useful
>- Most **designers** are part of this grou

### Basic Functional Documentation (B F''n D)
*At a minimum, the following questions should be answered by the product documentation:*

#### What is this product and why would anyone want it?

>- If you can't answer this question, go back to research phase, as you must understand the audience
>- Honest, buzzword-free appraisal of capabilities and use cases

#### How does this product fit into a broader ecosystem, it at all? Does it have any dependencies?

>- Answer can be single sentence, architecture diagram, or complex discussion.
>- e.g. Web Frameworks being pared with complimentary products; developers must know which ones prior to installation

#### When can I achoir this product? Which of the possible many distribution packages should I choose and why?

>- Self xplantorie

#### How do I install the product? What are the basic configuration options?

>- Consumer applications should barely need this
>- Server apps REALLY need this, often longest part

#### What does a simple, start to finish operation look like?

>- Take user from nothing to something
>- Convince readers that they've learned something

##### BONUS: DON'T WRITE FROM MEMORY. Always verify content, even code/shell commands

### Style

>- *CONSISTENCTY IS KING.* Don't call something a dialogue in one document and a pop-up in another, for example.
>- Bias towards including headers, tables, lists, diagrams, and images. Makes writing more approachable and easier to scan
>- Use inline styles to offset important text
>- Typically using **bold** for user interface elements and *italics* for emphasis
>- Don't verbify obscure nouns: "Grep it" vs "You can use grep to search the file"
>- Copy edit, but don't obsess

### Catalogue the Diff

>- An import aspect of tech writing is to record changes to a product
>- Good change logs can inspire confidence in a product and people to to upgrade
>- What's new/different/removed? How to upgrade? Any "gotchas"?
>- New simple features => just noting they exist is fine
>- Terse, minimalist, and scannable

### Build a Website

>- simple as
>- hosting content on a website gives you the power to fix inaccuracies and sync content with latest version of software, INSTANTLY
>- Distributing PDFs does not allow for this

### Help Others Write

>- Writing and distribution should encourage others to contribute!
>- Even a large team of writers can't know everything worth knowing about an app
>- Open source, mod scene, obscure wikis, prove people will share expertise and passion if it's easy and hospitable for them to do so => PEOPLE WILL CONTRIBUTE IF YOU LET THEM
>- Ultimately your job to ensure quality of documentation

### Publish Frequently

>- Not a special, challenging event, just quick sanity check and glance build log. Simple and functional

## Chapter 2: Specifics

**How do tech writers tech write?**

### Use Lightweight Markup

>- Human readable
>- Not overly dense with computer syntax
>- Free and easy to use/create with any free/open-source text editor
>- MICROSOFT WORD IS NO GOOD - same issue with PDFs as mentioned before

### Use Distributed Version Control

>- Better performance
>- Allow for offline work
>- superior for concurrent work on same file (COMP 3350)
>- Use *_MODERN_* tools, like GitHub(Enterprise, Desktop) and SourceTree

#### Pros
>- Documentation and code branches stay in sync
>- Developers are more likely to contribute if they don't have to clone a separate repo

#### Cons
>- Large repository (>= 2GB) can dramatically slow down documentation builds
>- Documentation changes can become bogged down with commit hooks, pull requests, and submission policies that are designed for stable code bases

#### README of the repository root 

>- quick product summary
>- instructions on how to build the documentation locally
>- instructions on how to contribute

### Don't Duplicate

>- Use (links)[] to get the holy grail of tech writing, *single sourcing*
>- Core Idea: break writing into bite-sized pieces, called **topics**
>- A **topic does NOT overlap in content with another**
>- This means you only have to update one thing when things change, and things will change.
>- Keep topics short and complete in their discussion
>- Assume very litle knowledge of previous topics (unlike books with chapters) and include links to other topics if needed

#### Version Control and Duplication

DO **NOT** STORE ALL SIMILAR COPIES OF DOCUMENTATION IN VERSION CONTROL. It's not going to help if you have a heap of different manuals and make users sift through them to find the one for them.

>- A solution - _Conditional Text_: selectively include/exclude portions of the file depending on cases. Can be hacky and not supported in markdown. Do not rely on it entirely

### Make Static Websites

>- simple as
>- Intuitive reason for using these based off of all the discussion in this book and class lectures

### Rsync

>- Tool: Transfers only files that need to be added or updated, delete stale files.

### Metrics

>- Use Google Analytics and track the static site
>- Serve as a check against your thoughts and intuition: if your docs aren't popular maybe you're doing something wrong, maybe users will report errors

### Script Your Complexity Away

>- If you're actually making a PDF, you need a publishing pipeline. Don't do all this yourself, use modern technology. Can even build it both as a PDF and HTML for a static site!

### The Legal Problem

>- "In short, assholes ruin everything": Patent trolls using your docs as evidence for copywronging
>- May have to hide docs behind customer login for one of these reasons

### Localization

>- Translating other documentation into other languages = NIGHTMARE
>- Perform cost benefit analysis, then triple it L O L 
>- Update doc, send it to translation company, THEN WAIT, build, and publish
>- This delays releases in other regions

### Contrived Workflow

>- example of irl scenario, page 33 if you're interested

### What About Wikis

*Have a place in tech writing but think carefully before selecting one*

#### Pros

>- Users don't need to install any apps, clone repos, learn workflows, to contribute
>- Users can spot issues and fix them very quickly
>- Every wiki has out of the box search (as opposed to static site)
>- Great for living docs that grow over time, don't need to be marked as belonging to a particular software version

#### Cons

>- Wikis are web apps, require hosting and maintenance over time (can crash and/or slow down - needs scaling). As a tech writer, you don't care about managing websites
>- Writing on a wiki sucks, mangled html tags with lightweight markup, as you're literally writing on the wiki app, which means if your connection is disrupted you could lose your work during writing/editing
>- Version control with "blame" for problematic content doesn't exist, it's really just last person to edit has ownership (wikipedia has edit history to discourage destruction/vandalism)
>- Not local


## Chapter 3: The Grand Finale

Just a high level summary

1. Learn everything about a subject
2. Write down exactly what an audience needs to know and _no more_
3. Make the content beautiful, discoverable, scannable, and searchable
4. Consider everything a draft and iterate relentlessly
5. Make contributuon simple