Exosome Microarray Analysis: No Donor A, Langerhans cells only
================
Claire Levy
January 18, 2017

Experiment overview
-------------------

Experiments were done on two cells types: Langerhans cells and vaginal epithelial cells.

Langerhans cells from 3 donors were exposed to HIV, Sendai virus or no virus and each of those were exposed to the following:

-   Exosomes
-   Seminal supernatant
-   Liposomes
-   Media control

The following analysis is only for Langerhans cells and only for Donors B and C
-------------------------------------------------------------------------------

    ## Inputting the data ...
    ## Perform Quality Control assessment of the LumiBatch object ...

Plots of non-normalized data

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/density-1.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non-norm-1.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20MSD%20plot-1.png)![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20MSD%20plot-2.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20boxplot-1.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20density-1.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-1.png)![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-2.png)![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-3.png)

![](no_Donor_A_Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/normed%20boxplot-1.png)

Non-specific filtering
----------------------

Limma suggests to keep probes that are expressed above background on at least n arrays where n is smallest number of replicates assigned to any of the treatment combinations.

We have 3 donors x 3 viruses x 4 Treatments so I will keep probes with detection levels above background in at least 3 samples.

Number of probes in data set before filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   47323     47323 47323    47323
    ## Samples       24        24    24       24

Number of probes in data set after filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   20991     20991 20991    20991
    ## Samples       24        24    24       24

### Number of DE probes for each contrast:

<table style="width:51%;">
<colgroup>
<col width="36%" />
<col width="9%" />
<col width="5%" />
</colgroup>
<thead>
<tr class="header">
<th align="center">variable</th>
<th align="center">down</th>
<th align="center">up</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center">None.MediaVsNone.Exos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="even">
<td align="center">None.MediaVsNone.Lipo</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="odd">
<td align="center">None.MediaVsNone.Sup</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="even">
<td align="center">Sendai.MediaVsSendai.Exos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="odd">
<td align="center">Sendai.MediaVsSendai.Lipo</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="even">
<td align="center">Sendai.MediaVsSendai.Sup</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="odd">
<td align="center">HIV.MediaVsHIV.Exos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="even">
<td align="center">HIV.MediaVsHIV.Lipo</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="odd">
<td align="center">HIV.MediaVsHIV.Sup</td>
<td align="center">9</td>
<td align="center">10</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Sup DE genes

