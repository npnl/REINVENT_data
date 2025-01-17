# REINVENT data

This repository contains the data used in our papers:
* [A Virtual Reality Muscle–Computer Interface for Neurorehabilitation in Chronic Stroke: A Pilot Study](https://doi.org/10.3390/s20133754)
  * Available in [data](https://github.com/npnl/REINVENT_data/tree/master/data)
* [Coming Soon...](link)
  * Available in [Tele-REINVENT_data](https://github.com/npnl/REINVENT_data/tree/master/Tele-REINVENT_data)

# Notes

## Acquisition

Similar to our previous work (Vourvopoulos, A., et al., 2019) data was acquired using the [Labstreaming Layer](https://github.com/sccn/labstreaminglayer) protocol, and thus recorded as independent streams of data timestamped and saved as .xdf files.


## REINVENT

The folder _**data**_ contains .mat files that correspond to the extracted .xdf files after normalizing (downsampling or interpolating) all signals to a common sample rate of 1000 Hz.
Data was stored in individual files for each participant (_sXX_), during each session (_tXX_) and per block of trials.
E.g.: file _s03t04_block_5_ corresponds to Participant 3's fifth block of the fourth training session.

For all recordings, **EMG** electrodes were placed over:
* Flexor Carpi Radialis (FCR)
* Flexor Carpi Ulnaris (FCU)
* Extensor Carpi Radialis Longus (ECR)
* Extensor Carpi Ulnaris (ECU)

For the neuromuscular control task, **EEG** electrodes were placed following the 10-10 convention over:
* FC3
* FC4
* C3
* C4
* C5
* C6
* CP3
* CP4

### Neuromuscular control task

Files _sXXtXX_extension_X.mat_ and _sXXtXX_extension_X.mat_ contain a single _data_ structure with the following fields:
* **sampleRate** of 1000 Hz for all signals, except gripEMG
* **timeStamp** of each data point in seconds
* 4 channels of **EMG** data recorded from FCR, FCU, ECR, ECU
* 8 channels of **EEG** data recorded from FC3, FC4, C3, C4, C5, C6, CP3, CP4
* The **target** the participants were asked to follow
* The **error** = Expected position (target) - cursor position
* **gripEMG**: 4 channels of EMG recorded during the power grip.
  * Note that *gripEMG* was **not** downsampled. This field has a sample rate of 2000 Hz

### Traninng sessions

Files _sXXtXX_block_X.mat_ contain a single _data_ structure with the following fields:
* **sampleRate** of 1000 Hz for all signals, except gripEMG
* **timeStamp** of each data point in seconds
* 4 channels of **EMG** data recorded from FCR, FCU, ECR, ECU
* **markers** of events happening in the VR environment
* Current **trial** number
* Current block **score**
* **ERthreshold** used by the interface to calculate success
  * Note that for Participant 1, we did not have implemented the real-time recording of the threshold.
* **gripEMG**: 4 channels of EMG recorded during the power grip.
  * Note that _gripEMG_ was **not** downsampled. This field has a sample rate of 2000 Hz



## Tele-REINVENT

The folder _**Tele-REINVENT_data**_ contains .mat files that correspond to the extracted .xdf files after normalizing (downsampling or interpolating) all signals to a common sample rate of 1000 Hz.
Data was stored in individual files for each session.

For all recordings, **EMG** electrodes were placed over:
  * Wrist extensor muscle
  * Wrist flexor muscle

Files _session_X.mat_ contain a single _data_ structure with the following fields:
  * **session** number
  * **sampleRate** of 1000 Hz for all signals
  * **mvc** with the time and EMG signals during the recorded calibration
  * **time** of each data point in seconds
  * 2 channels of **EMG** data recorded from the extensor and flexor muscles
  * Current **trial** number


## Figures

The file _sensors2020data_ contains the processed data used to create the [figures and statistical comparisons](https://npnl.github.io/REINVENT_data) shown in Marin-Pardo et al., 2020.

The file _sensors2021data_ contains the processed data used to create the [figures and statistical comparisons](https://npnl.github.io/Tele-REINVENT_data) shown in Marin-Pardo et al., 2021.

# References

Vourvopoulos, A., Pardo, O. M., Lefebvre, S., Neureither, M., Saldana, D., Jahng, E., & Liew, S. L. (2019). Effects of a brain-computer interface with virtual reality (VR) neurofeedback: a pilot study in chronic stroke patients. Frontiers in human neuroscience, 13, 210.
[https://doi.org/10.3389/fnhum.2019.00210](https://doi.org/10.3389/fnhum.2019.00210)

Marin-Pardo, O., Laine, C. M., Rennie, M., Ito, K. L., Finley, J., & Liew, S. L. (2020). A Virtual Reality Muscle–Computer Interface for Neurorehabilitation in Chronic Stroke: A Pilot Study. Sensors, 20(13), 3754.
[https://doi.org/10.3390/s20133754](https://doi.org/10.3390/s20133754)

# License
