---
title: 'mothur v.1.4.0'
redirect_from: '/wiki/Mothur_v.1.4.0.html'
---
We are happy to release [mothur v.1.4.0](/wiki/mothur_v.1.4.0)
today, June 21, 2009 (aka Fathur's Day). Since the May release we have
added an additional 120 users. Thanks to the 466 of you for your
continued support! We are very excited about this release. With this
release you can go from the fna file generated by a pyrosequencer to
Venn diagrams in a pretty short period of time, without having to leave
mothur. Yes, we have added a function to [ trim](/wiki/trim.seqs)
primers off of your sequences and generate a group file based on barcode
sequences, [ align](/wiki/align.seqs) those sequences to any
reference alignment you might like, and [ screen
sequences](/wiki/screen.seqs) based on their quality and start and
end positions. The [ aligner](/wiki/align.seqs) is parallelized so
that you can do your alignment on as many processors as you desire (same
goes for the distance calculator, [dist.seqs](/wiki/dist.seqs)). In
addition to a number of other commands, which are described below, we
have added options to previous commands. For example, if you request a
rarefaction be calculated for a distance of 0.03, but that line doesn't
show up in the \*list file, mothur is now smart enough to use the
previous line. Another option is the ability to run mothur commands off
the command line in what we are calling [command line
mode](/wiki/command_line_mode). We have also done our best to
remove a number of bugs and memory leaks. Please forward us any bugs you
encounter along the way. Finally, you should notice a reorganization of
the wiki pages so that the command names correspond to the page names.

There are also several news items of note:

-   In the coming months mothur will be moving. I have taken a job at
    the University of Michigan in the Department of Microbiology &
    Immunology. Because of this, we have secured the
    [https://www.mothur.org](https://www.mothur.org) domain and will be moving the mothur wiki to
    that site in the next month.

<!-- -->

-   We received a phenomenal level of interest in the July workshop to
    be held at the University of Massachusetts - 30 people(!) will be
    attending. My wife fears that the Tuesday night BBQ will turn into a
    kegger. I also have received a number of invitations for the Fall
    and Spring semester. It's great to see so much interest.

<!-- -->

-   The mothur manuscript is written and we have 8 non-UMass co-authors.
    I consider that a great success for this open source experiment.
    Feel free to check out their contributions on the [analysis
    examples](/wiki/analysis_examples) page. Also, you have until
    Monday, June 29, to post an example and be included on the
    manuscript. If you haven't seen it and think you should be a
    co-author, please let me know.

<!-- -->

-   I have been approached by several people about (i) writing letters
    of support for proposals, (ii) being a co-PI, (iii) being a
    subcontractor and (iv) doing people's analysis for them (for free).
    Please see the collaboration link on the
    main page of the wiki for collaboration options.

If you haven't noticed, we're very excited about the mothur project
and have big plans. Next up on our docket is incorporating a
Bellerophon-like chimera checker, a classifier, and the ability to
essentially parallelize the [cluster](/wiki/cluster) command. If
you have ideas, please don't hesitate to get in touch.

Happy Fathur's Day!

## Major updates

-   [align.seqs](/wiki/align.seqs) - generates an alignment to a
    user-supplied template alignment database \[pds\]
-   [summary.seqs](/wiki/summary.seqs) - outputs statistics
    regarding a collection of sequences \[pds\]
-   [screen.seqs](/wiki/screen.seqs) - screen sequence and name,
    group, and/or align.report files based on whether sequences satisfy
    user-defined criteria \[pds\]
-   [reverse.seqs](/wiki/reverse.seqs) - outputs the reverse
    complement of a file of sequences \[pds\]
-   [heatmap.sim](/wiki/heatmap.sim) - creates a heatmap based on
    groups similiarity.
-   [get.rabund](/wiki/get.rabund) - outputs an rabund file
-   [get.sabund](/wiki/get.sabund) - outputs an sabund file
-   [trim.seqs](/wiki/trim.seqs) - trims and culls sequences based
    on user-defined criteria, barcodes, and primers
-   [merge.files](/wiki/merge.files) - concatenates a list of files

## Minor updates

-   [tree.shared](/wiki/tree.shared) command now allows you to
    input a distance file \[sw\]
-   added "smart" distance recognition on all commands using the label
    parameter \[sw\]
-   added a "name" option to [unique.seqs](/wiki/unique.seqs)
-   added ability to omit () on the [quit](/wiki/quit) command
    \[sw\]
-   the deconvolute() command is now called the
    [unique.seqs](/wiki/unique.seqs).
-   the [bin.seqs](/wiki/bin.seqs) and
    [get.oturep](/wiki/get.oturep) commands now accept a group
    file. If you provide a group file they will append the group info to
    the sequence name and bin number \[sw\]
-   no longer support sequence files in nexus, clustal or phylip form
    \[sw\]
-   [dist.seqs](/wiki/dist.seqs) now has the ability to output a
    phylip formatted distance in addition to the column format. To do so
    use the parameter phylip=t \[sw\]
-   sharedmultiple.summary file is only generated from the
    [summary.shared](/wiki/summary.shared) command when there are
    more than two samples \[sw\]
-   [dist.seqs](/wiki/dist.seqs) can now use n processors.
-   the heatmap command is now called
    [heatmap.bin](/wiki/heatmap.bin).
-   modified how the [help](/wiki/help) command is called
-   created the [command line mode](/wiki/command_line_mode)

## Bug fixes

-   fixed infinite loop if mothur is given a non-existent batchfile
    \[sw\]
-   fixed [get.group](/wiki/get.group) command. \[sw\]
-   optimized [summary.shared](/wiki/summary.shared) command \[sw\]
-   ability to use -1 in a distance file to represent infinity \[sw\]
-   [tree.shared](/wiki/tree.shared) command creates trees with
    root to tip length of 0.5 \[sw\]
-   fixed bug where [unique.seqs](/wiki/unique.seqs) would double
    the length of the last sequence \[ps\]
-   fixed bug with read.dist for windows users
    \[sw\]
-   fixed help for [filter.seqs](/wiki/filter.seqs) and
    [align.seqs](/wiki/align.seqs)
-   fixed bug with deconvolute that double the length of last sequence
-   mothur now recognizes TRUE, true, T and t as true.
-   removed using namespace std from all files except mothur.h and
    defined arrays to comply with C++ standard to better support VS.
-   added <ctime> and defined math functions for windows user.
-   fixed memory access violation with
    read.dist.
-   fixed a minor bug in [tree.shared](/wiki/tree.shared) command.
-   [get.oturep](/wiki/get.oturep) can now process aligned
    sequences as well as unaligned sequences.

## Wiki updates

-   Reorganized the [mothur manual](/wiki/mothur_manual)
-   Changed page names for commands to be the name of the command (e.g.
    read.dists is at read.dist)
-   Created a commands [ category](/wiki/tags#commands)