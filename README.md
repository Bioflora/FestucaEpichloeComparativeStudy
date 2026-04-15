# FestucaEpichloecomparativeStudy

```
The project is organized under the main directory FestucaEpichloeComparativeStudy/, structured into two major modules: Plant_host/ and 
Fungal_endophyte/. Each module contains data, scripts, and/or outputs corresponding to specific stages of the analysis.
Folder system as follows:

FestucaEpichloeComparativeStudy/
│
├── Plant_host/
│   └── data/                                                                      
│       └── flow_cytometry_host.csv            # Genome size estimations via flow cytometry for the Festuca species.
│                                              Variables: Holobiont_ID (holobiont identification code);
│                                              Host_sp (plant host species);
|                                              Endophyte_sp (fungal endophyte species);
│                                              measurement_ID (measurement identification code);
│                                              nucleids (number of particles counted in the sample); 
│                                              nucleids_ST (number of particles counted in the standard); 
│                                              mean (arithmetic mean of the fluorescence intensities of all particlesincluded in the sample); 
│                                              mean_ST (arithmetic mean of the fluorescence intensities of all particles included in the standard);
│                                              CV (coefficient of Variation of the sample); 
│                                              CV_ST (coefficient of Variation of the standard);
│                                              pg/2C (estimated genome size of the sample); 
│                                              pg/2C_ST (known genome size of the standard);
│
│
├── Fungal_endophyte/
│   ├── data/
│   │   ├── outputs_script1/                   # Output files of the morphological analyses (from script1.Rmd)
│   │   ├── outputs_script2/                   # Raw single-gene, species tree and concatenated ML files (from script2.sh)
│   │   ├── outputs_script3/                   # Formated single-gene, species tree and concatenated ML files (from script3.Rmd)
│   │   ├── outputs_script4/                   # Alkaloids heatmap (from script4.Rmd)
│   │   ├── Phylogenetic_analysis/
│   │   │   │  
│   │   │   ├── MSA/                           # Multiple sequence alignments (FASTA format)
│   │   │   │  
│   │   │   ├── PP_values_ASTRAL_SPTREE.xlsx   # Posterior probability values for each node of the ASTRAL phylogenetic tree. Input script2.Rmd.
│   │   │   ├── Q_values_ASTRAL_SPTREE.xlsx    # Quartet values for each node of the ASTRAL phylogenetic tree. Input script2.Rmd.
│   │   │   ├── UFBoot_values_actG.xlsx        # UltraFast bootstrap values for each node in the actG phylogenetic tree. Input script2.Rmd.
│   │   │   ├── UFBoot_values_CalM.xlsx        # UltraFast bootstrap values for each node in the CalM phylogenetic tree. Input script2.Rmd.
│   │   │   ├── UFBoot_values_ITS.xlsx         # UltraFast bootstrap values for each node in the ITS phylogenetic tree. Input script2.Rmd.
│   │   │   ├── UFBoot_values_tefA.xlsx        # UltraFast bootstrap values for each node in the tefA phylogenetic tree. Input script2.Rmd.
│   │   │   ├── UFBoot_values_tubB.xlsx        # UltraFast bootstrap values for each node in the tubB phylogenetic tree. Input script2.Rmd.
│   │   │   └── UFBoot_and_scfl_values_MLtree  # UltraFast bootstrap and SCFL values for each node in the ML phylogeentic tree. Input script2.Rmd.
│   │   │   
│   │   ├── culture_growth_dataset.csv         # Dataset for culture growth rate analysis (used in script1.Rmd).
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: IndID (measurement identification code);
│   │   │                                      Ind (short name for each isolate);
│   │   │                                      Rep (replicate code within each isolate);
│   │   │                                      Day (Day the measurement was made);
│   │   │                                      Diameter (diameter of the culture in mm)
│   │   │                                      Species (holobiont idntification code).
│   │   │ 
│   │   ├── spores_dataset.csv                 # Morphometric data of asexual reproductive structures (used in script1.Rmd). 
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: Species (holobiont identification code);
│   │   │                                      SampleID (measurement identification code); 
│   │   │                                      Ind (short name for each isolate);   
│   │   │                                      conidL (conidial length in μm);
│   │   │                                      conidW (conidial width in μm); 
│   │   │                                      conidiophL (conidiophore length in μm);
│   │   │                                      conidiophW (conidiophore width in μm); 
│   │   │                                      conidA (conidial area in μm²); 
│   │   │
│   │   ├── alkaloids_qualitative.csv          # Dataset for qualitative detection for the four alkaloid families.
│   │   │                                      Presence indicated with "YES", traces indicated with "TRACES" and absence indicated with "NO".
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 25 correspond to chemical compounds tested.
│   │   │
│   │   ├── alkaloids_quantitative.csv         # Dataset for quantitative measurements for the three alkaloid families.
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 6 correspond to compounds concentrations detected (units are specified in each case).
│   │   │   
│   │   ├── alkaloids_PCR.csv                  # Dataset for PCR results for the key fungal genes involved in alkaloid synthesis.
│   │   │                                      Presence indicated with "+" and absence indicated with "-".
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 9 correspond to the key fungal genes tested.
│   │   │
│   │   │  
│   │   └── flow_cytometry_endophyte.csv       # Genome size estimations of Epichloë festucae via flow cytometry.
│   │                                          Variables: Holobiont_ID (holobiont identification code);
│   │                                          Host_sp: (plant host specuiese identification code); 
│   │                                          Measurement_ID (measurement identification code);
│   │                                          nucleids (number of particles counted in the sample); 
│   │                                          nucleids_ST (number of particles counted in the standard); 
│   │                                          mean (arithmetic mean of the fluorescence intensities of all particles included in the sample); 
│   │                                          mean_ST (arithmetic mean of the fluorescence intensities of all particles included in the standard);
│   │                                          CV (coefficient of Variation of the sample); 
│   │                                          CV_ST (coefficient of Variation of the standard);
│   │                                          pg/1C (estimated genome size of the sample); 
│   │                                          pg/1C_ST (known genome size of the standard);             
│   │
│   └── scripts/
│       ├── script1.Rmd                       # RMarkdown: Morphological analysis of fungal endophyte.
│       ├── script2.sh                        # Shell script: Phylogenetic inference using IQ-TREE2 and ASTRAL.
│       ├── script3.Rmd                       # Rmarkdown: Visualization and editing of phylogenetic trees.
│       └── script4.Rmd                       # RMarkdown: Generation of the alkaloids heatmap.
└

```
