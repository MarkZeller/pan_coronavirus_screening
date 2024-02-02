This repository describes the development of a pan-coronavirus qPCR. It's based on all available coronaviridae reference sequences in GenBank.  

Primer and gBlock sequences
'''
/>pan_CoV_F1\n
ACWCARHTVAAYYTNAARTAYGC\n
/>pan_CoV_F2\n
AARTTYTAYGGHGGNTGGVA\n
/>pan_CoV_R\n
TCRCAYTTNGGRTARTCCCA\n
/>pan_CoV_gBlock\n
ccctactataactcaaatgaatcttaagtatgccattagtgcaaagaatagagctcgcaccgtagctggtgtctctatctgtagtactatgaccaatagacagtttcatcaaaaattattgaaatcaatagccgccactagaggagctactgtagtaattggaacaagcaaattctatggtggttggcacaacatgttaaaaactgtttatagtgatgtagaaaaccctcaccttatgggttgggattatcctaaatgtgatagagccatg
'''

Primer and amplicon characteristics:
'''
Tm F1: 53.5 ºC	59.9 ºC	66.6 ºC
Tm F2: 55.5 ºC	62 ºC	68.5 ºC
Tm R: 56.3 ºC	62.1 ºC	67.3 ºC

length F1 - R: 251
length F2 - R: 92
'''

Protocol in a nutshell:
| Component				|Volume for 20ul reaction|
|:--------------------------------------|-----------------------:|
| One-Step SYBR Green Master Mix[^1]	|		 10 	 |
| pan_CoV_F1 or pan_CoV_F2		|		  1	 |
| pan_CoV_R				|		  1	 |
| Nuclease-free water			|		5.2 	 |
| RNA template or pan_CoV_gBlock	|		  2	 |
| qScript One-Step RT[^1]		|		0.8	 |
[^1]: part of the qScript One-Step SYBR Green RT-qPCR kit

qPCR cycling conditions:
| Step                             	| Cycle conditions	|
|:--------------------------------------|----------------------:|
| cDNA synthesis		        |   50ºC, 10 min		|
| Taq activation	                |   95ºC, 5min   	|
| PCR cycling (40 cycles)               |   95ºC, 10s      	|
| 			                |   60ºC, 30S[^2]	|
[^2]data collection on the SYBR green channel