<table style="width:93%;">
<colgroup>
<col width="19%" />
<col width="15%" />
<col width="43%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">TargetID</th>
<th align="center">DEFINITION</th>
<th align="center">adj.P.Val</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>3940435</strong></td>
<td align="center">EMP1</td>
<td align="center">Homo sapiens epithelial membrane protein 1 (EMP1), mRNA.</td>
<td align="center">0.0005172</td>
</tr>
<tr class="even">
<td align="center"><strong>6370678</strong></td>
<td align="center">ROD1</td>
<td align="center">Homo sapiens ROD1 regulator of differentiation 1 (S. pombe) (ROD1), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>3990561</strong></td>
<td align="center">LY6H</td>
<td align="center">Homo sapiens lymphocyte antigen 6 complex, locus H (LY6H), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="even">
<td align="center"><strong>1570553</strong></td>
<td align="center">IL8</td>
<td align="center">Homo sapiens interleukin 8 (IL8), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>1410653</strong></td>
<td align="center">TERF2IP</td>
<td align="center">Homo sapiens telomeric repeat binding factor 2, interacting protein (TERF2IP), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="even">
<td align="center"><strong>670202</strong></td>
<td align="center">SESTD1</td>
<td align="center">Homo sapiens SEC14 and spectrin domains 1 (SESTD1), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>1980309</strong></td>
<td align="center">IL8</td>
<td align="center">Homo sapiens interleukin 8 (IL8), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="even">
<td align="center"><strong>460164</strong></td>
<td align="center">FTHL11</td>
<td align="center">Homo sapiens ferritin, heavy polypeptide-like 11 (FTHL11) on chromosome 8.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>5360672</strong></td>
<td align="center">CCNG2</td>
<td align="center">Homo sapiens cyclin G2 (CCNG2), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="even">
<td align="center"><strong>2260309</strong></td>
<td align="center">RPPH1</td>
<td align="center">Homo sapiens ribonuclease P RNA component H1 (RPPH1), RNase P RNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>6580639</strong></td>
<td align="center">ACOT7</td>
<td align="center">Homo sapiens acyl-CoA thioesterase 7 (ACOT7), transcript variant hBACHa, mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="even">
<td align="center"><strong>6180706</strong></td>
<td align="center">LY6H</td>
<td align="center">Homo sapiens lymphocyte antigen 6 complex, locus H (LY6H), mRNA.</td>
<td align="center">0.03765</td>
</tr>
<tr class="odd">
<td align="center"><strong>3130092</strong></td>
<td align="center">ATP1B3</td>
<td align="center">Homo sapiens ATPase, Na+/K+ transporting, beta 3 polypeptide (ATP1B3), mRNA. XM_945518</td>
<td align="center">0.03919</td>
</tr>
<tr class="even">
<td align="center"><strong>610201</strong></td>
<td align="center">HES6</td>
<td align="center">Homo sapiens hairy and enhancer of split 6 (Drosophila) (HES6), mRNA.</td>
<td align="center">0.03919</td>
</tr>
<tr class="odd">
<td align="center"><strong>7650528</strong></td>
<td align="center">LOC650518</td>
<td align="center">PREDICTED: Homo sapiens similar to Proteasome subunit alpha type 6 (Proteasome iota chain) (Macropain iota chain) (Multicatalytic endopeptidase complex iota chain) (LOC650518), mRNA.</td>
<td align="center">0.03919</td>
</tr>
<tr class="even">
<td align="center"><strong>1660669</strong></td>
<td align="center">FTHL16</td>
<td align="center">PREDICTED: Homo sapiens misc_RNA (FTHL16), miscRNA.</td>
<td align="center">0.03919</td>
</tr>
<tr class="odd">
<td align="center"><strong>3460296</strong></td>
<td align="center">HDGFRP3</td>
<td align="center">Homo sapiens hepatoma-derived growth factor, related protein 3 (HDGFRP3), mRNA.</td>
<td align="center">0.03919</td>
</tr>
<tr class="even">
<td align="center"><strong>6280332</strong></td>
<td align="center">CXCL16</td>
<td align="center">Homo sapiens chemokine (C-X-C motif) ligand 16 (CXCL16), mRNA.</td>
<td align="center">0.03919</td>
</tr>
<tr class="odd">
<td align="center"><strong>6200128</strong></td>
<td align="center">ROD1</td>
<td align="center">Homo sapiens ROD1 regulator of differentiation 1 (S. pombe) (ROD1), mRNA.</td>
<td align="center">0.03919</td>
</tr>
</tbody>
</table>

CAMERA testing
==============

Hallmark gene sets: top 6 results
---------------------------------

### None.Media Vs None.Exos

<table style="width:92%;">
<colgroup>
<col width="54%" />
<col width="12%" />
<col width="16%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">277</td>
<td align="center">Down</td>
<td align="center">0.1499</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">93</td>
<td align="center">Down</td>
<td align="center">0.1499</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ESTROGEN_RESPONSE_EARLY</strong></td>
<td align="center">173</td>
<td align="center">Down</td>
<td align="center">0.1981</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ANDROGEN_RESPONSE</strong></td>
<td align="center">115</td>
<td align="center">Down</td>
<td align="center">0.4741</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">201</td>
<td align="center">Up</td>
<td align="center">0.4741</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.4741</td>
</tr>
</tbody>
</table>

### None.Media Vs None.Lipo

<table style="width:94%;">
<colgroup>
<col width="56%" />
<col width="12%" />
<col width="16%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">265</td>
<td align="center">Up</td>
<td align="center">0.1876</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.1876</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">201</td>
<td align="center">Up</td>
<td align="center">0.1876</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">277</td>
<td align="center">Down</td>
<td align="center">0.1876</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">93</td>
<td align="center">Down</td>
<td align="center">0.2364</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TGF_BETA_SIGNALING</strong></td>
<td align="center">67</td>
<td align="center">Down</td>
<td align="center">0.3766</td>
</tr>
</tbody>
</table>

### None.Media Vs None.Sup

