# PulSync
## PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices

<!--In this GitHub repository, we present an analytical tool for the quality review of raw photoplethysmography (PPG) signals, based on 7 multi-varied decision metrics. It has been applied in the review of 10 publicly available photoplethysmography datasets, referred below in [Citation](#citation). Although all [evaluated datasets](#evaluated-datasets) were advertised to contain raw signals, the characteristics of the PPG data look quite diverse. Our developed tool enables to automatically analyze the suitability and applicability of datasets and helps to identify preprocessed and filtered signals with a limited evidence. The [raw reference data](#reference-data), recorded with the MAX86140EVSYS# evaluation system, as well as the implemented [Python tool](/python/), based on the presented 7 decision metrics, are available for [download](#download), to support the reproducibility and the review of new datasets.-->

### Download
This GitHub repository provides the developed tool *PulSync*.
<!--The raw photoplethysmography reference signals can be downloaded via the following link:
https://ubicomp.eti.uni-siegen.de/home/datasets/data20/index.html.en-->

### Citation
"[PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices](https://www.eti.uni-siegen.de/ubicomp/papers/ubi_perhealth2021.pdf)", <a href="https://ubicomp.eti.uni-siegen.de/home/team/fwolling.html.en" target="_blank">Florian Wolling</a>, <a href="https://ubicomp.eti.uni-siegen.de/home/team/kristof.html.en" target="_blank">Kristof Van Laerhoven</a>, <a href="https://www.oulu.fi/university/researcher/pekka-siirtola" target="_blank">Pekka Siirtola</a>, and <a href="https://www.oulu.fi/university/researcher/juha-roning" target="_blank">Juha Röning</a>. In *PerHealth 2021: 5th IEEE PerCom Workshop on Pervasive Health Technologies (PerHealth 2021)*, Virtual Event, IEEE, March 2021. <!--<a href="https://doi.org" target="_blank">https://doi.org</a>-->

### Disclaimer
You may use the source code of the developed synchronization tool *PulSync* for scientific, non-commercial purposes, provided that you give credit to the owners when publishing any work based on it. We would also be very interested to hear back from you if you use our tool or alignment method in any way and are happy to answer any questions or address any remarks related to it.

<!--### Presentation Video
<a href="https://www.youtube.com/watch?v=RshKMVtH7P0" target="_blank"><img src="https://raw.githubusercontent.com/fwolling/PPGraw/main/fig/youtube.png" alt="DATA'20 - The Quest for Raw Signals - A Quality Review of Photoplethysmography Datasets" width="600" style="float: center;" /></a>-->

### Applied Dataset
The *PulSync* processing pipeline has been evaluated using the dataset 716 of Howell and Porr from the University of Glasgow. It contains ECG measurements from 25 subjects, recorded with two independent, pretended synchronous sensing devices in Einthoven II and resembled V2-V1 lead configurations. The "sitting" subset contains manually annotated peak labels with a precision of ±1 sample. Those were used to generate the heart rate variability (HRV) interval functions that are utilized to align the recordings.

"[High precision ECG Database with annotated R peaks, recorded and filmed under realistic conditions](http://researchdata.gla.ac.uk/716/)", Luis Howell and Bernd Porr. University of Glasgow, 2018. <a href="http://dx.doi.org/10.5525/gla.researchdata.716" target="_blank">http://dx.doi.org/10.5525/gla.researchdata.716</a>

### Results
