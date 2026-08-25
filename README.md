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
│                                              CV (coefficient of variation, sample); 
│                                              CV_ST (coefficient of variation, standard);
│                                              pg/2C (estimated genome size, sample); 
│                                              pg/2C_ST (known genome size, standard);
│
│
├── Fungal_endophyte/
│   ├── data/
│   │   ├── outputs_script_1/                  # Output files of the morphological analyses (from script_1.Rmd)
│   │   ├── outputs_script_2/                  # Phylogenetic trees and their support values files (from script_2.Rmd) 
│   │   ├── outputs_script_3/                  # Alkaloids heatmap, raw figures (from script3.Rmd)
│   │   ├── Phylogenetic_analysis/
│   │   │   │  
│   │   │   ├── MSA/                           # Multiple sequence alignments (FASTA format; input script_2.Rmd)
│   │   │   └── TREES/                         # Raw phylogenetic trees obtained from IQTREE and ASTRAL (input script_2.Rmd)
│   │   │   
│   │   ├── culture_growth_dataset.csv         # Dataset for culture growth rate analysis (input script_1.Rmd).
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: IndID (measurement identification code);
│   │   │                                      Ind (short name for each isolate);
│   │   │                                      Rep (replicate code within each isolate);
│   │   │                                      Day (day the measurement was made);
│   │   │                                      Diameter (diameter of the culture in mm)
│   │   │                                      Species (holobiont identification code).
│   │   │ 
│   │   ├── spores_dataset.csv                 # Morphometric data of asexual reproductive structures (input in script_1.Rmd). 
│   │   │                                      This file is semicolon-delimited and uses a comma as the decimal separator.
│   │   │                                      Variables: Species (holobiont identification code);
│   │   │                                      SampleID (measurement identification code); 
│   │   │                                      Ind (short name for each isolate);   
│   │   │                                      conidL (conidial length in μm);
│   │   │                                      conidW (conidial width in μm); 
│   │   │                                      conidiogL (conidiogenous cell length in μm);
│   │   │                                      conidiogW (conidiogenous cell basal width in μm); 
│   │   │                                      conidA (conidial area in μm²). 
│   │   │
│   │   ├── alkaloids_qualitative.csv          # Dataset for qualitative detection, four alkaloid families (input script_3.Rmd).
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
│   │   ├── alkaloids_PCR.csv                  # PCR results for fungal genes in alkaloid synthesis (input script_3.Rmd).
│   │   │                                      Presence indicated with "+" and absence indicated with "-".
│   │   │                                      Variables: Hostsp (holobiont identification code);
│   │   │                                      SampleID (Individual identification code);
│   │   │                                      E (Epichloë incidence in the individuals tested);
│   │   │                                      Columns 4 to 9 correspond to the key fungal genes tested.
│   │   │
│   │   ├── panelC_cultures.tiff               # Raw panel C from Figure 2; uploaded by script_1.Rmd
│   │   │  
│   │   └── flow_cytometry_endophyte.csv       # Genome size estimations of Epichloë festucae via flow cytometry.
│   │                                          Variables: Holobiont_ID (holobiont identification code);
│   │                                          Host_sp: (plant host species identification code); 
│   │                                          Measurement_ID (measurement identification code);
│   │                                          nucleids (number of particles counted, sample); 
│   │                                          nucleids_ST (number of particles counted, standard); 
│   │                                          mean (arithmetic mean of the fluorescence intensities, sample); 
│   │                                          mean_ST (arithmetic mean of the fluorescence intensities, standard);
│   │                                          CV (coefficient of variation,sample); 
│   │                                          CV_ST (coefficient of variation, standard);
│   │                                          pg/1C (estimated genome size, sample); 
│   │                                          pg/1C_ST (known genome size, standard);             
│   │
│   └── scripts/
│       ├── script_1.Rmd                       # RMarkdown: Morphological analysis of fungal endophytes.
│       ├── script_2.Rmd                       # Rmarkdown: Visualization and editing of phylogenetic trees.
│       └── script_3.Rmd                       # RMarkdown: Generation of the alkaloids heatmap figure.
└

```
