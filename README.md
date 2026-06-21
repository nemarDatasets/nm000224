# Imagined speech EEG dataset — short and long words (Nguyen et al. 2017)

## Overview

This dataset comprises preprocessed EEG recordings from 6 healthy participants performing imagined speech tasks, specifically discriminating between short and long words ('cooperate' vs 'in'). Data were acquired at 256 Hz using 64 EEG channels and processed with bandpass filtering (8-70 Hz), notch filtering (60 Hz), and artifact removal. The dataset contains 3,600 trials analyzed using Riemannian manifold and relevance vector machine approaches for brain-computer interface applications, achieving mean classification accuracy of 73.3±8.9%.

## Dataset Summary

| Property | Value |
|---|---|
| Subjects | 6 |
| Channels | 64 |
| Classes | 2 |
| Trial length | 5 s |
| Sampling frequency | 256 Hz |
| Sessions | 1 |
| Total trials | 1200 |
| Paradigm | MotorImagery |

## Data Collection Methods

EEG data were acquired using a BrainProducts ActiCHamp system at 256 Hz sampling rate with 64 channels (60 EEG, 4 EOG) in a standard 1020 montage. Participants performed imagined speech tasks cued by auditory beeps (5 beeps at 1.4 s rhythm) and visual cues, with 5-second analysis windows split into 3 overlapping 2-second epochs. Preprocessing included 5th-order Butterworth bandpass filtering (8-70 Hz), 60 Hz notch filtering, and adaptive EOG artifact removal.

## How to Access via MOABB

Install MOABB and load this dataset directly:

```python
from moabb.datasets import Nguyen2017_SL
from moabb.paradigms import MotorImagery
paradigm = MotorImagery()

dataset = Nguyen2017_SL()
X, y, metadata = paradigm.get_data(dataset)
```

For more details see the [MOABB documentation](https://moabb.neurotechx.com/) and the
[MOABB dataset page](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Nguyen2017_SL.html).

## Citation

If you use this dataset please cite the primary publication:

> DOI: [10.1088/1741-2552/aa8235](https://doi.org/10.1088/1741-2552/aa8235)

## NEMAR / MOABB Benchmark Collection

This BIDS-formatted dataset was converted from the original data using the
[MOABB](https://moabb.neurotechx.com/) pipeline and re-hosted on
[NEMAR](https://nemar.org/) as part of the MOABB benchmark collection.
The original data and license terms apply — see `dataset_description.json` for details.
