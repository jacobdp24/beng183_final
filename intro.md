# RNA-Chromatin Interactions 

###### BENG183 Final Paper date:12-9-19
###### Group 17 Aditya Sampath, Blake Gabel, Jacob Doering-Powell

1. [Introduction](#1)
2. [History](#2)
3. [The Goal of CHIP-Sequencing](#3)
4. [Understanding functional features of the genome](#4)<br>
    4.1. [Nucleosome](#41)<br>
    4.2. [Transcription Factors and TF binding sites](#42)<br>
    4.3. [Histone Modification](#43)<br>
    4.4. [Insulator](#44)
5. [Overivew of Chip-Squencing](#5)<br>
    5.1. [The workflow of CHIP-Sequencing](#51)<br>
    5.2. [Experimental Design](#52)
6. [Data Analysis](#6)<br>
    6.1. [FastQ File Format](#61)<br>
    6.2. [Downstream Analysis](#62)
7. [Advantages of Chip-Sequencing](#7)
8. [Applications](#8)



## 1. Introduction<a name="1"></a>

RNA exists in the cell not only as an intermediary between DNA and the final protein product, but also as non-coding RNAs (ncRNAs) which fulfill biological purposes beyond just DNA transcription. Among these purposes is RNA’s role in RNA-genome interactions, where RNA exists as part of the epigenome [1]. As part of the epigenome, RNA takes part in actions such as gene activation and silencing, on both a local level (via RNA-protein interactions and local DNA interactions), and a global level (where the RNA can modify gene expression levels). These interactions occur both proximally and directly, depending on the distance that the RNA and DNA have between themselves. As a result of the variety of different interactions that RNA and DNA can have, new technologies have emerged to map out connections to the genome. These technologies include MARGI (mapping RNA-genome interactions) and CHAR-seq. Each sequencing technology allows for different information to be learned regarding RNA-genome interactions [1].