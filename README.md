# REINVENT data

This repository contains the data used in our paper [A Virtual Reality Muscle-Computer-Interface for Neurorehabilitation in
Chronic Stroke: A Pilot Study](link)

# Notes

## Acquisition

Similar to our previous work (Vourvopoulos et al.) data was acquired using the [Labstreaming Layer](https://github.com/sccn/labstreaminglayer) protocol, and thus recorded as independent streams of data timestamped and saved as .xdf files.

## Data

The folder *data* contains .mat files that correspond to the extracted .xdf files after normalizing all signals to a common sample rate of 1000 Hz. Data was stored in individual files for each participant (_sXX_), during each session (_tXX_) and per block of trials. E.g.: file _s03t04_block_5_ corresponds to Participant 3's fifth block of the fourth training session.

Files _sXXtXX_extension_X.mat_ and _sXXtXX_extension_X.mat_ contain...

Files _sXXtXX_block_X.mat_ contain...

## Figures

The file _sensors2020data_ contains the processed data used to create the [figures and statistical comparisons](https://npnl.github.io/REINVENT_data) shown in Marin-Pardo et al.

# References

Vourvopoulos, A., Pardo, O. M., Lefebvre, S., Neureither, M., Saldana, D., Jahng, E., & Liew, S. L. (2019). Effects of a brain-computer interface with virtual reality (VR) neurofeedback: a pilot study in chronic stroke patients. Frontiers in human neuroscience, 13, 210.
[https://doi.org/10.3389/fnhum.2019.00210](https://doi.org/10.3389/fnhum.2019.00210)

[Octavio paper](link)

# License
