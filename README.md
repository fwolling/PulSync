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

<table>
  <thead>
    <tr><td></td><td>misalignment Δ</td><td></td><td>remaining error ε</td><td></td></tr>
    <tr><td>subject</td><td>mean</td><td>std</td><td>mean</td><td>std</td></tr>
  </thead>
  <tbody>
    <tr><td>01</td><td>0.6 s</td><td>±0.023 s</td><td>-3.856 ms</td><td>±23.287 ms</td></tr>
    <tr><td>02</td><td>-0.051 s</td><td>±0.023 s</td><td>-7.082 ms</td><td>±23.449 ms</td></tr>
    <tr><td>03</td><td>0.453 s</td><td>±0.011 s</td><td>-3.46 ms</td><td>±11.195 ms</td></tr>
    <tr><td>04</td><td>-0.363 s</td><td>±0.014 s</td><td>5.36 ms</td><td>±14.265 ms</td></tr>
    <tr><td>05</td><td>0.038 s</td><td>±0.017 s</td><td>2.487 ms</td><td>±17.075 ms</td></tr>
    <tr><td>06</td><td>-0.168 s</td><td>±0.009 s</td><td>-7.906 ms</td><td>±8.902 ms</td></tr>
    <tr><td>07</td><td>-0.375 s</td><td>±0.007 s</td><td>-7.414 ms</td><td>±7.361 ms</td></tr>
    <tr><td>08</td><td>0.327 s</td><td>±0.013 s</td><td>7.117 ms</td><td>±13.002 ms</td></tr>
    <tr><td>09</td><td>-3.393 s</td><td>±0.01 s</td><td>6.939 ms</td><td>±9.879 ms</td></tr>
    <tr><td>10</td><td>-3.493 s</td><td>±0.01 s</td><td>-12.445 ms</td><td>±10.223 ms</td></tr>
    <tr><td>11</td><td>-0.402 s</td><td>±0.004 s</td><td>-1.621 ms</td><td>±3.728 ms</td></tr>
    <tr><td>12</td><td>-0.491 s</td><td>±0.006 s</td><td>-11.187 ms</td><td>±5.55 ms</td></tr>
    <tr><td>13</td><td>1.401 s</td><td>±0.011 s</td><td>-2.915 ms</td><td>±10.56 ms</td></tr>
    <tr><td>14</td><td>3.216 s</td><td>±0.008 s</td><td>3.654 ms</td><td>±7.893 ms</td></tr>
    <tr><td>15</td><td>-0.397 s</td><td>±0.017 s</td><td>3.127 ms</td><td>±16.765 ms</td></tr>
    <tr><td>16</td><td>0.196 s</td><td>±0.015 s</td><td>-3.698 ms</td><td>±14.89 ms</td></tr>
    <tr><td>17</td><td>0.51 s</td><td>±0.006 s</td><td>-10.0 ms</td><td>±5.586 ms</td></tr>
    <tr><td>18</td><td>-0.083 s</td><td>±0.006 s</td><td>-2.676 ms</td><td>±5.521 ms</td></tr>
    <tr><td>19</td><td>4.969 s</td><td>±0.007 s</td><td>9.257 ms</td><td>±6.627 ms</td></tr>
    <tr><td>20</td><td>3.186 s</td><td>±0.008 s</td><td>1.945 ms</td><td>±8.233 ms</td></tr>
    <tr><td>21</td><td>-0.06 s</td><td>±0.002 s</td><td>-20.188 ms</td><td>±1.72 ms</td></tr>
    <tr><td>22</td><td>-0.163 s</td><td>±0.007 s</td><td>-3.329 ms</td><td>±6.952 ms</td></tr>
    <tr><td>23</td><td>-0.975 s</td><td>±0.007 s</td><td>-14.811 ms</td><td>±6.698 ms</td></tr>
    <tr><td>24</td><td>-1.833 s</td><td>±0.003 s</td><td>6.83 ms</td><td>±3.206 ms</td></tr>
    <tr><td>25</td><td>-0.553 s</td><td>±0.008 s</td><td>2.993 ms</td><td>±8.011 ms</td></tr>
  </tbody>
</table>

### References
<a id="ref_s01">**[1]:**</a> "[High precision ECG Database with annotated R peaks, recorded and filmed under realistic conditions](http://researchdata.gla.ac.uk/716/)", Luis Howell and Bernd Porr. University of Glasgow, 2018. <a href="http://dx.doi.org/10.5525/gla.researchdata.716" target="_blank">http://dx.doi.org/10.5525/gla.researchdata.716</a>
