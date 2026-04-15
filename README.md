# FestucaEpichloecomparativeStudy

```
The project is organized under the main directory FestucaEpichloeComparativeStudy/, structured into two
major modules: Plant_host/ and Fungal_endophyte/. Each module contains data, scripts, and/or outputs
corresponding to specific stages of the analysis. Folder system as follows:

FestucaEpichloeComparativeStudy/
│
├── Plant_host/
│   └── data/                                                                      
│       └── flow_cytometry_host.csv            # Genome size estimations via flow cytometry for the Fescues.
│                                              Variables: Holobiont_ID (holobiont identification code);
│                                              Host_sp (plant host species);
|                                              Endophyte_sp (fungal endophyte species);
│                                              measurement_ID (measurement identification code);
│                                              nucleids (number of particles counted, sample); 
│                                              nucleids_ST (number of particles counted, standard); 
│                                              mean (arithmetic mean of the fluorescence intensities, sample); 
│                                              mean_ST (arithmetic mean of the fluorescence intensities, standard);
│                                              CV (coefficient of Variation, sample); 
│                                              CV_ST (coefficient of Variation, standard);
│                                              pg/2C (estimated genome size, sample); 
│                                              pg/2C_ST (known genome size, standard);
│
│
├── Fungal_endophyte/
│   ├── data/
│   │   ├── outputs_script1/                   # Output files of the morphological analyses
│   │   ├── outputs_script2/                   # Raw single-gene, species tree and concatenated ML files
│   │   ├── outputs_script3/                   # Formated single-gene, species tree and concatenated ML files
│   │   ├── outputs_script4/                   # Alkaloids heatmap, raw figures (from script4.Rmd)
│   │   ├── Phylogenetic_analysis/
│   │   │   │  
│   │   │   ├── MSA/                           # Multiple sequence alignments (FASTA format; input script2.sh)
│   │   │   ├── TREES/                         # Files obtained from script2.sh (raw phylogenetic trees; input script3.Rmd) 
│   │   │   ├── PP_values_ASTRAL_SPTREE.xlsx   # Posterior probability values for the ASTRAL tree; input script3.Rmd.
│   │   │   ├── Q_values_ASTRAL_SPTREE.xlsx    # Quartet values for each node of the ASTRAL tree; input script3.Rmd.
│   │   │   ├── UFBoot_values_actG.xlsx        # UltraFast bootstrap values for the actG tree; input script3.Rmd.
│   │   │   ├── UFBoot_values_CalM.xlsx        # UltraFast bootstrap values for the CalM tree; input script3.Rmd.
│   │   │   ├── UFBoot_values_ITS.xlsx         # UltraFast bootstrap values for ITS tree; input script3.Rmd.
│   │   │   ├── UFBoot_values_tefA.xlsx        # UltraFast bootstrap values for the tefA tree; input script3.Rmd.
│   │   │   ├── UFBoot_values_tubB.xlsx        # UltraFast bootstrap values for the tubB tree; input script3.Rmd.
│   │   │   └── UFBootscfl_values_MLtree.xslx  # UltraFast bootstrap and SCFL values for the ML tree; input script3.Rmd.
│   │   │   
│   │   ├── culture_growth_dataset.csv         # Dataset for culture growth rate analysis (input script1.Rmd).
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: IndID (measurement identification code);
│   │   │                                      Ind (short name for each isolate);
│   │   │                                      Rep (replicate code within each isolate);
│   │   │                                      Day (Day the measurement was made);
│   │   │                                      Diameter (diameter of the culture in mm)
│   │   │                                      Species (holobiont idntification code).
│   │   │ 
│   │   ├── spores_dataset.csv                 # Morphometric data of asexual reproductive structures (input in script1.Rmd). 
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: Species (holobiont identification code);
│   │   │                                      SampleID (measurement identification code); 
│   │   │                                      Ind (short name for each isolate);   
│   │   │                                      conidL (conidial length in μm);
│   │   │                                      conidW (conidial width in μm); 
│   │   │                                      conidiophL (conidiophore length in μm);
│   │   │                                      conidiophW (conidiophore width in μm); 
│   │   │                                      conidA (conidial area in μm²). 
│   │   │
│   │   ├── alkaloids_qualitative.csv          # Dataset for qualitative detection, four alkaloid families (input script4.Rmd).
│   │   │                                      Presence indicated with "YES", traces with "TRACES" and absence with "NO".
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 25 correspond to chemical compounds tested.
│   │   │
│   │   ├── alkaloids_quantitative.csv         # Dataset for quantitative measurements, three alkaloid families.
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 6 correspond to compounds concentrations (units specified).
│   │   │   
│   │   ├── alkaloids_PCR.csv                  # PCR results for fungal genes in alkaloid synthesis (input script4.Rmd).
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
│   │                                          nucleids (number of particles counted, sample); 
│   │                                          nucleids_ST (number of particles counted, standard); 
│   │                                          mean (arithmetic mean of the fluorescence intensities, sample); 
│   │                                          mean_ST (arithmetic mean of the fluorescence intensities, standard);
│   │                                          CV (coefficient of Variation,sample); 
│   │                                          CV_ST (coefficient of Variation, standard);
│   │                                          pg/1C (estimated genome size, sample); 
│   │                                          pg/1C_ST (known genome size, standard);             
│   │
│   └── scripts/
│       ├── script1.Rmd                       # RMarkdown: Morphological analysis of fungal endophyte.
│       ├── script2.sh                        # Shell script: Phylogenetic inference using IQ-TREE2 and ASTRAL.
│       ├── script3.Rmd                       # Rmarkdown: Visualization and editing of phylogenetic trees.
│       └── script4.Rmd                       # RMarkdown: Generation of the alkaloids heatmap (raw figures).
└

```
