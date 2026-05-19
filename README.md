# PSLpred: Prediction of Subcellular Localization of Bacterial Proteins

PSLpred is a computational web server developed for predicting the subcellular localization of Gram-negative bacterial proteins.

The tool predicts whether a bacterial protein belongs to cytoplasmic, extracellular, inner-membrane, outer-membrane, or periplasmic localization classes. PSLpred uses a hybrid machine learning approach that combines PSI-BLAST similarity search with support vector machine models based on amino acid composition, dipeptide composition, and physicochemical properties.

Web Server: http://www.imtech.res.in/raghava/pslpred/



## Citation

Bhasin, M., Garg, A., and Raghava, G. P. S. PSLpred: prediction of subcellular localization of bacterial proteins. Bioinformatics, 21(10), 2522-2524, 2005.

https://doi.org/10.1093/bioinformatics/bti309

his tool and dataset is also available on Zenodo at https://doi.org/10.5281/zenodo.20291158



## About the Research

Subcellular localization prediction is important because the biological function of a protein is strongly linked to where it is located inside or outside the cell.

In Gram-negative bacteria, proteins may localize to different compartments such as cytoplasm, inner membrane, periplasm, outer membrane, or extracellular space. Correct prediction of these locations helps in genome annotation, functional annotation, virulence factor identification, and drug or vaccine target discovery.

Earlier bacterial localization tools such as PSORT I, PSORT-B, NNPSL, and CELLO showed useful performance, but there was still scope for improvement, especially for extracellular proteins. PSLpred was developed to improve the prediction accuracy for Gram-negative bacterial protein localization using a hybrid SVM-based strategy.

Data Compilation: The dataset used in this study was the same dataset used previously for CELLO and PSORT-B. It was generated from SWISS-PROT release 40.29 and originally contained 1443 proteins. After removing 141 proteins with more than one localization, 1302 proteins were used for model development.

The final dataset contained:

- 248 cytoplasmic proteins
- 268 inner-membrane proteins
- 244 periplasmic proteins
- 352 outer-membrane proteins
- 190 extracellular proteins

Methodology: PSLpred uses support vector machine models trained with amino acid composition, dipeptide composition, physicochemical properties, and PSI-BLAST output. A hybrid model combining all these features achieved the best performance.



## Key Features

### 1. Gram-Negative Bacterial Protein Localization Prediction

Predictive Modeling: Allows users to submit bacterial protein sequences and predict their subcellular localization.

The tool predicts five localization classes:

- Cytoplasmic proteins
- Extracellular proteins
- Inner-membrane proteins
- Outer-membrane proteins
- Periplasmic proteins

Single Localization Prediction: The original version of PSLpred predicts one localization site for a submitted protein sequence.



### 2. SVM-Based Prediction Models

Amino Acid Composition Model: The amino acid composition-based SVM model achieved 86.1% overall accuracy.

Dipeptide Composition Model: The dipeptide composition-based SVM model also achieved 86.1% overall accuracy.

Physicochemical Properties Model: The physicochemical property-based SVM model achieved 83.0% overall accuracy.

ProPSI-BLAST Module: The PSI-BLAST-based similarity module achieved 68.1% overall accuracy.

Hybrid Model 1: The hybrid model combining amino acid composition, dipeptide composition, and physicochemical properties achieved 87.4% overall accuracy.

Hybrid Model 2: The best hybrid model combined amino acid composition, dipeptide composition, physicochemical properties, and PSI-BLAST output. It achieved 91.2% overall accuracy with MCC 0.89.



### 3. Best Performance Highlights

The best hybrid PSLpred model achieved the following class-wise accuracies:

- Cytoplasm: 90.7%
- Extracellular: 86.8%
- Inner membrane: 90.3%
- Outer membrane: 95.2%
- Periplasmic: 90.6%

Overall Accuracy: 91.2%

Overall MCC: 0.89

Reliability Index: PSLpred predicted around 74% of sequences with approximately 98% accuracy at reliability index 5.



### 4. Comparison with Existing Methods

PSLpred showed better overall performance than CELLO and PSORT-B on the same dataset.

Overall performance comparison:

- PSLpred: 91.2% accuracy
- CELLO: 88.9% accuracy
- PSORT-B: 74.8% accuracy

For extracellular proteins, PSLpred achieved 86.8% accuracy, improving over CELLO, which achieved 78.9% accuracy.

For periplasmic proteins, PSLpred achieved 90.6% accuracy, improving over CELLO and PSORT-B.



### 5. Integrated Web-Bench

Sequence Submission: Users can submit protein sequences for localization prediction.

SVM-Based Backend: The tool uses support vector machine models for classification.

Hybrid Prediction: The best-performing prediction option combines sequence composition, physicochemical properties, and PSI-BLAST similarity output.

Reliability Index: The server provides a reliability index to indicate prediction confidence.

Supplementary Information: Additional model details and performance tables are available through the PSLpred supplementary page.



## Applications

Bacterial Protein Annotation: PSLpred can help annotate Gram-negative bacterial proteins according to their likely subcellular location.

Genome Annotation: The tool can support automated annotation of newly sequenced bacterial genomes.

Virulence Factor Identification: Extracellular and membrane-associated proteins may represent important virulence-related proteins.

Drug Target Discovery: Localization information can help prioritize bacterial proteins as possible drug targets.

Vaccine Candidate Screening: Outer-membrane, extracellular, and periplasmic proteins may be useful for identifying vaccine candidates.

Comparative Proteomics: PSLpred can support large-scale comparison of protein localization patterns across Gram-negative bacteria.



## Contact and Authors

Prof. G. P. S. Raghava  
Corresponding Author  

Email: raghava@iiitd.ac.in

Department of Computational Biology, 

Indraprastha Institute of Information Technology (IIIT-Delhi), New Delhi, India.


## Support

This work was supported by the Council of Scientific and Industrial Research and the Department of Biotechnology, Government of India.

This work has IMTECH communication number 52/2004.
