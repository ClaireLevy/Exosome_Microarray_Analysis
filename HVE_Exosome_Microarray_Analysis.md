Exosome Microarray Analysis: HVE cells only
================
Claire Levy
January 13, 2017

Experiment overview
-------------------

Experiments were done on two cells types: Langerhans cells and vaginal epithelial cells.

HVE cells were exposed to the following:

-   High concentration of exosomes ("HighExosomes")
-   Low concentration of exosomes ("LowExosomes")
-   Seminal supernatant
-   Media control

The following analysis is only for HVE cells
--------------------------------------------

    ## Inputting the data ...
    ## Perform Quality Control assessment of the LumiBatch object ...

Plots of non-normalized data: HVE\_A2 appears as the main outlier, it is donor A with low exosomes. ![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/density%20plot%20of%20nonnorm%20data-1.png)

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/sample%20relations%20plot-1.png)

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/plot%20nonnorm%20dims-1.png)

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/boxplot-1.png)

Plots of quantile normalized data

    ## Perform quantile normalization ...

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/quantile%20normalization%20and%20plots-1.png)

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/normalized%20MDS-1.png)![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/normalized%20MDS-2.png)

![](HVE_Exosome_Microarray_Analysis_files/figure-markdown_github/quantile%20norm%20boxplot-1.png)

### Non-specific filtering

Limma suggests to keep probes that are expressed above background on at least n arrays where n is smallest number of replicates assigned to any of the treatment combinations.

We have 3 donors x 4 Treatments so I will keep probes with detection levels above background in at least 3 samples.

Number of probes in data set before filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   47323     47323 47323    47323
    ## Samples       12        12    12       12

Numbers of probes in data set after filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   20619     20619 20619    20619
    ## Samples       12        12    12       12

### Number of DE probes for each contrast:

<table style="width:40%;">
<colgroup>
<col width="25%" />
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
<td align="center">MediaVsLowExos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="even">
<td align="center">MediaVsHighExos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
<tr class="odd">
<td align="center">MediaVsSup</td>
<td align="center">0</td>
<td align="center">13</td>
</tr>
<tr class="even">
<td align="center">LowExosVsHighExos</td>
<td align="center">0</td>
<td align="center">0</td>
</tr>
</tbody>
</table>

### Media Vs Sup DE genes

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
<td align="center"><strong>5360347</strong></td>
<td align="center">NQO1</td>
<td align="center">Homo sapiens NAD(P)H dehydrogenase, quinone 1 (NQO1), transcript variant 1, mRNA.</td>
<td align="center">1.017e-05</td>
</tr>
<tr class="even">
<td align="center"><strong>2650730</strong></td>
<td align="center">STC1</td>
<td align="center">Homo sapiens stanniocalcin 1 (STC1), mRNA.</td>
<td align="center">0.001621</td>
</tr>
<tr class="odd">
<td align="center"><strong>5220240</strong></td>
<td align="center">FTH1</td>
<td align="center">Homo sapiens ferritin, heavy polypeptide 1 (FTH1), mRNA.</td>
<td align="center">0.001621</td>
</tr>
<tr class="even">
<td align="center"><strong>730286</strong></td>
<td align="center">TXNRD1</td>
<td align="center">Homo sapiens thioredoxin reductase 1 (TXNRD1), transcript variant 5, mRNA.</td>
<td align="center">0.001621</td>
</tr>
<tr class="odd">
<td align="center"><strong>270615</strong></td>
<td align="center">ABCC3</td>
<td align="center">Homo sapiens ATP-binding cassette, sub-family C (CFTR/MRP), member 3 (ABCC3), mRNA.</td>
<td align="center">0.002305</td>
</tr>
<tr class="even">
<td align="center"><strong>3850204</strong></td>
<td align="center">FTHL16</td>
<td align="center">PREDICTED: Homo sapiens misc_RNA (FTHL16), miscRNA.</td>
<td align="center">0.005116</td>
</tr>
<tr class="odd">
<td align="center"><strong>2970431</strong></td>
<td align="center">FTHL7</td>
<td align="center">Homo sapiens ferritin, heavy polypeptide-like 7 (FTHL7) on chromosome 13.</td>
<td align="center">0.0108</td>
</tr>
<tr class="even">
<td align="center"><strong>5810328</strong></td>
<td align="center">FTL</td>
<td align="center">Homo sapiens ferritin, light polypeptide (FTL), mRNA.</td>
<td align="center">0.01233</td>
</tr>
<tr class="odd">
<td align="center"><strong>5090278</strong></td>
<td align="center">GPX2</td>
<td align="center">Homo sapiens glutathione peroxidase 2 (gastrointestinal) (GPX2), mRNA.</td>
<td align="center">0.01862</td>
</tr>
<tr class="even">
<td align="center"><strong>4200450</strong></td>
<td align="center">G6PD</td>
<td align="center">Homo sapiens glucose-6-phosphate dehydrogenase (G6PD), transcript variant 1, mRNA.</td>
<td align="center">0.02224</td>
</tr>
<tr class="odd">
<td align="center"><strong>1990577</strong></td>
<td align="center">GCLM</td>
<td align="center">Homo sapiens glutamate-cysteine ligase, modifier subunit (GCLM), mRNA.</td>
<td align="center">0.0233</td>
</tr>
<tr class="even">
<td align="center"><strong>7210632</strong></td>
<td align="center">AKR1C3</td>
<td align="center">Homo sapiens aldo-keto reductase family 1, member C3 (3-alpha hydroxysteroid dehydrogenase, type II) (AKR1C3), mRNA.</td>
<td align="center">0.0348</td>
</tr>
<tr class="odd">
<td align="center"><strong>3190133</strong></td>
<td align="center">FTHL12</td>
<td align="center">Homo sapiens ferritin, heavy polypeptide-like 12 (FTHL12) on chromosome 9.</td>
<td align="center">0.03753</td>
</tr>
</tbody>
</table>

