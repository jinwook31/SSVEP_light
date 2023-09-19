# SSVEP_Light Dataset

This project is the repository for a project that classifies EEG signals for three visual stimuli. This repository provides information on models, datasets, and visualization related to the project.

### Preprocessing

```
pip install -e .
cd preprocessor
python run.py
```

### Run Machine Learning

```
cd ssvl/svm
python run.py --platform Sc
python run.py --platform VR
```

### Dataset

This is an EEG signal dataset collected when 11 subjects were exposed to stimuli for approximately 4 seconds. We collected information from two platforms: VR and SC. It is a dataset that includes EEG stimuli from a total of 6 channels-`occipital lobe`, `partietal lobe` (Oz, O1, O2, Pz, P3, P4).

- Metadata 
    - area: All [default, 6 channel O+P], O (O Channels, 3), P (P Channels, 3)
    - platform: Sc (Screen, Traditional with High Acc), VR (Peripheral, Novel approach with weak stimuli than Sc)
    - pid: ['P02', 'P01', 'P04', 'P05', 'P06', 'P07', 'P08', 'P09', 'P10', 'P11', 'P12']

- Data Shape: Label x Trial (30) x Channel (6) x Sample (4sec)
    - Labels: 3 class light hz, {7, 10, 12}
    - Trial: 30 (data split by train: 24, valid: 3, test: 3)
    - Channel: 6 channels-`occipital lobe`, `partietal lobe`
    - Sapmle: 1025 (256 sampline rate x 4 second)

### Visualization

- check `notebook`