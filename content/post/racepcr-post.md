+++
title = "RacePCR- R package for designing primers for Race PCR"

date = 2018-03-20T00:00:00
lastmod = 2018-05-13T00:00:00
draft = false

tags = ["R","PCR"]
summary = "This package can be used to design gene specific primers (GSP) for Race PCR."

[header]
image = "headers/pcr.JPG"
caption = " "

[[gallery_item]]
album = "1"
image = ""
caption = ""
+++


## Description
You can use this package to design 3' and 5'primers for Race PCR. The design is based on the method described by Clonetech Race PCR manual. The resulting primers will have vector sequence automatically added to them. Source code is available on my [Github page](https://github.com/lrjoshi/RacepcR).

## Installation
>library(devtools)

>install_github("lrjoshi/RacepcR")

## Usage
>getDNA(dnaseq) #enter DNA Sequence and check length

>quality (dnaseq) #to see if your sequence contains character other than AGTC.

>gcbarplot(dnaseq) #gives barplot of nucleotide content

>get5prime(dnaseq,x) #gives you 5' primer

>get3prime(dnaseq,y) #gives you 3' primer

## Arguments
>dnaseq	: it is the sequence of your DNA. For eg : "aaggcctt"

>x	:position where you want to start your 5' primer

>y	:position where you want to start your 3' primer

## Note
This package depends on Biostrings package. So, you should have already installed Biostrings package from Bioconductor.

## Examples
>library (RacepcR)

>library(Biostrings)

>getDNA("aaggccttcc")

>quality ("aaggcct")

>gcbarplot("aaaaagccggt")

>get5prime("aaaggcggcggcttcggcgcgctcgtgctgctgctgcggcgctcctttcgctcgtcgctgctttctctcgct",30)

>get3prime("aaaggcggccccctcttcggccttcgctgctgctgcggcgcggctcgcgctgctgctttgctgctcgggctcgt",10)