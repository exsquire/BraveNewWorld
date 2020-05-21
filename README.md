# BraveNewWorld \[Work in Progress\]
My way of cataloguing and playing around with the new (to me) industry techniques

(Oh my gosh there are so many...)

## A note on cheatsheets
**Use Them.** Wallpaper your desk with them. Unfortunately, you cannot become a master of everything instantly. What you CAN do is build intuition - know what kind of powers you have access to with different languages, tools, or methods. If you know that, you can find it. If it's right in front of you, you can find it faster. Faster lookups means more repetition, more repetition means faster and learning. 

## Code in general
### Commandments:
1. Code is read more often than it is written. Think hard about what someone new to the language would struggle with and comment the purpose or action of that line accordingly. 
2. Function names should be verbs. Variable names should be nouns. 
3. There are different ways of naming variables. thisIsCamelCase, this_is_snake_case, ThisIsPascalCase. Different languages have different guidelines of when to use which. Knowing about them helps keep code consistent, which is important for reading it. 

## Python in general
1. List comprehensions look scary, but become second nature with a little practice \[**VALUE**\]. 

## Git and Github in general 
[Personal favorite beginners guide.][https://rogerdudler.github.io/git-guide/]
The unknown is scary. This is universal. There are many, many unknowns with git that make is seem really, really scary. In reality, there are very few commands to learn to use git for collaboration. Here is what I've learned from my betters:

### standard git workflow
1. git clone: copy a directory from github to your workstation
2. git branch: where am I?
2a. git branch -a: Oh no, I'm in the master branch, now I see all the branches
2b. git checkout: I want to be in the develop branch, let's "check that one out". I am now in the develop brach. 
3. do code, maybe add some files or folders
4. git add: We want to be very specific about what we add to the repository - add specific code files, data, folders, etc. to the "staging area".
5. git commit: Save a parcel of work - do this often. It is a snapshot of what is currently in your "staging area". 
6. git push origin branch: push the contents of your LOCAL stage to your REMOTE repository (on github). 

### Branching: Get used to it - it's a little to learn for a lot of power and collaboration experience \[**VALUE**\]
1. Never stay on your master branch - that is for airtight, unit-tested (more on this later), complete products. Do not sh\*t on the temple floor. 
2. Create and do all your work in a "dev" or "develop" branch, on github set dev branch as default. Once you have a bare minimum "working" product, DON'T TOUCH IT ANYMORE, see step 3 for how to build muscle for code collaboration, even by yourself. 
3. Modifications to the develop branch fall roughly into 2 categories - "features" and "bugfixes". Instead of working from the develop branch, make a NEW branch to address one of these modifications. Name scheme is "\[modification_type\]/\[description\]", e.g. "feature/make_pretty_graph" or "bugfix/dont_explode_if_this_happens"
4. Once the modification branch is complete, make a pull request to the develop branch on github. This says to the administrator of the page, "Hey, I've done some work to the stuff in this branch. Please look it over and add my changes if you like them."
5. Admins of the repository (you?) will get a notification of the pull request and will see the old code and new code side-by-side. They can comment, ask questions, suggest changes, and eventually deny or accept the pull. In a team setting, a certain number of other developers may be asked to do this in a process called "code review". If everyone signs off, it passes the review.  
6. Once the pull is reviewed, merge it into the development branch. You have just made progress. 

## BASH in general
1. Learn to use Tmux - zero effort to learn, command line gets less sucky forever. \[**VALUE**\]\[**VALUE**\]\[**VALUE**\]
2. BATS: Bash Automated Testing System - because pipelines use bash, and testing bash is awful. 

## Sequence data in general
It's really not that bad once you understand all the players.
**Sequencers**: takes in samples and spits out reads
**FASTA/FASTQ**: files that store the reads, fastq is fasta but with quality scores for each base
**Aligner**: [More flavors than BaskinRobins][https://en.wikipedia.org/wiki/List_of_sequence_alignment_software]. Spits out a SAM file, which is a text file with all the sample reads aligned to the reference genome - so now all these floating strings have a genomic position and other information about how the alignment went. 
**SAMtools**: Swiss army knife for working with SAM files.
  - Common workflow: SAM -> BAM (memory effecient samfile) -> Sorted BAM (required for indexing) -> Indexed BAM (very quick to parse). 
  


