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

## Comparison of timings and orbital space sizes for each freezing scheme
 *Timings are in minutes*

#### frozen_core

| Basis               | Nmo/pi              | nfrozen/pi          | nactive/pi          | nmo        | nfrozen    | nactive    | timing     |
| :-----------------: | :-----------------: | :-----------------: | :-----------------: | :--------: | :--------: | :--------: | :--------: |
| **6-31Gs**          | `[ 89, 23, 29, 72]` | `[  8,  0,  0,  5]` | `[ 81, 23, 29, 67]` | 213        | 13         | 200        | 78.78      |
| **6-31G**           | `[ 60, 10, 16, 49]` | `[  8,  0,  0,  5]` | `[ 52, 10, 16, 44]` | 135        | 13         | 122        | 12.22      |
| **6-311G(2d)**      | `[128, 41, 50,107]` | `[  8,  0,  0,  5]` | `[120, 41, 50,102]` | 326        | 13         | 313        | 316.92     |

#### frozen_sigma_ov_active_match

|       Basis       |      Nmo/pi       |    nfrozen/pi     |    nactive/pi     |   nmo    | nfrozen  | nactive  |  timing  |
|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:--------:|:--------:|:--------:|:--------:|
|    **6-31Gs**     |`[ 89, 23, 29, 72]`|`[ 89, 17, 21, 72]`|`[  0,  6,  8,  0]`|   213    |   199    |    14    |   2.28   |
|     **6-31G**     |`[ 60, 10, 16, 49]`|`[ 60,  4,  8, 49]`|`[  0,  6,  8,  0]`|   135    |   121    |    14    |   0.68   |
|  **6-311G(2d)**   |`[128, 41, 50,107]`|`[128, 35, 42,107]`|`[  0,  6,  8,  0]`|   326    |   312    |    14    |   9.50   |



#### frozen_sigma_ov_frozen_match

|       Basis       |      Nmo/pi       |    nfrozen/pi     |    nactive/pi     |   nmo    | nfrozen  | nactive  |  timing  |
|:-----------------:|:-----------------:|:-----------------:|:-----------------:|:--------:|:--------:|:--------:|:--------:|
|    **6-31Gs**     |`[ 89, 23, 29, 72]`|`[ 42,  0,  0, 32]`|`[ 47, 23, 29, 40]`|   213    |    74    |   139    |   4.55   |
|     **6-31G**     |`[ 60, 10, 16, 49]`|`[ 42,  0,  0, 32]`|`[ 18, 10, 16, 17]`|   135    |    74    |    61    |   0.92   |
|  **6-311G(2d)**   |`[128, 41, 50,107]`|`[ 42,  0,  0, 32]`|`[ 86, 41, 50, 75]`|   326    |    74    |   252    |  49.30   |



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