CAMERA testing
==============

Hallmark gene sets: top 6 results
---------------------------------

### Media Vs Low Exos

<table>
<colgroup>
<col width="64%" />
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
<td align="center"><strong>HALLMARK_ANDROGEN_RESPONSE</strong></td>
<td align="center">120</td>
<td align="center">Down</td>
<td align="center">0.6428</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ESTROGEN_RESPONSE_LATE</strong></td>
<td align="center">213</td>
<td align="center">Down</td>
<td align="center">0.6428</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_EPITHELIAL_MESENCHYMAL_TRANSITION</strong></td>
<td align="center">196</td>
<td align="center">Up</td>
<td align="center">0.6428</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">291</td>
<td align="center">Down</td>
<td align="center">0.6428</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_SPERMATOGENESIS</strong></td>
<td align="center">103</td>
<td align="center">Down</td>
<td align="center">0.6428</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">93</td>
<td align="center">Down</td>
<td align="center">0.6428</td>
</tr>
</tbody>
</table>

### Media Vs High Exos

See: doi: 10.1042/BCJ20160006

<table>
<colgroup>
<col width="62%" />
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
<td align="center"><strong>HALLMARK_EPITHELIAL_MESENCHYMAL_TRANSITION</strong></td>
<td align="center">196</td>
<td align="center">Up</td>
<td align="center">0.001277</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_UV_RESPONSE_DN</strong></td>
<td align="center">169</td>
<td align="center">Up</td>
<td align="center">0.9369</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_WNT_BETA_CATENIN_SIGNALING</strong></td>
<td align="center">47</td>
<td align="center">Up</td>
<td align="center">0.9369</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_G2M_CHECKPOINT</strong></td>
<td align="center">270</td>
<td align="center">Up</td>
<td align="center">0.9369</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL2_STAT5_SIGNALING</strong></td>
<td align="center">204</td>
<td align="center">Up</td>
<td align="center">0.9369</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MYOGENESIS</strong></td>
<td align="center">169</td>
<td align="center">Up</td>
<td align="center">0.9369</td>
</tr>
</tbody>
</table>

### Media Vs Sup

Apparently there are a lot of reactive O2 species in semen. See: Inactivation of human immunodeficiency virus type 1 by the amine oxidase-peroxidase system. PMID: 7559947

