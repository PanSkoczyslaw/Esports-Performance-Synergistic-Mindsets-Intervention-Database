# Esports-Performance-Synergistic-Mindsets-Intervention-Database

Database created for the scientific project "Esports Performance & Synergistic Mindsets Intervention" DOI: 10.17605/OSF.IO/4NZSV.
The data were collected from study participants. Each participant attended two laboratory sessions where their physiological parameters were measured during laboratory tasks. Subsequently, for two weeks, the participants received daily tasks to complete. After two weeks, they were invited to the second laboratory session, where their physiological parameters were measured again during a series of highly intensive and potentially stress-inducing tasks.

During the laboratory sessions, each participant was connected to three measurement devices:

-A device measuring heart-related parameters (VUAMS),
-A device for blood pressure measurement,
-Accelerometers placed on the dominant hand and legs to measure movement activity.
The data from each participant, each measurement device, and for each laboratory session were synchronized and merged into individual databases saved in CSV format. The raw files were recorded at different frequencies, and their durations varied. Blood pressure data files could not be synchronized using the time column and had to be merged based on the "marker" column, as these files were sourced from a separate computer that was not time-synchronized with the others.
The pipeline code for processing all files from session 1 is located in sync_merge_s1.ipynb, while the code for session 2 is in sync_merge_s2.ipynb.

Code for processing individual files that were unexpectedly skipped by the pipeline is available in the debugging files: individual_processing_debug_s1.ipynb and individual_processing_debug_s2.ipynb.

In the "Code" folder, there are also notebooks containing scripts to calculate means and standard deviations of physiological recordings for specific measurement moments, as well as overall means and standard deviations for each participant.
Additionally, the folder includes code to calculate the SNR (Signal-to-Noise Ratio) for individual data channels.
