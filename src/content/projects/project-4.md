---
title: 'Structural Variants in Bottlenose Dolphins'
description: 'Identifying polymorphisms across three bottlenose dolphin populations using bioinformatics'
image:
    url: '/dolph.jpg'
    alt: 'GitHub wallpaper'
worksImage1:
    url: '/image-1.webp'
    alt: 'first image of your project.'
worksImage2:
    url: '/image-2.webp'
    alt: 'second image of your project.'
keywords: structural variants, bottlenose dolphin, population genomics, bioinformatics, Manta, indels
advisor: Dr. Tom Schultz, Duke University Marine Lab
website: https://docs.google.com/document/d/1gdn5Yc0ZhydVWrD6fmrrjQN6Qd2-Hh-y56K5saBRDco/edit?usp=sharing
---

<div></div>
<div></div>

### Project Overview

This was my summer 2023 project as a Bonaventura Fellow at the Duke Marine Lab. 

From a high level, studying the underlying genetic mechanisms of speciation and population-level differentiations can provide a window into the past context or future possibility of speciation events.

A new avenue for studying variation beyond single-nucleotide polymorphisms (SNPs) comes in the form of stuctural variants (SVs). SVs are generally defined as large chromosomal-level alterations larger than 50 base pairs in size, comprising deletions, duplications, insertions, inversions, and translocations. At the time of writing, a little over two dozen examples of speciation tied to SVs were present in the literature. 

<div class="center">
    <img class="pro-img" width="500px" src="/sv.png" alt="first image of your project." />
</div>  
<h4>Examples of structural variants. Image from van Belzen et al., 2021. <i>Nature</i></h4>

Our study organism for detection and analysis of structural variants was the bottlenose dolphin. In the western North Atlantic, three ecotypes of common bottlenose dolphins are present - referred to as inshore, offshore, and coastal. The offshore and coastal ecotypes are separated by the continental shelf and have developed distinct phenotypic traits. From my independent study paper, linked above: "while previous research using whole genome data of western North Atlantic bottlenose dolphins focused on SNP calling, our study attempts to use compiled short-reads to call SVs and instead provide a foundation for understanding whether SVs play a part in the differentiation and potential speciation between these two distinct ecotypes in addition to the third discrete inshore ecotype."

<div class="center">
    <img class="pro-img" width="500px" src="/dapc.png" alt="first image of your project." />
</div>  
<h4>Past work in bottlenose dolphins (see DAPC and STRUCTURE plot here) using SNPs has revealed three genetically distinct ecotypes. Red = inshore, green = offshore, blue = coastal. </h4>
<div></div>

### Project Results

Variant calling was done using Manta software (see Chen et al. 2016 for more information about Manta, link is in the Google Doc at the top of this page) on binary-aligned reads in **.bam** format. For this project, I had sequences for 12 individuals with 4 from each ecotype present. Resulting variant calls in **.vcf** format were filtered to remove low-quality variants, and then plotted using matplotlib. Prior to filtering, Manta discovered over 32,000 variants with this number being reduced to 15,520 after filtration. 

Also from my independent study paper: on average, coastal samples contained the least number of variants and insertions and deletions (indels) at 2173 and 900, respectively. Inshore samples averaged slightly more, at 2232 and 920 variants and indels. Offshore samples, however, contained substantially more variants, averaging over twice as many at 5962 variants, of which 2520 were indels. 

<div class="center">
    <img class="pro-img" width="500px" src="/variants.png" alt="first image of your project." />
    <h4>Graph showing # of variants by individual.
</h4>
</div>  

After initial analysis of called variants, I ran PCA and DAPC to cluster the samples, and just like the a priori ecotype designation which was done with the SNPs, we ended up with 4 samples in each of the 3 clusters (inshore, offshore, coastal). This was mostly where I wrapped up analysis over the summer, although I did go hunting through the **.vcfs** to both get summary statistics about variant sizes and types for a particular individual (not shown here) and to find a few variants of interest for my class lab project.

<div class="center">
    <img class="pro-img" width="500px" src="/dapc2.png" alt="first image of your project." />
    <h4>DAPC: Coastal individuals mapped to cluster 1, offshore to cluster 2, and inshore to cluster 3. (A) Assignment plot showing DAPC assignments. (B) Individual membership probabilities in table form. All individuals mapped perfectly into one cluster. Sorry, not the best figure.
</h4>
</div>  

<div></div>

### Lab Work from 2024 Spring

I took Tom (my advisor)'s course on marine mammal genomics in spring 2024 and did my lab project on genotyping individuals using some 50-100 base pair variants that I called last summer. For more information about this, see my IS paper. 

<div></div>

### Future Work

While I'm no longer working on this project, identifying functional polymorphic SVs that could be responsible for ongoing differentiation between dolphin populations is a compelling area of research. 
