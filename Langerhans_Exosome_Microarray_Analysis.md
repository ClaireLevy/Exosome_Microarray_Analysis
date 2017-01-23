Exosome Microarray Analysis: Langerhans cells only
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

The following analysis is only for Langerhans cells
---------------------------------------------------

    ## Inputting the data ...
    ## Perform Quality Control assessment of the LumiBatch object ...

Plots of non-normalized data

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/density-1.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non-norm-1.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20MSD%20plot-1.png)![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20MSD%20plot-2.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/non%20norm%20boxplot-1.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20density-1.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-1.png)![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-2.png)![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/norm%20MDS-3.png)

![](Langerhans_Exosome_Microarray_Analysis_files/figure-markdown_github/normed%20boxplot-1.png)

Non-specific filtering
----------------------

Limma suggests to keep probes that are expressed above background on at least n arrays where n is smallest number of replicates assigned to any of the treatment combinations.

We have 3 donors x 3 viruses x 4 Treatments so I will keep probes with detection levels above background in at least 3 samples.

Number of probes in data set before filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   47323     47323 47323    47323
    ## Samples       36        36    36       36

Number of probes in data set after filtering:

    ##          beadNum detection exprs se.exprs
    ## Features   24137     24137 24137    24137
    ## Samples       36        36    36       36

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
<td align="center">2</td>
<td align="center">1</td>
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
<td align="center">1</td>
<td align="center">4</td>
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
<td align="center">13</td>
</tr>
</tbody>
</table>

<table style="width:71%;">
<caption>Table continues below</caption>
<colgroup>
<col width="19%" />
<col width="13%" />
<col width="23%" />
<col width="13%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">ProbeID</th>
<th align="center">ENTREZ_GENE_ID</th>
<th align="center">TargetID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>4200577</strong></td>
<td align="center">4200577</td>
<td align="center">9569</td>
<td align="center">GTF2IRD1</td>
</tr>
<tr class="even">
<td align="center"><strong>2690279</strong></td>
<td align="center">2690279</td>
<td align="center">170261</td>
<td align="center">ZCCHC12</td>
</tr>
<tr class="odd">
<td align="center"><strong>4560129</strong></td>
<td align="center">4560129</td>
<td align="center">5641</td>
<td align="center">LGMN</td>
</tr>
</tbody>
</table>

<table style="width:78%;">
<colgroup>
<col width="19%" />
<col width="43%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">DEFINITION</th>
<th align="center">adj.P.Val</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>4200577</strong></td>
<td align="center">Homo sapiens GTF2I repeat domain containing 1 (GTF2IRD1), transcript variant 1, mRNA.</td>
<td align="center">0.006405</td>
</tr>
<tr class="even">
<td align="center"><strong>2690279</strong></td>
<td align="center">Homo sapiens zinc finger, CCHC domain containing 12 (ZCCHC12), mRNA.</td>
<td align="center">0.007722</td>
</tr>
<tr class="odd">
<td align="center"><strong>4560129</strong></td>
<td align="center">Homo sapiens legumain (LGMN), transcript variant 2, mRNA.</td>
<td align="center">0.02735</td>
</tr>
</tbody>
</table>

<table style="width:100%;">
<caption>Table continues below</caption>
<colgroup>
<col width="17%" />
<col width="12%" />
<col width="21%" />
<col width="13%" />
<col width="35%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">ProbeID</th>
<th align="center">ENTREZ_GENE_ID</th>
<th align="center">TargetID</th>
<th align="center">DEFINITION</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>1170300</strong></td>
<td align="center">1170300</td>
<td align="center">4495</td>
<td align="center">MT1G</td>
<td align="center">Homo sapiens metallothionein 1G (MT1G), mRNA.</td>
</tr>
<tr class="even">
<td align="center"><strong>7560037</strong></td>
<td align="center">7560037</td>
<td align="center">170954</td>
<td align="center">KIAA1949</td>
<td align="center">Homo sapiens KIAA1949 (KIAA1949), mRNA.</td>
</tr>
<tr class="odd">
<td align="center"><strong>130093</strong></td>
<td align="center">130093</td>
<td align="center">4496</td>
<td align="center">MT1H</td>
<td align="center">Homo sapiens metallothionein 1H (MT1H), mRNA.</td>
</tr>
<tr class="even">
<td align="center"><strong>2070288</strong></td>
<td align="center">2070288</td>
<td align="center">4493</td>
<td align="center">MT1E</td>
<td align="center">Homo sapiens metallothionein 1E (MT1E), mRNA.</td>
</tr>
<tr class="odd">
<td align="center"><strong>6620528</strong></td>
<td align="center">6620528</td>
<td align="center">4501</td>
<td align="center">MT1X</td>
<td align="center">Homo sapiens metallothionein 1X (MT1X), mRNA.</td>
</tr>
</tbody>
</table>

