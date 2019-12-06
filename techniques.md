# Experimental Techniques

#### Method

There have been several similar technologies developed recently to analyze the interactions between RNA and chromatin, including MARGI, ChAR-seq, and GRID-seq. The overarching method to identify such interactions is surprisingly similar between these technologies.

The general method is as follows:

![MARGI Overview](/Users/blakegabel/Documents/beng183/MARGI.jpg)
Graphical overview [3]

1. Crosslink the DNA to any nearby RNA, typically using formaldehyde
2. Ligate the RNA then the DNA to a synthesized linker
	* The linker needs to achieve three goals: one end must selectively bind to RNA and the other to DNA, have a means to identify which end bound to RNA or DNA, and a method for capture after fragmentation
3. RNA is reverse transcribed into cDNA, necessary for most sequencing techniques
4. DNA library is fragmented using either sonication or a digestive enzyme
5. Chimeric fragments are captured using the tag on the linker
6. Fragments are sequenced and appropriately mapped to either the genome or transcriptome

Each method has its own unique pipeline for data analysis and an example of processed ChAR-seq that maps the relative position of transcribed RNA to its genomic location post-transcription

![ChAR-seq](/Users/blakegabel/Documents/beng183/charseq.jpg)
*A.* All mapped RNA (y-axis) to genome location (x-axis) *B.* mRNA *C.* snRNA *D.* Cumulative frequency of length-normalized contacts for 16,812 RNAs identified on the ‘RNA-side’ of chimeric reads. *E.* Scatter plot of length normalized chromatin-contacts versus total expression for each RNA.  
[5]

#### Comparisons to GRID-seq
After developing their new technology, GRID-seq, to identify RNA-chromatin interactions, Zhou and his colleagues compared it to the other two recently developed technologies, MARGI and ChAR-seq.

One disadvantage of MARGI is that it employs a circularization step after reverse transcription and then the linker is cleaved to allow identification of RNA or DNA end. This circularization is not specific to the chimeric cDNA-gDNA fragment of interest, allowing for potential gDNA-gDNA fragments to be captured and sequenced. To avoid this error, the GRID-seq analysis pipeline ensures that all RNA reads only map somewhere to the transcribed genic regions [4].

Both GRID-seq and ChAR-seq attempted to normalize for nonspecific RNA interactions, either from free floating RNA or RNA that associated during library prep. The authors of ChAR-seq added excess free floating RNA to determine the false positive rate, which they calculate to be approximately 0.5% [5]. The authors of GRID-seq compared experimentally and computationally derived backgrounds with a mixture of human and Drosophila cells to assess cross-species interactions during library construction. After normalizing the two methods for counts, they concluded that nonspecific contacts overwhelmed specific contacts by genuine trans-acting RNAs [4]. GRID-seq uses a digestive enzyme for size selection, cutting 19-23 bp from the linker on either side. Due to the small size of the reads, efficient mapping becomes more difficult, increasing the rate of false mapping compared to longer reads (20-100 bp) [5].