<table>
<colgroup>
<col width="62%" />
<col width="12%" />
<col width="16%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">69</td>
<td align="center">Up</td>
<td align="center">0.02169</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_G2M_CHECKPOINT</strong></td>
<td align="center">246</td>
<td align="center">Up</td>
<td align="center">0.1998</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_HEDGEHOG_SIGNALING</strong></td>
<td align="center">36</td>
<td align="center">Up</td>
<td align="center">0.4808</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">93</td>
<td align="center">Up</td>
<td align="center">0.4808</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_SPERMATOGENESIS</strong></td>
<td align="center">95</td>
<td align="center">Up</td>
<td align="center">0.5586</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ANGIOGENESIS</strong></td>
<td align="center">31</td>
<td align="center">Up</td>
<td align="center">0.5586</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Exo

<table>
<colgroup>
<col width="63%" />
<col width="12%" />
<col width="16%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.2659</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V2</strong></td>
<td align="center">77</td>
<td align="center">Up</td>
<td align="center">0.272</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_APOPTOSIS</strong></td>
<td align="center">200</td>
<td align="center">Down</td>
<td align="center">0.9009</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">69</td>
<td align="center">Up</td>
<td align="center">0.9009</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_BILE_ACID_METABOLISM</strong></td>
<td align="center">93</td>
<td align="center">Up</td>
<td align="center">0.9009</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">201</td>
<td align="center">Up</td>
<td align="center">0.9009</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Lipo

<table>
<colgroup>
<col width="63%" />
<col width="12%" />
<col width="16%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.9248</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">69</td>
<td align="center">Up</td>
<td align="center">0.9248</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">201</td>
<td align="center">Up</td>
<td align="center">0.9248</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_SPERMATOGENESIS</strong></td>
<td align="center">95</td>
<td align="center">Up</td>
<td align="center">0.9248</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_NOTCH_SIGNALING</strong></td>
<td align="center">34</td>
<td align="center">Up</td>
<td align="center">0.9248</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_XENOBIOTIC_METABOLISM</strong></td>
<td align="center">176</td>
<td align="center">Up</td>
<td align="center">0.9248</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Sup

<table style="width:96%;">
<colgroup>
<col width="54%" />
<col width="12%" />
<col width="16%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_E2F_TARGETS</strong></td>
<td align="center">262</td>
<td align="center">Up</td>
<td align="center">0.0007544</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_G2M_CHECKPOINT</strong></td>
<td align="center">246</td>
<td align="center">Up</td>
<td align="center">0.001357</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.001579</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">196</td>
<td align="center">Down</td>
<td align="center">0.02654</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ANGIOGENESIS</strong></td>
<td align="center">31</td>
<td align="center">Down</td>
<td align="center">0.04219</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_APOPTOSIS</strong></td>
<td align="center">200</td>
<td align="center">Down</td>
<td align="center">0.1132</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Exo

<table style="width:96%;">
<colgroup>
<col width="56%" />
<col width="12%" />
<col width="16%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.01849</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">127</td>
<td align="center">Down</td>
<td align="center">0.03502</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">277</td>
<td align="center">Down</td>
<td align="center">0.03989</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">196</td>
<td align="center">Down</td>
<td align="center">0.04668</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">265</td>
<td align="center">Up</td>
<td align="center">0.103</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_IL6_JAK_STAT3_SIGNALING</strong></td>
<td align="center">95</td>
<td align="center">Down</td>
<td align="center">0.103</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Lipo

<table style="width:94%;">
<colgroup>
<col width="56%" />
<col width="12%" />
<col width="16%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">248</td>
<td align="center">Down</td>
<td align="center">0.4151</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INTERFERON_ALPHA_RESPONSE</strong></td>
<td align="center">120</td>
<td align="center">Up</td>
<td align="center">0.4151</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">127</td>
<td align="center">Down</td>
<td align="center">0.4151</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_COMPLEMENT</strong></td>
<td align="center">211</td>
<td align="center">Down</td>
<td align="center">0.4151</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ANDROGEN_RESPONSE</strong></td>
<td align="center">115</td>
<td align="center">Down</td>
<td align="center">0.4151</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">277</td>
<td align="center">Down</td>
<td align="center">0.4151</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Sup