<table style="width:35%;">
<colgroup>
<col width="19%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">adj.P.Val</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>1170300</strong></td>
<td align="center">0.006297</td>
</tr>
<tr class="even">
<td align="center"><strong>7560037</strong></td>
<td align="center">0.006297</td>
</tr>
<tr class="odd">
<td align="center"><strong>130093</strong></td>
<td align="center">0.01389</td>
</tr>
<tr class="even">
<td align="center"><strong>2070288</strong></td>
<td align="center">0.04671</td>
</tr>
<tr class="odd">
<td align="center"><strong>6620528</strong></td>
<td align="center">0.04776</td>
</tr>
</tbody>
</table>

<table style="width:71%;">
<caption>Table continues below</caption>
<colgroup>
<col width="19%" />
<col width="13%" />
<col width="23%" />
<col width="13%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">ProbeID</th>
<th align="center">ENTREZ_GENE_ID</th>
<th align="center">TargetID</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>4220187</strong></td>
<td align="center">4220187</td>
<td align="center">8291</td>
<td align="center">DYSF</td>
</tr>
<tr class="even">
<td align="center"><strong>6180706</strong></td>
<td align="center">6180706</td>
<td align="center">4062</td>
<td align="center">LY6H</td>
</tr>
<tr class="odd">
<td align="center"><strong>3990561</strong></td>
<td align="center">3990561</td>
<td align="center">4062</td>
<td align="center">LY6H</td>
</tr>
<tr class="even">
<td align="center"><strong>4260612</strong></td>
<td align="center">4260612</td>
<td align="center">8859</td>
<td align="center">STK19</td>
</tr>
<tr class="odd">
<td align="center"><strong>630678</strong></td>
<td align="center">630678</td>
<td align="center">414149</td>
<td align="center">ACBD7</td>
</tr>
<tr class="even">
<td align="center"><strong>2690279</strong></td>
<td align="center">2690279</td>
<td align="center">170261</td>
<td align="center">ZCCHC12</td>
</tr>
<tr class="odd">
<td align="center"><strong>2030093</strong></td>
<td align="center">2030093</td>
<td align="center">5315</td>
<td align="center">PKM2</td>
</tr>
<tr class="even">
<td align="center"><strong>4150204</strong></td>
<td align="center">4150204</td>
<td align="center">51450</td>
<td align="center">PRRX2</td>
</tr>
<tr class="odd">
<td align="center"><strong>1660484</strong></td>
<td align="center">1660484</td>
<td align="center">284013</td>
<td align="center">VMO1</td>
</tr>
<tr class="even">
<td align="center"><strong>3850202</strong></td>
<td align="center">3850202</td>
<td align="center">10261</td>
<td align="center">IGSF6</td>
</tr>
<tr class="odd">
<td align="center"><strong>6620609</strong></td>
<td align="center">6620609</td>
<td align="center">80325</td>
<td align="center">ABTB1</td>
</tr>
<tr class="even">
<td align="center"><strong>2140762</strong></td>
<td align="center">2140762</td>
<td align="center">7531</td>
<td align="center">YWHAE</td>
</tr>
<tr class="odd">
<td align="center"><strong>4230487</strong></td>
<td align="center">4230487</td>
<td align="center">728908</td>
<td align="center">LOC728908</td>
</tr>
<tr class="even">
<td align="center"><strong>2100296</strong></td>
<td align="center">2100296</td>
<td align="center">9476</td>
<td align="center">NAPSA</td>
</tr>
<tr class="odd">
<td align="center"><strong>160170</strong></td>
<td align="center">160170</td>
<td align="center">5315</td>
<td align="center">PKM2</td>
</tr>
<tr class="even">
<td align="center"><strong>6580639</strong></td>
<td align="center">6580639</td>
<td align="center">11332</td>
<td align="center">ACOT7</td>
</tr>
<tr class="odd">
<td align="center"><strong>6770097</strong></td>
<td align="center">6770097</td>
<td align="center">80019</td>
<td align="center">UBTD1</td>
</tr>
<tr class="even">
<td align="center"><strong>4880551</strong></td>
<td align="center">4880551</td>
<td align="center">79171</td>
<td align="center">RBM42</td>
</tr>
<tr class="odd">
<td align="center"><strong>2600630</strong></td>
<td align="center">2600630</td>
<td align="center">908</td>
<td align="center">CCT6A</td>
</tr>
<tr class="even">
<td align="center"><strong>70070</strong></td>
<td align="center">70070</td>
<td align="center">2907</td>
<td align="center">GRINA</td>
</tr>
<tr class="odd">
<td align="center"><strong>4120538</strong></td>
<td align="center">4120538</td>
<td align="center">731314</td>
<td align="center">LOC731314</td>
</tr>
<tr class="even">
<td align="center"><strong>4570239</strong></td>
<td align="center">4570239</td>
<td align="center">4014</td>
<td align="center">LOR</td>
</tr>
</tbody>
</table>

