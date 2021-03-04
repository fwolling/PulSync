# PulSync
## PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices

<!--In this GitHub repository, we present an analytical tool for the quality review of raw photoplethysmography (PPG) signals, based on 7 multi-varied decision metrics. It has been applied in the review of 10 publicly available photoplethysmography datasets, referred below in [Citation](#citation). Although all [evaluated datasets](#evaluated-datasets) were advertised to contain raw signals, the characteristics of the PPG data look quite diverse. Our developed tool enables to automatically analyze the suitability and applicability of datasets and helps to identify preprocessed and filtered signals with a limited evidence. The [raw reference data](#reference-data), recorded with the MAX86140EVSYS# evaluation system, as well as the implemented [Python tool](/python/), based on the presented 7 decision metrics, are available for [download](#download), to support the reproducibility and the review of new datasets.-->

### Download
In this GitHub repository, we present *PulSync*, a tool for the data-driven offline alignment of sensor data across multiple devices utilizing the unique fingerprint-like character of the heart rate variability (HRV) interval function. The accuracy of the novel method has been evaluated on a dataset from 25 subjects and demonstrated the reliable alignment of independent electrocardiography (ECG) recordings with a mean accuracy of -0.71 ± 3.44 samples, respectively -2.86 ± 11.43 ms at 250 Hz sampling rate. The implemented [Python tool](/python/) is available for download, to support the reproducibility and the alignment of datasets.

### Citation
"[PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices](https://www.eti.uni-siegen.de/ubicomp/papers/ubi_perhealth2021.pdf)", <a href="https://ubicomp.eti.uni-siegen.de/home/team/fwolling.html.en" target="_blank">Florian Wolling</a>, <a href="https://ubicomp.eti.uni-siegen.de/home/team/kristof.html.en" target="_blank">Kristof Van Laerhoven</a>, <a href="https://www.oulu.fi/university/researcher/pekka-siirtola" target="_blank">Pekka Siirtola</a>, and <a href="https://www.oulu.fi/university/researcher/juha-roning" target="_blank">Juha Röning</a>. In *PerHealth 2021: 5th IEEE PerCom Workshop on Pervasive Health Technologies (PerHealth 2021)*, Virtual Event, IEEE, March 2021. <!--<a href="https://doi.org" target="_blank">https://doi.org</a>-->

### Disclaimer
You may use the source code of the developed synchronization tool *PulSync* for scientific, non-commercial purposes, provided that you give credit to the owners when publishing any work based on it. We would also be very interested to hear back from you if you use our tool or alignment method in any way and are happy to answer any questions or address any remarks related to it.

<!--### Presentation Video
<a href="https://www.youtube.com/watch?v=RshKMVtH7P0" target="_blank"><img src="https://raw.githubusercontent.com/fwolling/PPGraw/main/fig/youtube.png" alt="DATA'20 - The Quest for Raw Signals - A Quality Review of Photoplethysmography Datasets" width="600" style="float: center;" /></a>-->

### Applied Dataset
The *PulSync* processing pipeline has been evaluated using the dataset 716 of Howell and Porr from the University of Glasgow <a href="#ref_s01">**[1]**</a>. It contains ECG measurements from 25 subjects, recorded with two independent, pretended synchronous sensing devices in Einthoven II and resembled V2-V1 lead configurations. The "sitting" subset contains manually annotated peak labels with a precision of ±1 sample. Those were used to generate the heart rate variability (HRV) interval functions that are utilized to align the recordings.

### Results
| subject  | misalignment Δ   | remaining error ε   |
| -------: | ---------------: | ------------------: |
| 01       |  0.600 ± 0.023 s |  -3.856 ± 23.287 ms |
| 02       | -0.051 ± 0.023 s |  -7.082 ± 23.449 ms |
| 03       |  0.453 ± 0.011 s |  -3.460 ± 11.195 ms |
| 04       | -0.363 ± 0.014 s |   5.360 ± 14.265 ms |
| 05       |  0.038 ± 0.017 s |   2.487 ± 17.075 ms |
| 06       | -0.168 ± 0.009 s |  -7.906 ±  8.902 ms |
| 07       | -0.375 ± 0.007 s |  -7.414 ±  7.361 ms |
| 08       |  0.327 ± 0.013 s |   7.117 ± 13.002 ms |
| 09       | -3.393 ± 0.010 s |   6.939 ±  9.879 ms |
| 10       | -3.493 ± 0.010 s | -12.445 ± 10.223 ms |
| 11       | -0.402 ± 0.004 s |  -1.621 ±  3.728 ms |
| 12       | -0.491 ± 0.006 s | -11.187 ±  5.550 ms |
| 13       |  1.401 ± 0.011 s |  -2.915 ± 10.560 ms |
| 14       |  3.216 ± 0.008 s |   3.654 ±  7.893 ms |
| 15       | -0.397 ± 0.017 s |   3.127 ± 16.765 ms |
| 16       |  0.196 ± 0.015 s |  -3.698 ± 14.890 ms |
| 17       |  0.510 ± 0.006 s | -10.000 ±  5.586 ms |
| 18       | -0.083 ± 0.006 s |  -2.676 ±  5.521 ms |
| 19       |  4.969 ± 0.007 s |   9.257 ±  6.627 ms |
| 20       |  3.186 ± 0.008 s |   1.945 ±  8.233 ms |
| 21       | -0.060 ± 0.002 s | -20.188 ±  1.720 ms |
| 22       | -0.163 ± 0.007 s |  -3.329 ±  6.952 ms |
| 23       | -0.975 ± 0.007 s | -14.811 ±  6.698 ms |
| 24       | -1.833 ± 0.003 s |   6.830 ±  3.206 ms |
| 25       | -0.553 ± 0.008 s |   2.993 ±  8.011 ms |

### References
<a id="ref_s01">**[1]:**</a> "[High precision ECG Database with annotated R peaks, recorded and filmed under realistic conditions](http://researchdata.gla.ac.uk/716/)", Luis Howell and Bernd Porr. University of Glasgow, 2018. <a href="http://dx.doi.org/10.5525/gla.researchdata.716" target="_blank">http://dx.doi.org/10.5525/gla.researchdata.716</a>