wikipedia says: xenobiotic metabolism (from the Greek xenos "stranger" and biotic "related to living beings") is the set of metabolic pathways that modify the chemical structure of xenobiotics, which are compounds foreign to an organism's normal biochemistry, such any drug or poison Results look drug related, but the "foreign substance" part makes sense in our context I guess.

<table>
<colgroup>
<col width="61%" />
<col width="11%" />
<col width="15%" />
<col width="11%" />
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
<td align="center">71</td>
<td align="center">Up</td>
<td align="center">1.681e-06</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_XENOBIOTIC_METABOLISM</strong></td>
<td align="center">189</td>
<td align="center">Up</td>
<td align="center">0.02032</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V1</strong></td>
<td align="center">303</td>
<td align="center">Up</td>
<td align="center">0.09788</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">291</td>
<td align="center">Up</td>
<td align="center">0.1619</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_FATTY_ACID_METABOLISM</strong></td>
<td align="center">177</td>
<td align="center">Up</td>
<td align="center">0.1904</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">93</td>
<td align="center">Down</td>
<td align="center">0.1904</td>
</tr>
</tbody>
</table>

### Low Exos Vs High Exos

<table>
<colgroup>
<col width="63%" />
<col width="11%" />
<col width="15%" />
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
<td align="center"><strong>HALLMARK_UV_RESPONSE_DN</strong></td>
<td align="center">169</td>
<td align="center">Up</td>
<td align="center">0.05732</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MITOTIC_SPINDLE</strong></td>
<td align="center">243</td>
<td align="center">Up</td>
<td align="center">0.1731</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_APICAL_JUNCTION</strong></td>
<td align="center">223</td>
<td align="center">Up</td>
<td align="center">0.2063</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_EPITHELIAL_MESENCHYMAL_TRANSITION</strong></td>
<td align="center">196</td>
<td align="center">Up</td>
<td align="center">0.2063</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL2_STAT5_SIGNALING</strong></td>
<td align="center">204</td>
<td align="center">Up</td>
<td align="center">0.2063</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ANDROGEN_RESPONSE</strong></td>
<td align="center">120</td>
<td align="center">Up</td>
<td align="center">0.2063</td>
</tr>
</tbody>
</table>

GO biological process gene sets: top 6 results
----------------------------------------------