<table style="width:78%;">
<colgroup>
<col width="19%" />
<col width="43%" />
<col width="15%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">DEFINITION</th>
<th align="center">adj.P.Val</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>4220187</strong></td>
<td align="center">Homo sapiens dysferlin, limb girdle muscular dystrophy 2B (autosomal recessive) (DYSF), mRNA.</td>
<td align="center">0.008757</td>
</tr>
<tr class="even">
<td align="center"><strong>6180706</strong></td>
<td align="center">Homo sapiens lymphocyte antigen 6 complex, locus H (LY6H), mRNA.</td>
<td align="center">0.008757</td>
</tr>
<tr class="odd">
<td align="center"><strong>3990561</strong></td>
<td align="center">Homo sapiens lymphocyte antigen 6 complex, locus H (LY6H), mRNA.</td>
<td align="center">0.008757</td>
</tr>
<tr class="even">
<td align="center"><strong>4260612</strong></td>
<td align="center">Homo sapiens serine/threonine kinase 19 (STK19), transcript variant 1, mRNA.</td>
<td align="center">0.01302</td>
</tr>
<tr class="odd">
<td align="center"><strong>630678</strong></td>
<td align="center">PREDICTED: Homo sapiens acyl-Coenzyme A binding domain containing 7 (ACBD7), mRNA.</td>
<td align="center">0.01302</td>
</tr>
<tr class="even">
<td align="center"><strong>2690279</strong></td>
<td align="center">Homo sapiens zinc finger, CCHC domain containing 12 (ZCCHC12), mRNA.</td>
<td align="center">0.01304</td>
</tr>
<tr class="odd">
<td align="center"><strong>2030093</strong></td>
<td align="center">Homo sapiens pyruvate kinase, muscle (PKM2), transcript variant 2, mRNA.</td>
<td align="center">0.01995</td>
</tr>
<tr class="even">
<td align="center"><strong>4150204</strong></td>
<td align="center">Homo sapiens paired related homeobox 2 (PRRX2), mRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="odd">
<td align="center"><strong>1660484</strong></td>
<td align="center">Homo sapiens vitelline membrane outer layer 1 homolog (chicken) (VMO1), mRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="even">
<td align="center"><strong>3850202</strong></td>
<td align="center">Homo sapiens immunoglobulin superfamily, member 6 (IGSF6), mRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="odd">
<td align="center"><strong>6620609</strong></td>
<td align="center">Homo sapiens ankyrin repeat and BTB (POZ) domain containing 1 (ABTB1), transcript variant 3, mRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="even">
<td align="center"><strong>2140762</strong></td>
<td align="center">Homo sapiens tyrosine 3-monooxygenase/tryptophan 5-monooxygenase activation protein, epsilon polypeptide (YWHAE), mRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="odd">
<td align="center"><strong>4230487</strong></td>
<td align="center">PREDICTED: Homo sapiens misc_RNA (LOC728908), miscRNA.</td>
<td align="center">0.03157</td>
</tr>
<tr class="even">
<td align="center"><strong>2100296</strong></td>
<td align="center">Homo sapiens napsin A aspartic peptidase (NAPSA), mRNA.</td>
<td align="center">0.03515</td>
</tr>
<tr class="odd">
<td align="center"><strong>160170</strong></td>
<td align="center">Homo sapiens pyruvate kinase, muscle (PKM2), transcript variant 3, mRNA.</td>
<td align="center">0.04301</td>
</tr>
<tr class="even">
<td align="center"><strong>6580639</strong></td>
<td align="center">Homo sapiens acyl-CoA thioesterase 7 (ACOT7), transcript variant hBACHa, mRNA.</td>
<td align="center">0.04398</td>
</tr>
<tr class="odd">
<td align="center"><strong>6770097</strong></td>
<td align="center">Homo sapiens ubiquitin domain containing 1 (UBTD1), mRNA.</td>
<td align="center">0.04398</td>
</tr>
<tr class="even">
<td align="center"><strong>4880551</strong></td>
<td align="center">Homo sapiens RNA binding motif protein 42 (RBM42), mRNA.</td>
<td align="center">0.04408</td>
</tr>
<tr class="odd">
<td align="center"><strong>2600630</strong></td>
<td align="center">Homo sapiens chaperonin containing TCP1, subunit 6A (zeta 1) (CCT6A), transcript variant 1, mRNA.</td>
<td align="center">0.04408</td>
</tr>
<tr class="even">
<td align="center"><strong>70070</strong></td>
<td align="center">Homo sapiens glutamate receptor, ionotropic, N-methyl D-aspartate-associated protein 1 (glutamate binding) (GRINA), transcript variant 1, mRNA.</td>
<td align="center">0.04433</td>
</tr>
<tr class="odd">
<td align="center"><strong>4120538</strong></td>
<td align="center">PREDICTED: Homo sapiens similar to H2A histone family, member X (LOC731314), mRNA.</td>
<td align="center">0.04433</td>
</tr>
<tr class="even">
<td align="center"><strong>4570239</strong></td>
<td align="center">Homo sapiens loricrin (LOR), mRNA.</td>
<td align="center">0.04433</td>
</tr>
</tbody>
</table>

