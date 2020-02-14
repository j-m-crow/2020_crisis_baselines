This directory files continaing relevant portions of CLT26 corresponding to the specific experiments conducted in the paper.

Files are named according to the specific configuration/strata, as follows:

`A_B_C_D_E_F_G.json`

- `A` => classification target
  - (`{Informativeness | Information Type | Crisis Category | Information Source}`)
- `B` => arity configuration 
  - (`binaryFalse` = multiclass config. ; `binaryTrue` = binary config.)
- `C` => class balancing configuration
  - (`balancedFalse` = imbalanced ; `balancedTrue` = balanced)
- `D` => original or rehydrated data
  - (`filteredFalse` = original data ; `filteredTrue` = rehydrated data)
- `E` => semantic concepts inclusion/exclusion
  - (`semanticConceptsTrue` = semantic concepts annotations included ; `semanticConceptsFalse` = semantic concepts excluded)
- F => fold number (corresponding to 5-fold CV used for all experiment configurations)
  - (`{0 | 1 | 2 | 3 | 4}`)
- G => train/validation/test per fold
  - (`{TRAIN | VALIDATION | TEST}`)
  
For example `Information Source_binaryTrue_balancedTrue_filteredTrue_semanticConceptsFalse_4_VALIDATION.json` is the validation set for 4th iteration of 5-fold CV, where the target is binarised, contains only tweets that were possible to rehydrate, is class balanced, and does not contain semantic concepts annotations.

All files contain Tweet-IDs for ease of cross-referencing with aggregate rehydrated data files, original CLT26 files, and original semantic annotation files.
  
Please refer to the paper for further details or contact the author for more information.