Sean wrote some code (<https://github.com/seaaan/Bioinformatics/tree/master/GOTermMappingsForCamera>) to extract just the Biological Process gene sets out of all the GO gene sets. I will use those to test against the HVE data here.

### Media Vs Low Exos

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
<td align="center"><strong>GO_PEPTIDE_CROSS_LINKING</strong></td>
<td align="center">35</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINOCYTE_DIFFERENTIATION</strong></td>
<td align="center">89</td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_MYOBLAST_DIFFERENTIATION</strong></td>
<td align="center">17</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_ACTIN_FILAMENT_BASED_MOVEMENT</strong></td>
<td align="center">30</td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_KERATINIZATION</strong></td>
<td align="center">39</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_CARDIAC_MUSCLE_CELL_CONTRACTION</strong></td>
<td align="center">29</td>
<td align="center">Down</td>
</tr>
</tbody>
</table>

<table style="width:89%;">
<colgroup>
<col width="79%" />
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
<td align="center"><strong>GO_PEPTIDE_CROSS_LINKING</strong></td>
<td align="center">0.07043</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINOCYTE_DIFFERENTIATION</strong></td>
<td align="center">0.07043</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_MYOBLAST_DIFFERENTIATION</strong></td>
<td align="center">0.07043</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_ACTIN_FILAMENT_BASED_MOVEMENT</strong></td>
<td align="center">0.07113</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_KERATINIZATION</strong></td>
<td align="center">0.07113</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_REGULATION_OF_CARDIAC_MUSCLE_CELL_CONTRACTION</strong></td>
<td align="center">0.08575</td>
</tr>
</tbody>
</table>

### Media Vs High Exos

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
<td align="center"><strong>GO_PEPTIDE_CROSS_LINKING</strong></td>
<td align="center">35</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINIZATION</strong></td>
<td align="center">39</td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MEIOTIC_CHROMOSOME_SEPARATION</strong></td>
<td align="center">9</td>
<td align="center">Down</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINOCYTE_DIFFERENTIATION</strong></td>
<td align="center">89</td>
<td align="center">Down</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_CELL_ADHESION_MEDIATED_BY_INTEGRIN</strong></td>
<td align="center">31</td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHROMOSOME_SEPARATION</strong></td>
<td align="center">15</td>
<td align="center">Down</td>
</tr>
</tbody>
</table>

<table style="width:92%;">
<colgroup>
<col width="80%" />
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
<td align="center"><strong>GO_PEPTIDE_CROSS_LINKING</strong></td>
<td align="center">0.002746</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINIZATION</strong></td>
<td align="center">0.002746</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_MEIOTIC_CHROMOSOME_SEPARATION</strong></td>
<td align="center">0.527</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINOCYTE_DIFFERENTIATION</strong></td>
<td align="center">0.527</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_CELL_ADHESION_MEDIATED_BY_INTEGRIN</strong></td>
<td align="center">0.527</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_CHROMOSOME_SEPARATION</strong></td>
<td align="center">0.527</td>
</tr>
</tbody>
</table>

### Media Vs Sup

<table>
<colgroup>
<col width="58%" />
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
<td align="center"><strong>GO_CELLULAR_RESPONSE_TO_CADMIUM_ION</strong></td>
<td align="center">12</td>
<td align="center">Up</td>
<td align="center">1.43e-07</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PEPTIDE_CROSS_LINKING</strong></td>
<td align="center">35</td>
<td align="center">Down</td>
<td align="center">1.524e-06</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_CYCLOOXYGENASE_PATHWAY</strong></td>
<td align="center">9</td>
<td align="center">Up</td>
<td align="center">0.0002325</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PROSTAGLANDIN_METABOLIC_PROCESS</strong></td>
<td align="center">27</td>
<td align="center">Up</td>
<td align="center">0.0003587</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PROSTANOID_METABOLIC_PROCESS</strong></td>
<td align="center">27</td>
<td align="center">Up</td>
<td align="center">0.0003587</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_KERATINIZATION</strong></td>
<td align="center">39</td>
<td align="center">Down</td>
<td align="center">0.0003587</td>
</tr>
</tbody>
</table>

### Low Exos Vs High Exos

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
<td align="center"><strong>GO_REGULATION_OF_CALCINEURIN_NFAT_SIGNALING_CASCADE</strong></td>
<td align="center">17</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NEURON_MIGRATION</strong></td>
<td align="center">80</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PROTEIN_REFOLDING</strong></td>
<td align="center">28</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_NEURAL_PRECURSOR_CELL_PROLIFERATION</strong></td>
<td align="center">23</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_SISTER_CHROMATID_COHESION</strong></td>
<td align="center">20</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PHOSPHATIDYLETHANOLAMINE_ACYL_CHAIN_REMODELING</strong></td>
<td align="center">17</td>
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
<td align="center"><strong>GO_REGULATION_OF_CALCINEURIN_NFAT_SIGNALING_CASCADE</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NEURON_MIGRATION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PROTEIN_REFOLDING</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_NEURAL_PRECURSOR_CELL_PROLIFERATION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_SISTER_CHROMATID_COHESION</strong></td>
<td align="center">Up</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PHOSPHATIDYLETHANOLAMINE_ACYL_CHAIN_REMODELING</strong></td>
<td align="center">Up</td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="91%" />
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
<td align="center"><strong>GO_REGULATION_OF_CALCINEURIN_NFAT_SIGNALING_CASCADE</strong></td>
<td align="center">0.3669</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_NEURON_MIGRATION</strong></td>
<td align="center">0.3669</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_PROTEIN_REFOLDING</strong></td>
<td align="center">0.3669</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_POSITIVE_REGULATION_OF_NEURAL_PRECURSOR_CELL_PROLIFERATION</strong></td>
<td align="center">0.3669</td>
</tr>
<tr class="odd">
<td align="center"><strong>GO_REGULATION_OF_SISTER_CHROMATID_COHESION</strong></td>
<td align="center">0.4251</td>
</tr>
<tr class="even">
<td align="center"><strong>GO_PHOSPHATIDYLETHANOLAMINE_ACYL_CHAIN_REMODELING</strong></td>
<td align="center">0.4262</td>
</tr>
</tbody>
</table>