CAMERA testing
==============

Hallmark gene sets: top 6 results
---------------------------------

\begin{center}
### None.Media Vs None.Exos
\end{center}
<table>
<colgroup>
<col width="56%" />
<col width="10%" />
<col width="14%" />
<col width="10%" />
<col width="7%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">73</td>
<td align="center">Up</td>
<td align="center">0.01136</td>
<td align="center">0.4394</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">294</td>
<td align="center">Down</td>
<td align="center">0.01758</td>
<td align="center">0.4394</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_UNFOLDED_PROTEIN_RESPONSE</strong></td>
<td align="center">154</td>
<td align="center">Down</td>
<td align="center">0.03232</td>
<td align="center">0.4462</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">135</td>
<td align="center">Down</td>
<td align="center">0.03569</td>
<td align="center">0.4462</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">213</td>
<td align="center">Up</td>
<td align="center">0.05954</td>
<td align="center">0.5954</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_NOTCH_SIGNALING</strong></td>
<td align="center">39</td>
<td align="center">Down</td>
<td align="center">0.1044</td>
<td align="center">0.8701</td>
</tr>
</tbody>
</table>

\begin{center}
### None.Media Vs None.Lipo
\end{center}
<table>
<colgroup>
<col width="50%" />
<col width="10%" />
<col width="14%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">258</td>
<td align="center">Down</td>
<td align="center">5.64e-08</td>
<td align="center">2.82e-06</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_OXIDATIVE_PHOSPHORYLATION</strong></td>
<td align="center">272</td>
<td align="center">Up</td>
<td align="center">0.0001904</td>
<td align="center">0.00476</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_DNA_REPAIR</strong></td>
<td align="center">213</td>
<td align="center">Up</td>
<td align="center">0.0004751</td>
<td align="center">0.007919</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">214</td>
<td align="center">Down</td>
<td align="center">0.001003</td>
<td align="center">0.01253</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V2</strong></td>
<td align="center">83</td>
<td align="center">Up</td>
<td align="center">0.00172</td>
<td align="center">0.0172</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V1</strong></td>
<td align="center">306</td>
<td align="center">Up</td>
<td align="center">0.006571</td>
<td align="center">0.05475</td>
</tr>
</tbody>
</table>