<table>
<colgroup>
<col width="61%" />
<col width="11%" />
<col width="15%" />
<col width="10%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">127</td>
<td align="center">Down</td>
<td align="center">0.001944</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">208</td>
<td align="center">Down</td>
<td align="center">0.0579</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">196</td>
<td align="center">Down</td>
<td align="center">0.1322</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">69</td>
<td align="center">Up</td>
<td align="center">0.1968</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL6_JAK_STAT3_SIGNALING</strong></td>
<td align="center">95</td>
<td align="center">Down</td>
<td align="center">0.1968</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INTERFERON_GAMMA_RESPONSE</strong></td>
<td align="center">251</td>
<td align="center">Down</td>
<td align="center">0.2765</td>
</tr>
</tbody>
</table>

GO biological process gene sets: top 6 results
----------------------------------------------

Sean wrote some code (<https://github.com/seaaan/Bioinformatics/tree/master/GOTermMappingsForCamera>) to extract just the Biological Process gene sets out of all the GO gene sets. I will use those to test against the LC data here.

### None.Media Vs None.Exos

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="74%" />
<col width="11%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_RESPIRATORY_CHAIN_COMPLEX_IV_ASSEMBLY</strong></td>
<td align="center">18</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_APPETITE</strong></td>
<td align="center">15</td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_TRNA_MODIFICATION</strong></td>
<td align="center">58</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CYTOCHROME_COMPLEX_ASSEMBLY</strong></td>
<td align="center">30</td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_ASSEMBLY</strong></td>
<td align="center">92</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NEGATIVE_REGULATION_OF_RESPONSE_TO_FOOD</strong></td>
<td align="center">11</td>
<td align="center">Up</td>
</tr>
</tbody>
</table>

<table style="width:90%;">
<colgroup>
<col width="80%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_RESPIRATORY_CHAIN_COMPLEX_IV_ASSEMBLY</strong></td>
<td align="center">0.06571</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_APPETITE</strong></td>
<td align="center">0.06571</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_TRNA_MODIFICATION</strong></td>
<td align="center">0.06571</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CYTOCHROME_COMPLEX_ASSEMBLY</strong></td>
<td align="center">0.06571</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_ASSEMBLY</strong></td>
<td align="center">0.06571</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NEGATIVE_REGULATION_OF_RESPONSE_TO_FOOD</strong></td>
<td align="center">0.06571</td>
</tr>
</tbody>
</table>

### None.Media Vs None.Lipo

<table style="width:97%;">
<caption>Table continues below</caption>
<colgroup>
<col width="86%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_ELECTRON_TRANSPORT_NADH_TO_UBIQUINONE</strong></td>
<td align="center">39</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_I_BIOGENESIS</strong></td>
<td align="center">66</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_I_ASSEMBLY</strong></td>
<td align="center">66</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NADH_DEHYDROGENASE_COMPLEX_ASSEMBLY</strong></td>
<td align="center">66</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PATHWAY_RESTRICTED_SMAD_PROTEIN_PHOSPHORYLATION</strong></td>
<td align="center">7</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHONDROCYTE_DEVELOPMENT</strong></td>
<td align="center">14</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="77%" />
<col width="15%" />
<col width="7%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_ELECTRON_TRANSPORT_NADH_TO_UBIQUINONE</strong></td>
<td align="center">Up</td>
<td align="center">0.2083</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_I_BIOGENESIS</strong></td>
<td align="center">Up</td>
<td align="center">0.2083</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_RESPIRATORY_CHAIN_COMPLEX_I_ASSEMBLY</strong></td>
<td align="center">Up</td>
<td align="center">0.2083</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NADH_DEHYDROGENASE_COMPLEX_ASSEMBLY</strong></td>
<td align="center">Up</td>
<td align="center">0.2083</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PATHWAY_RESTRICTED_SMAD_PROTEIN_PHOSPHORYLATION</strong></td>
<td align="center">Down</td>
<td align="center">0.2083</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHONDROCYTE_DEVELOPMENT</strong></td>
<td align="center">Down</td>
<td align="center">0.2083</td>
</tr>
</tbody>
</table>

### None.Media Vs None.Sup

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="90%" />
<col width="10%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">11</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">176</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_ESTABLISHMENT_OF_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">157</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">8</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">44</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_AZOLE_TRANSPORT</strong></td>
<td align="center">10</td>
</tr>
</tbody>
</table>

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="86%" />
<col width="13%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_ESTABLISHMENT_OF_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_AZOLE_TRANSPORT</strong></td>
<td align="center">Down</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="88%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">9.167e-06</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">0.04165</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_ESTABLISHMENT_OF_PROTEIN_LOCALIZATION_TO_ENDOPLASMIC_RETICULUM</strong></td>
<td align="center">0.04186</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">0.1615</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">0.2479</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_AZOLE_TRANSPORT</strong></td>
<td align="center">0.2479</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Exo

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="90%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_HEMATOPOIETIC_STEM_CELL_PROLIFERATION</strong></td>
<td align="center">9</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NUCLEAR_TRANSCRIBED_MRNA_CATABOLIC_PROCESS_NONSENSE_MEDIATED_DECAY</strong></td>
<td align="center">179</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PARENTAL_BEHAVIOR</strong></td>
<td align="center">10</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MATERNAL_BEHAVIOR</strong></td>
<td align="center">10</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RELAXATION_OF_CARDIAC_MUSCLE</strong></td>
<td align="center">14</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_RECEPTOR_ACTIVITY</strong></td>
<td align="center">43</td>
</tr>
</tbody>
</table>

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="87%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_HEMATOPOIETIC_STEM_CELL_PROLIFERATION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NUCLEAR_TRANSCRIBED_MRNA_CATABOLIC_PROCESS_NONSENSE_MEDIATED_DECAY</strong></td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PARENTAL_BEHAVIOR</strong></td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MATERNAL_BEHAVIOR</strong></td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RELAXATION_OF_CARDIAC_MUSCLE</strong></td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_RECEPTOR_ACTIVITY</strong></td>
<td align="center">Up</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="92%" />
<col width="7%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_HEMATOPOIETIC_STEM_CELL_PROLIFERATION</strong></td>
<td align="center">0.3193</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NUCLEAR_TRANSCRIBED_MRNA_CATABOLIC_PROCESS_NONSENSE_MEDIATED_DECAY</strong></td>
<td align="center">0.3193</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PARENTAL_BEHAVIOR</strong></td>
<td align="center">0.3193</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MATERNAL_BEHAVIOR</strong></td>
<td align="center">0.3193</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_RELAXATION_OF_CARDIAC_MUSCLE</strong></td>
<td align="center">0.5461</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_RECEPTOR_ACTIVITY</strong></td>
<td align="center">0.5644</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Lipo

<table style="width:100%;">
<caption>Table continues below</caption>
<colgroup>
<col width="74%" />
<col width="11%" />
<col width="13%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_RECEPTOR_RECYCLING</strong></td>
<td align="center">28</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MRNA_TRANSCRIPTION</strong></td>
<td align="center">27</td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_DIGESTIVE_SYSTEM_PROCESS</strong></td>
<td align="center">26</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_TRNA_METABOLIC_PROCESS</strong></td>
<td align="center">178</td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MUSCLE_ATROPHY</strong></td>
<td align="center">11</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_ANDROGEN_RECEPTOR_SIGNALING_PATHWAY</strong></td>
<td align="center">28</td>
<td align="center">Up</td>
</tr>
</tbody>
</table>

<table style="width:90%;">
<colgroup>
<col width="81%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_RECEPTOR_RECYCLING</strong></td>
<td align="center">0.9975</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MRNA_TRANSCRIPTION</strong></td>
<td align="center">0.9975</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_DIGESTIVE_SYSTEM_PROCESS</strong></td>
<td align="center">0.9975</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_TRNA_METABOLIC_PROCESS</strong></td>
<td align="center">0.9975</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MUSCLE_ATROPHY</strong></td>
<td align="center">0.9975</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_ANDROGEN_RECEPTOR_SIGNALING_PATHWAY</strong></td>
<td align="center">0.9975</td>
</tr>
</tbody>
</table>

### Sendai.Media Vs Sendai.Sup

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="91%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">11</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHROMATIN_ASSEMBLY_OR_DISASSEMBLY</strong></td>
<td align="center">143</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_GLUCOSE_CATABOLIC_PROCESS</strong></td>
<td align="center">40</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_DNA_PACKAGING</strong></td>
<td align="center">154</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_CELLULAR_RESPONSE_TO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_STIMULUS</strong></td>
<td align="center">10</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CENTROMERE_COMPLEX_ASSEMBLY</strong></td>
<td align="center">42</td>
</tr>
</tbody>
</table>

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="88%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHROMATIN_ASSEMBLY_OR_DISASSEMBLY</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_GLUCOSE_CATABOLIC_PROCESS</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_DNA_PACKAGING</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_CELLULAR_RESPONSE_TO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_STIMULUS</strong></td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CENTROMERE_COMPLEX_ASSEMBLY</strong></td>
<td align="center">Up</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="90%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">0.0006411</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHROMATIN_ASSEMBLY_OR_DISASSEMBLY</strong></td>
<td align="center">0.03166</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_GLUCOSE_CATABOLIC_PROCESS</strong></td>
<td align="center">0.03166</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_DNA_PACKAGING</strong></td>
<td align="center">0.03166</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_CELLULAR_RESPONSE_TO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_STIMULUS</strong></td>
<td align="center">0.03893</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CENTROMERE_COMPLEX_ASSEMBLY</strong></td>
<td align="center">0.04996</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Exo

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="89%" />
<col width="10%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_ELECTRON_TRANSPORT_UBIQUINOL_TO_CYTOCHROME_C</strong></td>
<td align="center">17</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">59</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">87</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">99</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_SPINDLE_ASSEMBLY</strong></td>
<td align="center">68</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MITOTIC_SPINDLE_ASSEMBLY</strong></td>
<td align="center">37</td>
</tr>
</tbody>
</table>

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="86%" />
<col width="13%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_ELECTRON_TRANSPORT_UBIQUINOL_TO_CYTOCHROME_C</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_SPINDLE_ASSEMBLY</strong></td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MITOTIC_SPINDLE_ASSEMBLY</strong></td>
<td align="center">Down</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="89%" />
<col width="10%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_MITOCHONDRIAL_ELECTRON_TRANSPORT_UBIQUINOL_TO_CYTOCHROME_C</strong></td>
<td align="center">0.007938</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">0.007938</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">0.007938</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_INTERLEUKIN_6_PRODUCTION</strong></td>
<td align="center">0.02142</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_SPINDLE_ASSEMBLY</strong></td>
<td align="center">0.04277</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_MITOTIC_SPINDLE_ASSEMBLY</strong></td>
<td align="center">0.05276</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Lipo

<table>
<colgroup>
<col width="65%" />
<col width="11%" />
<col width="15%" />
<col width="7%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_GAMMA_AMINOBUTYRIC_ACID_SIGNALING_PATHWAY</strong></td>
<td align="center">11</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PLASMA_MEMBRANE_FUSION</strong></td>
<td align="center">25</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_VENTRICULAR_SEPTUM_MORPHOGENESIS</strong></td>
<td align="center">22</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_STEROL_BIOSYNTHETIC_PROCESS</strong></td>
<td align="center">52</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_ENDOCARDIAL_CUSHION_FORMATION</strong></td>
<td align="center">10</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_DENDRITE_MORPHOGENESIS</strong></td>
<td align="center">40</td>
<td align="center">Down</td>
<td align="center">0.9687</td>
</tr>
</tbody>
</table>

### HIV.Media Vs HIV.Sup

<table style="width:97%;">
<caption>Table continues below</caption>
<colgroup>
<col width="86%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">8</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">13</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">11</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_SIGNALING_PATHWAY</strong></td>
<td align="center">13</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_ENDOTHELIAL_CELL_CHEMOTAXIS</strong></td>
<td align="center">7</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_ENERGY_HOMEOSTASIS</strong></td>
<td align="center">17</td>
</tr>
</tbody>
</table>

<table>
<caption>Table continues below</caption>
<colgroup>
<col width="84%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">Direction</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_SIGNALING_PATHWAY</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_ENDOTHELIAL_CELL_CHEMOTAXIS</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_ENERGY_HOMEOSTASIS</strong></td>
<td align="center">Down</td>
</tr>
</tbody>
</table>

<table style="width:99%;">
<colgroup>
<col width="86%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>GO_INDUCTION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">5.029e-06</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_POSITIVE_CHEMOTAXIS</strong></td>
<td align="center">0.0006786</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">0.002693</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_VASCULAR_ENDOTHELIAL_GROWTH_FACTOR_SIGNALING_PATHWAY</strong></td>
<td align="center">0.009709</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_ENDOTHELIAL_CELL_CHEMOTAXIS</strong></td>
<td align="center">0.076</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_ENERGY_HOMEOSTASIS</strong></td>
<td align="center">0.1178</td>
</tr>
</tbody>
</table>
