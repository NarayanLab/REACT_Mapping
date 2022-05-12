# REACT_Mapping
## <ins>Re</ins>petitive <ins>Act</ins>ivity (REACT) Mapping of Atrial Tachyarrhythmias
Repository contains codes to compute REACT maps from input electrgram signals. REACT mapping is a novel approach to identify islands with organized electrograms in atrial fibrillation.

DETAILED README IN PROGRESS..

Code execution syntax: Generate_REACT_Map(offset, egmMat, rhythmType, CL, chamber)

offset: Basket catheter offset

egmMat: [time x 64] matrix of electrograms

rhythmType: 'AF' or 'AT'

CL: Cycle length value

Chamber: 1 for LA and 0 for RA