\begin{center}
### None.Media Vs None.Sup
\end{center}
<table>
<caption>Table continues below</caption>
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
<th align="center">PValue</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_UNFOLDED_PROTEIN_RESPONSE</strong></td>
<td align="center">154</td>
<td align="center">Down</td>
<td align="center">0.001996</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">73</td>
<td align="center">Up</td>
<td align="center">0.002298</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">135</td>
<td align="center">Down</td>
<td align="center">0.01063</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_G2M_CHECKPOINT</strong></td>
<td align="center">270</td>
<td align="center">Up</td>
<td align="center">0.01735</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">294</td>
<td align="center">Down</td>
<td align="center">0.03114</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">227</td>
<td align="center">Down</td>
<td align="center">0.03199</td>
</tr>
</tbody>
</table>

<table style="width:75%;">
<colgroup>
<col width="65%" />
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
<td align="center"><strong>HALLMARK_UNFOLDED_PROTEIN_RESPONSE</strong></td>
<td align="center">0.05744</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">0.05744</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">0.1771</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_G2M_CHECKPOINT</strong></td>
<td align="center">0.2169</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">0.2454</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">0.2454</td>
</tr>
</tbody>
</table>

\begin{center}
### Sendai.Media Vs Sendai.Exo
\end{center}
<table>
<colgroup>
<col width="56%" />
<col width="10%" />
<col width="14%" />
<col width="10%" />
<col width="7%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_GLYCOLYSIS</strong></td>
<td align="center">242</td>
<td align="center">Up</td>
<td align="center">0.0115</td>
<td align="center">0.4646</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INTERFERON_ALPHA_RESPONSE</strong></td>
<td align="center">124</td>
<td align="center">Down</td>
<td align="center">0.02341</td>
<td align="center">0.4646</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V1</strong></td>
<td align="center">306</td>
<td align="center">Down</td>
<td align="center">0.04111</td>
<td align="center">0.4646</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_HYPOXIA</strong></td>
<td align="center">250</td>
<td align="center">Up</td>
<td align="center">0.04382</td>
<td align="center">0.4646</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_CHOLESTEROL_HOMEOSTASIS</strong></td>
<td align="center">94</td>
<td align="center">Up</td>
<td align="center">0.05488</td>
<td align="center">0.4646</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">73</td>
<td align="center">Up</td>
<td align="center">0.0573</td>
<td align="center">0.4646</td>
</tr>
</tbody>
</table>

\begin{center}
### Sendai.Media Vs Sendai.Lipo
\end{center}
<table>
<colgroup>
<col width="52%" />
<col width="12%" />
<col width="16%" />
<col width="12%" />
<col width="8%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_MITOTIC_SPINDLE</strong></td>
<td align="center">251</td>
<td align="center">Up</td>
<td align="center">0.07728</td>
<td align="center">0.9933</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">258</td>
<td align="center">Down</td>
<td align="center">0.07856</td>
<td align="center">0.9933</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_SPERMATOGENESIS</strong></td>
<td align="center">117</td>
<td align="center">Up</td>
<td align="center">0.08184</td>
<td align="center">0.9933</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_UV_RESPONSE_UP</strong></td>
<td align="center">196</td>
<td align="center">Down</td>
<td align="center">0.1401</td>
<td align="center">0.9933</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_PANCREAS_BETA_CELLS</strong></td>
<td align="center">30</td>
<td align="center">Down</td>
<td align="center">0.1438</td>
<td align="center">0.9933</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TGF_BETA_SIGNALING</strong></td>
<td align="center">74</td>
<td align="center">Down</td>
<td align="center">0.144</td>
<td align="center">0.9933</td>
</tr>
</tbody>
</table>

\begin{center}
### Sendai.Media Vs Sendai.Sup
\end{center}
<table>
<colgroup>
<col width="50%" />
<col width="10%" />
<col width="14%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_INTERFERON_ALPHA_RESPONSE</strong></td>
<td align="center">124</td>
<td align="center">Down</td>
<td align="center">4.042e-11</td>
<td align="center">2.021e-09</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INTERFERON_GAMMA_RESPONSE</strong></td>
<td align="center">270</td>
<td align="center">Down</td>
<td align="center">6.068e-08</td>
<td align="center">1.517e-06</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL6_JAK_STAT3_SIGNALING</strong></td>
<td align="center">104</td>
<td align="center">Down</td>
<td align="center">0.0004971</td>
<td align="center">0.008284</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">214</td>
<td align="center">Down</td>
<td align="center">0.001009</td>
<td align="center">0.01249</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">258</td>
<td align="center">Down</td>
<td align="center">0.001249</td>
<td align="center">0.01249</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">227</td>
<td align="center">Down</td>
<td align="center">0.006023</td>
<td align="center">0.05019</td>
</tr>
</tbody>
</table>

