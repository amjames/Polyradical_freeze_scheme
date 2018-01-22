# Polyradicals: comparison of freezing schemes for (1)

## Comparison of various freezing schemes
#### frozen_core
 Here I have used the option `freeze_core = True` in all psi4 calculations.

#### frozen_sigma_ov_frozen_match
 Here I have frozen all sigma occupied orbitals, keeping only occupied orbitals in irreps `A2` and `B1` active.
 The frozen virtual orbitals have been selected so that the number of frozen virtual orbitals is the 
 same as the number of frozen occupied orbitals in each irrep. The options pertaining to orbital freezing used for each 
 calculation are listed below for each basis.

 **6-31G**

 |option       | value          |
 |:-----------:|:--------------:|
 |`FROZEN_DOCC`|`[21, 0, 0,16]` |
 |`DOCC`       |`[21, 2, 4,16]` |
 |`FROZEN_UOCC`|`[21, 0, 0,16]` |
 |`SOCC`       |`[ 0, 1, 0, 0]` |

 **6-31Gs**

 |option       | value         |
 |:-----------:|:-------------:|
 |`FROZEN_DOCC`|`[21, 0, 0,16]`|
 |`DOCC`       |`[21, 2, 4,16]`|
 |`FROZEN_UOCC`|`[21, 0, 0,16]`|
 |`SOCC`       |`[ 0, 1, 0, 0]`|

 **6-311G(2d)**

 |option       | value         |
 |:-----------:|:-------------:|
 |`FROZEN_DOCC`|`[21, 0, 0,16]`|
 |`DOCC`       |`[21, 2, 4,16]`|
 |`FROZEN_UOCC`|`[21, 0, 0,16]`|
 |`SOCC`       |`[ 0, 1, 0, 0]`|

#### frozen_sigma_ov_active_match
 Here I have frozen all sigma occupied orbitals, keeping only occupied orbitals in irreps `A2` and `B1` active.
 The frozen virtual orbitals have been selected so that the number of active virtual orbitals is the 
 same as the number of active occupied orbitals in each irrep. The options pertaining to orbital freezing used for each 
 calculation are listed below for each basis.

 **6-31G**

 |option       | value         |
 |:-----------:|:-------------:|
 |`FROZEN_DOCC`|`[21, 0, 0,16]`|
 |`DOCC`       |`[21, 2, 4,16]`|
 |`FROZEN_UOCC`|`[39, 4, 8,33]`|
 |`SOCC`       |`[ 0, 1, 0, 0]`|

 **6-31Gs**

 |option       | value         |
 |:-----------:|:-------------:|
 |`FROZEN_DOCC`|`[21, 0, 0,16]`|
 |`DOCC`       |`[21, 2, 4,16]`|
 |`FROZEN_UOCC`|`[68,17,21,56]`|
 |`SOCC`       |`[ 0, 1, 0, 0]`|

 **6-311G(2d)**

 |option       | value          |
 |:-----------:|:--------------:|
 |`FROZEN_DOCC`|`[ 21, 0, 0,16]`|
 |`DOCC`       |`[ 21, 2, 4,16]`|
 |`FROZEN_UOCC`|`[107,35,42,91]`|
 |`SOCC`       |`[  0, 1, 0, 0]`|


## Output files
#### frozen_core
   - [mol1/6-311G(2d)](frozen_core_mol1_6-311G_2d_outfile.txt)
   - [mol1/6-31Gs](frozen_core_mol1_6-31Gs_outfile.txt)
   - [mol1/6-31G](frozen_core_mol1_6-31G_outfile.txt)
#### frozen_sigma_ov_frozen_match
   - [mol1/6-311G(2d)](frozen_sigma_ov_frozen_match_mol1_6-311G_2d_outfile.txt)
   - [mol1/6-31Gs](frozen_sigma_ov_frozen_match_mol1_6-31Gs_outfile.txt)
   - [mol1/6-31G](frozen_sigma_ov_frozen_match_mol1_6-31G_outfile.txt)
#### frozen_sigma_ov_active_match
   - [mol1/6-31Gs](frozen_sigma_ov_active_match_mol1_6-31Gs_outfile.txt)
   - [mol1/6-311G(2d)](frozen_sigma_ov_active_match_mol1_6-311G_2d_outfile.txt)
   - [mol1/6-31G](frozen_sigma_ov_active_match_mol1_6-31G_outfile.txt)
