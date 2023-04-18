# REACT_Mapping
## <ins>Re</ins>petitive <ins>Act</ins>ivity (REACT) Mapping of Atrial Tachyarrhythmias
Repository contains codes to compute REACT maps from input electrgram signals. REACT mapping is a novel approach to identify islands with organized electrograms in atrial fibrillation.

Full paper: https://academic.oup.com/europace/advance-article/doi/10.1093/europace/euad055/7080278 

Last updated on 04/17/2023. New version has an option to run it in serial or parallel.

Code execution syntax: Generate_REACT_Map(offset, egmMat, rhythmType, CL, chamber, parallelProcessing)

offset: Basket catheter offset

egmMat: [time x 64] matrix of electrograms - consider truncating time to as less samples as possible (4000 samples takes ~20 sec in parallel mode)

rhythmType: 'AF' or 'AT'

CL: [1x64] Cycle length of each electrogram

Chamber: 1 for LA and 0 for RA

parallelProcessing: 1 for yes and 0 for no