\begin{center}
### HIV.Media Vs HIV.Exo
\end{center}
<table>
<colgroup>
<col width="48%" />
<col width="11%" />
<col width="15%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">135</td>
<td align="center">Down</td>
<td align="center">4.091e-05</td>
<td align="center">0.002046</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">258</td>
<td align="center">Down</td>
<td align="center">0.001547</td>
<td align="center">0.03867</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">214</td>
<td align="center">Down</td>
<td align="center">0.003603</td>
<td align="center">0.04704</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MTORC1_SIGNALING</strong></td>
<td align="center">294</td>
<td align="center">Down</td>
<td align="center">0.003763</td>
<td align="center">0.04704</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL6_JAK_STAT3_SIGNALING</strong></td>
<td align="center">104</td>
<td align="center">Down</td>
<td align="center">0.006261</td>
<td align="center">0.06261</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">227</td>
<td align="center">Down</td>
<td align="center">0.008814</td>
<td align="center">0.06583</td>
</tr>
</tbody>
</table>

\begin{center}
### HIV.Media Vs HIV.Lipo
\end{center}
<table>
<colgroup>
<col width="50%" />
<col width="11%" />
<col width="15%" />
<col width="12%" />
<col width="9%" />
</colgroup>
<thead>
<tr class="header">
<th align="center"> </th>
<th align="center">NGenes</th>
<th align="center">Direction</th>
<th align="center">PValue</th>
<th align="center">FDR</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_TNFA_SIGNALING_VIA_NFKB</strong></td>
<td align="center">258</td>
<td align="center">Down</td>
<td align="center">0.0002242</td>
<td align="center">0.01121</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V2</strong></td>
<td align="center">83</td>
<td align="center">Up</td>
<td align="center">0.002188</td>
<td align="center">0.05469</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ANDROGEN_RESPONSE</strong></td>
<td align="center">126</td>
<td align="center">Down</td>
<td align="center">0.03306</td>
<td align="center">0.3641</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_COMPLEMENT</strong></td>
<td align="center">226</td>
<td align="center">Down</td>
<td align="center">0.04518</td>
<td align="center">0.3641</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_IL2_STAT5_SIGNALING</strong></td>
<td align="center">249</td>
<td align="center">Down</td>
<td align="center">0.05063</td>
<td align="center">0.3641</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">135</td>
<td align="center">Down</td>
<td align="center">0.05086</td>
<td align="center">0.3641</td>
</tr>
</tbody>
</table>

\begin{center}
### HIV.Media Vs HIV.Sup
\end{center}
<table>
<caption>Table continues below</caption>
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
<th align="center">PValue</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">135</td>
<td align="center">Down</td>
<td align="center">7.757e-05</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">214</td>
<td align="center">Down</td>
<td align="center">0.003724</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">227</td>
<td align="center">Down</td>
<td align="center">0.005486</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">73</td>
<td align="center">Up</td>
<td align="center">0.00847</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V2</strong></td>
<td align="center">83</td>
<td align="center">Down</td>
<td align="center">0.03238</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_E2F_TARGETS</strong></td>
<td align="center">287</td>
<td align="center">Up</td>
<td align="center">0.0337</td>
</tr>
</tbody>
</table>

<table style="width:76%;">
<colgroup>
<col width="65%" />
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
<td align="center"><strong>HALLMARK_PROTEIN_SECRETION</strong></td>
<td align="center">0.003879</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_INFLAMMATORY_RESPONSE</strong></td>
<td align="center">0.09144</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_ALLOGRAFT_REJECTION</strong></td>
<td align="center">0.09144</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_REACTIVE_OXIGEN_SPECIES_PATHWAY</strong></td>
<td align="center">0.1059</td>
</tr>
<tr class="odd">
<td align="center"><strong>HALLMARK_MYC_TARGETS_V2</strong></td>
<td align="center">0.2418</td>
</tr>
<tr class="even">
<td align="center"><strong>HALLMARK_E2F_TARGETS</strong></td>
<td align="center">0.2418</td>
</tr>
</tbody>
</table>
