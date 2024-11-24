# Esports-Performance-Synergistic-Mindsets-Intervention-Database
**https://osf.io/4nzsv/**
Database created for the scientific project **"Esports Performance & Synergistic Mindsets Intervention"**  
DOI: [10.17605/OSF.IO/4NZSV](https://doi.org/10.17605/OSF.IO/4NZSV).

The data were collected from study participants. Each participant attended two laboratory sessions where their physiological parameters were measured during laboratory tasks. Subsequently, for two weeks, the participants received daily tasks to complete. After two weeks, they were invited to the second laboratory session, where their physiological parameters were measured again during a series of highly intensive and potentially stress-inducing tasks.

## Measurement Setup

During the laboratory sessions, each participant was connected to three measurement devices:
- **A device measuring heart-related parameters (VUAMS)**  
- **A device for blood pressure measurement**  
- **Accelerometers placed on the dominant hand and legs to measure movement activity**

## Data Processing

The data from each participant, each measurement device, and for each laboratory session were synchronized and merged into individual databases saved in CSV format.  
- Raw files were recorded at different frequencies, and their durations varied.
- Blood pressure data files could not be synchronized using the time column and had to be merged based on the "marker" column, as these files were sourced from a separate computer that was not time-synchronized with the others.  

### Processing Pipelines

- **Session 1**: Pipeline code is located in `sync_merge_s1.ipynb`  
- **Session 2**: Pipeline code is located in `sync_merge_s2.ipynb`

### Debugging

Code for processing individual files that were unexpectedly skipped by the pipeline is available in the debugging files:
- `individual_processing_debug_s1.ipynb`  
- `individual_processing_debug_s2.ipynb`

## Additional Scripts

In the `Code` folder, there are also notebooks containing scripts to:
- Calculate means and standard deviations of physiological recordings for specific measurement moments
- Calculate overall means and standard deviations for each participant
- Calculate the SNR (Signal-to-Noise Ratio) for individual data channels
