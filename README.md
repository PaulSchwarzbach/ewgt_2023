# EWGT 2023
Dataset for the Paper entitled "Simulation-based Evaluation and Integration of Indoor Positioning Systems in Connected Aircraft Cabins"

# Descriptor

The dataset consist of three .csv files containing the visibility analysis from ray launching, the anchor states and the results of the probabilistic range sampling. The file `visibility.csv` contain visibility states inside a grid with resolution of 10cm of the two simulated heights in the cabin. The columns of the file include the following data:

* `x`: position of the predicted grid cell in x.
* `y`: position of the predicted grid cell in y.
* `height`: height of the simulated prediction plane. Is used to investigate the viability of the tag for two different height in the cabin.
* `anchor_id`: ID of the anchor for which the visibility is specified.
* `visibility`: computed visibility state (`LOS=1/OLOS=2/NLOS=3`) based on the radio propagation simulation with ray launching.


The second .csv file includes the sampled ranges based on the observability and is named `ranges.csv`. Each line of the file contains the following data:

*  `ref_pos_x`: static reference position of the passenger in x.
*  `ref_pos_y`: static reference position of the passenger in y.
*  `height`: height of the used prediction plane.
*  `anchor_id`: ID of the anchor for which the range is sampled.
*  `range`: sampled range between the anchor and the tag at the passenger. This range is used in the localization module to estimate the position of the passenger based on the simulated radio channel characteristics and visibility state from the radio propagation simulation.
