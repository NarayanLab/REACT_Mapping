# REACT_Mapping
## <ins>Re</ins>petitive <ins>Act</ins>ivity (REACT) Mapping of Atrial Tachyarrhythmias
Repository contains codes to compute REACT maps from input electrgram signals. REACT mapping is a novel approach to identify islands with organized electrograms in atrial fibrillation.

### Full paper: https://academic.oup.com/europace/advance-article/doi/10.1093/europace/euad055/7080278 

Update on 04/17/2023: New version has an option to run it in serial or parallel.

Update on 07/15/2023: Option to automatically calculate cycle length (algorithm uses autocorrelation)

### Code execution syntax: 

Generate_REACT_Map(offset, egmMat, rhythmType, CL, chamber, parallelProcessing, tsegment)

offset: Basket catheter spline offset ('A' or 'B' or 'C' or...'H'). 

egmMat: [time x 64] matrix of electrograms - *consider truncating time to as less samples as possible for better execution speed*

rhythmType: 'AF' or 'AT'

CL: [1x64] Cycle length of each electrogram. If CL is unknown, then leave it empty, i.e. [], to automatically calculate it.

Chamber: 1 for LA and 0 for RA

parallelProcessing: 1 for yes and 0 for no

tsegment: timesamples range

Example usage: Generate_REACT_Map_Grid('A', EGM(100:3400), 'AF', [], 1, 1, 100:3400)

![Picture1](https://github.com/NarayanLab/REACT_Mapping/assets/69654253/8dbf1025-05a5-4d99-87f3-67b895bb1a92)

