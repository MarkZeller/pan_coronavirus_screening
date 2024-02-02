This repository describes the development of a pan-coronavirus qPCR. It's based on all available coronaviridae reference sequences in GenBank. pan_CoV_F2 should in theory work on all, while pan_CoV_F1 has a few mismatches in some of the animal CoVs. pan_CoV_F2 is newly designed, so not sure if it works yet.

Primer and gBlock sequences[^1]:
```
>pan_CoV_F1
ACWCARHTVAAYYTNAARTAYGC
>pan_CoV_F2
AARTTYTAYGGHGGNTGGVA
>pan_CoV_R
TCRCAYTTNGGRTARTCCCA
>pan_CoV_gBlock
ccctactataactcaaatgaatcttaagtatgccattagtgcaaagaatagagctcgcaccgtagctggtgtctctatctgtagtactatgaccaatagacagtttcatcaaaaattattgaaatcaatagccgccactagaggagctactgtagtaattggaacaagcaaattctatggtggttggcacaacatgttaaaaactgtttatagtgatgtagaaaaccctcaccttatgggttgggattatcctaaatgtgatagagccatg
```

Primer and amplicon characteristics:
```
Tm F1: 53.5 ºC	59.9 ºC	66.6 ºC
Tm F2: 55.5 ºC	62 ºC	68.5 ºC
Tm R: 56.3 ºC	62.1 ºC	67.3 ºC

length F1 - R: 251
length F2 - R: 92
```

Reaction setup:
| Component				|Volumes for 20ul reaction|
|:--------------------------------------|-----------------------:|
| One-Step SYBR Green Master Mix[^2]	|		 10 	 |
| pan_CoV_F1 or pan_CoV_F2		|		  1	 |
| pan_CoV_R				|		  1	 |
| Nuclease-free water			|		5.2 	 |
| RNA template or pan_CoV_gBlock	|		  2	 |
| qScript One-Step RT[^2]		|		0.8	 |


qPCR conditions:
| Step                             	| Cycle conditions	|
|:--------------------------------------|----------------------:|
| cDNA synthesis		        |   50ºC, 10 min		|
| Taq activation	                |   95ºC, 5min   	|
| PCR cycling (40 cycles)               |   95ºC, 10s      	|
| 			                |   60ºC, 30s[^3]	|

Add positive samples on a 2% agarose gel along with the positive control to check if the amplicon has the expected size.

[^1]: dilute gBlock to ~100 copies; can be used as a positive control for both F1 - R and F2 - R assays
[^2]: part of the qScript One-Step SYBR Green RT-qPCR kit
[^3]: data collection on the SYBR green channel

