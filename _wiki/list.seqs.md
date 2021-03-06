---
title: 'list.seqs'
tags: 'commands'
redirect_from: '/wiki/List.seqs.html'
---
The **list.seqs** command will write out the names
of the sequences found within a [ fastq](/wiki/fastq_file), [
fasta](/wiki/fasta_file), [ name](/wiki/name_file), [
group](/wiki/group_file), [ count](/wiki/Count_File), [
list](/wiki/list_file), or [
align.report](/wiki/align.report_file) file. This could be useful
for using the [get.seqs](/wiki/get.seqs) and
[remove.seqs](/wiki/remove.seqs) commands as well as to generate a
[group file](/wiki/group_file). To complete this analysis, you need
to download the folder compressed in the [
Esophagus.zip](https://mothur.s3.us-east-2.amazonaws.com/wiki/esophagus.zip) archive.


## Options

At least one of the following options must be used. Each of these
options will generate a file ending in accnos that contains a single
column containing the list of the sequences contained in the input file.

### fastq option

The fastq option is used as presented in the following command:

    mothur > list.seqs(fastq=test.fastq)

### fasta option

The fasta option is used as presented in the following command:

    mothur > list.seqs(fasta=esophagus.fasta)

The resulting esophagus.accnos file looks something like:

    59_10_1
    59_10_10
    59_10_11
    59_10_13
    59_10_15
    59_10_16
    59_10_17
    ...

### name option

The name option is used as presented in the following command (be sure
to run [unique.seqs](/wiki/unique.seqs) on esophagus.fasta first):

    mothur > list.seqs(name=esophagus.names)

### count option

The [ count](/wiki/Count_File) file is similar to the name file in
that it is used to represent the number of duplicate sequences for a
given representative sequence. It can also contain group information.

    mothur > list.seqs(count=esophagus.count_table)

### group option

The group option is used as presented in the following command:

    mothur > list.seqs(group=esophagus.groups)

### alignreport option

The alignreport option is used as presented in the following command:

    mothur > list.seqs(alignreport=esophagus.align.report)

### list option

The list option is used as presented in the following command:

    mothur > list.seqs(list=esophagus.fn.list)

### taxonomy option

The taxonomy option is used as presented in the following command:

    mothur > list.seqs(taxonomy=esophagus.silva.full.taxonomy)

## Revisions

-   1.28.0 Added count option
-   1.33.0 Added fastq option
-   1.40.0 - Allow for () characters in taxonomy definitions.
    [\#350](https://github.com/mothur/mothur/issues/350)


