# PulSync
## PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices

### Download
In this GitHub repository, we present *PulSync*, a tool for the data-driven offline alignment of sensor data across multiple devices utilizing the unique fingerprint-like character of the heart rate variability (HRV) interval function. The accuracy of the novel method has been evaluated on a dataset from 25 subjects <a href="#ref_s01"><b>[1]</b></a> and demonstrated the reliable alignment of independent electrocardiography (ECG) recordings with a mean accuracy of -0.71 ± 3.44 samples, respectively -2.86 ± 11.43 ms at 250 Hz sampling rate. The implemented [Python tool](/src/) is available for download, to support the reproducibility as well as the alignment of datasets from unsynchronized in-the-wild recordings. The [Jupyter notebook](/src/example_ecg.ipynb) demonstrates the use of the *PulSync* [Python tool](/src/) on the example of the ECG recordings and R peak labels from subject 23, exemplarily prepared as a [Pickle file](/src/gla716_sub23.p).

### Citation
"[PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices](https://www.eti.uni-siegen.de/ubicomp/papers/ubi_percomws21b.pdf)", <a href="https://ubicomp.eti.uni-siegen.de/home/team/fwolling.html.en" target="_blank">Florian Wolling</a>, <a href="https://ubicomp.eti.uni-siegen.de/home/team/kristof.html.en" target="_blank">Kristof Van Laerhoven</a>, <a href="https://www.oulu.fi/university/researcher/pekka-siirtola" target="_blank">Pekka Siirtola</a>, and <a href="https://www.oulu.fi/university/researcher/juha-roning" target="_blank">Juha Röning</a>. In *PerHealth 2021: 5th IEEE PerCom Workshop on Pervasive Health Technologies (PerHealth 2021)*, Virtual Event, IEEE, March 2021. <!--<a href="https://doi.org" target="_blank">https://doi.org</a>-->

### Disclaimer
You may use the source code of the developed synchronization tool *PulSync* for scientific, non-commercial purposes, provided that you give credit to the owners when publishing any work based on it. We would also be very interested to hear back from you if you use our tool or alignment method in any way and are happy to answer any questions or address any remarks related to it.

### Teaser Video
The 1-minute teaser for the [PerHealth'21](https://sites.google.com/view/perhealth2021/) workshop can be found on [YouTube](https://www.youtube.com/watch?v=TENI1LUWinA).

<a href="https://www.youtube.com/watch?v=TENI1LUWinA" target="_blank"><img src="https://raw.githubusercontent.com/fwolling/PulSync/main/fig/youtube_teaser.png" alt="PerHealth'21 Teaser - PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices" width="600" style="float: center;" /></a>

### Full Presentation Video
The full 15-minute presentation for the [PerHealth'21](https://sites.google.com/view/perhealth2021/) workshop can be found on [YouTube](https://www.youtube.com/watch?v=QiZApuLrRic), as well.

<a href="https://www.youtube.com/watch?v=QiZApuLrRic" target="_blank"><img src="https://raw.githubusercontent.com/fwolling/PulSync/main/fig/youtube_full.png" alt="PerHealth'21 Full Presentation - PulSync: The Heart Rate Variability as a Unique Fingerprint for the Alignment of Sensor Data Across Multiple Wearable Devices" width="600" style="float: center;" /></a>

### Applied Dataset
The *PulSync* processing pipeline has been evaluated using the dataset 716 of Howell and Porr from the University of Glasgow <a href="#ref_s01">**[1]**</a>. It contains ECG measurements from 25 subjects, recorded with two independent, pretended synchronous sensing devices in Einthoven II and resembled V2-V1 lead configurations. The "sitting" subset contains manually annotated peak labels with a precision of ±1 sample. Those were used to generate the heart rate variability (HRV) interval functions that are utilized to align the recordings.

### Results
The evaluation of the data-driven alignment method *PulSync* resulted in a promising accuracy of -0.71 ± 3.44 samples, respectively -2.86 ± 11.43 ms at a sampling rate of 250 Hz and with the HRV interval functions resampled at 25 Hz. The initial misalignment of the original recordings was determined with a mean of 15.328 ± 428.023 samples, 0.061 ± 1.712 s respectively. The smallest initial misalignment was present in the recordings of subject 5 with 0.038 s, while subject 19 showed the largest offset of even 4.969 s.

<table>
  <thead>
    <tr align="right"><th></th><th></th><th colspan="2">alignment error ε</th></tr>
    <tr align="right"><th>subject</th><th>original misalignment Δ</th><th>mean</th><th>std</th></tr>
  </thead>
  <tbody>
    <tr align="right"><td>01</td><td>600.164 ms</td><td>-3.856 ms</td><td>±23.287 ms</td></tr>
    <tr align="right"><td>02</td><td>-51.084 ms</td><td>-7.082 ms</td><td>±23.449 ms</td></tr>
    <tr align="right"><td>03</td><td>452.556 ms</td><td>-3.460 ms</td><td>±11.195 ms</td></tr>
    <tr align="right"><td>04</td><td>-362.652 ms</td><td>5.360 ms</td><td>±14.265 ms</td></tr>
    <tr align="right"><td>05</td><td><b>38.488 ms</b></td><td>2.487 ms</td><td>±17.075 ms</td></tr>
    <tr align="right"><td>06</td><td>-167.911 ms</td><td>-7.906 ms</td><td>±8.902 ms</td></tr>
    <tr align="right"><td>07</td><td>-375.427 ms</td><td>-7.414 ms</td><td>±7.361 ms</td></tr>
    <tr align="right"><td>08</td><td>327.127 ms</td><td>7.117 ms</td><td>±13.002 ms</td></tr>
    <tr align="right"><td>09</td><td>-3393.174 ms</td><td>6.939 ms</td><td>±9.879 ms</td></tr>
    <tr align="right"><td>10</td><td>-3492.561 ms</td><td>-12.445 ms</td><td>±10.223 ms</td></tr>
    <tr align="right"><td>11</td><td>-401.634 ms</td><td><b>-1.621 ms</b></td><td>±3.728 ms</td></tr>
    <tr align="right"><td>12</td><td>-491.203 ms</td><td>-11.187 ms</td><td>±5.550 ms</td></tr>
    <tr align="right"><td>13</td><td>1401.131 ms</td><td>-2.915 ms</td><td>±10.560 ms</td></tr>
    <tr align="right"><td>14</td><td>3215.762 ms</td><td>3.654 ms</td><td>±7.893 ms</td></tr>
    <tr align="right"><td>15</td><td>-396.886 ms</td><td>3.127 ms</td><td>±16.765 ms</td></tr>
    <tr align="right"><td>16</td><td>196.308 ms</td><td>-3.698 ms</td><td>±14.890 ms</td></tr>
    <tr align="right"><td>17</td><td>510.017 ms</td><td>-10.000 ms</td><td>±5.586 ms</td></tr>
    <tr align="right"><td>18</td><td>-82.679 ms</td><td>-2.676 ms</td><td>±5.521 ms</td></tr>
    <tr align="right"><td>19</td><td><b>4969.422 ms</b></td><td>9.257 ms</td><td>±6.627 ms</td></tr>
    <tr align="right"><td>20</td><td>3186.051 ms</td><td>1.945 ms</td><td>±8.233 ms</td></tr>
    <tr align="right"><td>21</td><td>-60.189 ms</td><td><b>-20.188 ms</b></td><td>±1.720 ms</td></tr>
    <tr align="right"><td>22</td><td>-163.334 ms</td><td>-3.329 ms</td><td>±6.952 ms</td></tr>
    <tr align="right"><td>23</td><td>-974.843 ms</td><td>-14.811 ms</td><td>±6.698 ms</td></tr>
    <tr align="right"><td>24</td><td>-1833.231 ms</td><td>6.830 ms</td><td>±3.206 ms</td></tr>
    <tr align="right"><td>25</td><td>-553.026 ms</td><td>2.993 ms</td><td>±8.011 ms</td></tr>
  </tbody>
</table>

### References
<a id="ref_s01"><b>[1]:</b></a> "[High precision ECG Database with annotated R peaks, recorded and filmed under realistic conditions](http://researchdata.gla.ac.uk/716/)", Luis Howell and Bernd Porr. University of Glasgow, 2018. <a href="http://dx.doi.org/10.5525/gla.researchdata.716" target="_blank">http://dx.doi.org/10.5525/gla.researchdata.716</a>
