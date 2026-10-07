---
layout: default  # Or another layout if you have one
title: Overview
permalink: /overview/ 
---
<style>
.wrapper { max-width: 1200px; padding-left: 24px; padding-right: 24px; }
</style>

We collected the on-road data during September 2023 in Rosyth, Queensferry and Penicuik near Edinburgh, Scotland.
Foggy data was collected first, and the counterpart clear data in overcast weather was collected two weeks later by traversing the same routes.

<a id="data-episodes-and-sequences"></a>

# Data episodes and sequences
In total, 52 data **episodes**, consisting of 103 data **sequences**, were collected.
Apart from only one episode (`R00`, last row of the table below) that contains only a foggy sequence, each of the remaining 51 episodes comprise a **foggy** sequence and a *counterpart* **clear** sequence of the same route.
The total duration of the foggy and the clear videos are 2578 seconds and 2443 seconds, respectively.

Further, by visually examining the foggy images, we subjectively classify the 52 foggy sequences into **thin** fog (20 sequences totalling 1101 seconds) and **thick** fog (32 sequences totalling 1477 seconds).

In the following table we show the details of each data episode in SDIRF, including the scene, the weather condition, the start time, and the duration.
We also show the camera's gain and the exposure settings of each sequence.
For each combination of gain and exposure settings, we conducted a [photometric calibration]({{ site.baseurl }}/photometric_calibration/) in a controlled environment.

<!-- <!DOCTYPE html> -->
<!-- <html lang="en"> -->
<!-- <head> -->
<!-- <meta charset="UTF-8"> -->
<!-- <title>Fog Dataset Project Page</title> -->

<style>

/* body{
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Arial;
    margin:0;
    background:#fafafa;
    color:#333;
} */

/* .container{
    width:1100px;
    margin:auto;
    padding:40px;
} */

/* h1{
    text-align:center;
} */

/* .section{
    margin-top:50px;
} */

/* .table-container{
    overflow-x:auto;
} */

/* table{
    border-collapse:collapse;
    width:100%;
    background:white;
    box-shadow:0 3px 12px rgba(0,0,0,0.06);
} */

th,td{
    border:1px solid #ddd;
    padding:7px;
    font-size:14px;
    text-align:center;
}

.sequence-thumb {
    width: 150px;
    height: auto;
    display: block;
    margin: 0 auto;
    border: 1px solid #ddd;
    border-radius: 4px;
    background: #fafafa;
}

.sequence-thumb-table {
    table-layout: fixed;
    width: 100%;
}

.sequence-thumb-table th:nth-child(1),
.sequence-thumb-table td:nth-child(1),
.sequence-thumb-table th:nth-child(2),
.sequence-thumb-table td:nth-child(2),
.sequence-thumb-table th:nth-child(3),
.sequence-thumb-table td:nth-child(3) {
    width: 12%;
    min-width: 70px;
}

.sequence-thumb-table th:nth-child(4),
.sequence-thumb-table td:nth-child(4),
.sequence-thumb-table th:nth-child(5),
.sequence-thumb-table td:nth-child(5) {
    width: 32%;
}

/* thead{
    background:#f2f2f2;
} */

/* tbody tr:nth-child(even){
    background:#fafafa;
} */

/* tbody tr:hover{
    background:#eef5ff;
} */

/* td.scene{
    text-align:left;
} */

</style>
<!-- </head> -->


<!-- <body> -->

<!-- <div class="container"> -->

<!-- <h1>Fog Dataset Sequences</h1> -->

<!-- <div class="section"> -->
<!-- <h2>Dataset Sequences</h2> -->

<!-- <div class="table-container"> -->

<table>

<thead>

<tr>
<th rowspan="3">Episode</th>
<th rowspan="3">Scene</th>
<th colspan="9">Sequence</th>
</tr>

<tr>
<th colspan="5">Foggy</th>
<th colspan="4">Overcast</th>
</tr>

<tr>
<th>Fog density</th>
<th>Start date and time</th>
<th>Duration (s)</th>
<th>Gain</th>
<th>Exposure</th>
<th>Start date and time</th>
<th>Duration (s)</th>
<th>Gain</th>
<th>Exposure</th>
</tr>

</thead>

<tbody>

<tr><td>P00</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:52:14</td><td>49.1</td><td>5</td><td>10</td><td>22 Sep 2023 13:15:07</td><td>42.3</td><td>0</td><td>1</td></tr>
<tr><td>P01</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:53:37</td><td>62.5</td><td>5</td><td>10</td><td>22 Sep 2023 13:17:44</td><td>44.7</td><td>0</td><td>1</td></tr>
<tr><td>P02</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:54:53</td><td>42.9</td><td>5</td><td>10</td><td>22 Sep 2023 13:18:45</td><td>35.7</td><td>0</td><td>1</td></tr>
<tr><td>P03</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:56:14</td><td>10.9</td><td>5</td><td>10</td><td>22 Sep 2023 13:19:58</td><td>9.9</td><td>0</td><td>1</td></tr>
<tr><td>P04</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:56:31</td><td>68.7</td><td>5</td><td>10</td><td>22 Sep 2023 13:20:15</td><td>61.0</td><td>0</td><td>1</td></tr>
<tr><td>P05</td><td class="scene">Residential area</td><td>Thick</td><td>08 Sep 2023 06:59:46</td><td>23.8</td><td>5</td><td>10</td><td>22 Sep 2023 13:22:32</td><td>19.0</td><td>0</td><td>1</td></tr>
<tr><td>P06</td><td class="scene">Suburban road, residential area</td><td>Thin</td><td>08 Sep 2023 07:00:35</td><td>26.9</td><td>5</td><td>10</td><td>22 Sep 2023 13:26:21</td><td>22.4</td><td>0</td><td>1</td></tr>
<tr><td>P07</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:02:12</td><td>52.2</td><td>5</td><td>10</td><td>22 Sep 2023 13:26:52</td><td>44.5</td><td>0</td><td>1</td></tr>
<tr><td>P08</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:03:12</td><td>32.4</td><td>5</td><td>10</td><td>22 Sep 2023 13:27:44</td><td>30.3</td><td>0</td><td>1</td></tr>
<tr><td>P09</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:17:28</td><td>94.5</td><td>0</td><td>3</td><td>22 Sep 2023 13:30:34</td><td>88.6</td><td>0</td><td>1</td></tr>
<tr><td>P10</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:19:31</td><td>105.2</td><td>0</td><td>3</td><td>22 Sep 2023 13:32:31</td><td>94.2</td><td>0</td><td>1</td></tr>
<tr><td>P11</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:21:19</td><td>82.5</td><td>0</td><td>3</td><td>22 Sep 2023 13:34:16</td><td>77.6</td><td>0</td><td>1</td></tr>
<tr><td>P12</td><td class="scene">Suburban road</td><td>Thin</td><td>08 Sep 2023 07:22:50</td><td>50.2</td><td>0</td><td>3</td><td>22 Sep 2023 13:35:38</td><td>49.9</td><td>0</td><td>1</td></tr>
<tr><td>P13</td><td class="scene">Suburban road</td><td>Thin</td><td>08 Sep 2023 07:25:23</td><td>65.3</td><td>0</td><td>3</td><td>22 Sep 2023 13:41:07</td><td>75.8</td><td>0</td><td>1</td></tr>
<tr><td>P14</td><td class="scene">Suburban road</td><td>Thin</td><td>08 Sep 2023 07:36:38</td><td>34.1</td><td>0</td><td>3</td><td>22 Sep 2023 13:42:43</td><td>28.9</td><td>0</td><td>1</td></tr>
<tr><td>P15</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:37:16</td><td>120.2</td><td>0</td><td>3</td><td>22 Sep 2023 13:43:15</td><td>109.8</td><td>0</td><td>1</td></tr>
<tr><td>P16</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:39:22</td><td>33.0</td><td>0</td><td>3</td><td>22 Sep 2023 13:45:11</td><td>28.0</td><td>0</td><td>1</td></tr>
<tr><td>P17</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:40:22</td><td>41.5</td><td>0</td><td>3</td><td>22 Sep 2023 13:45:46</td><td>37.9</td><td>0</td><td>1</td></tr>
<tr><td>P18</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:41:12</td><td>16.1</td><td>0</td><td>3</td><td>22 Sep 2023 13:46:33</td><td>16.8</td><td>0</td><td>1</td></tr>
<tr><td>P19</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:41:42</td><td>59.8</td><td>0</td><td>3</td><td>22 Sep 2023 13:47:03</td><td>60.0</td><td>0</td><td>1</td></tr>
<tr><td>P20</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:50:47</td><td>64.6</td><td>0</td><td>2</td><td>22 Sep 2023 13:49:01</td><td>55.6</td><td>0</td><td>1</td></tr>
<tr><td>P21</td><td class="scene">Suburban road, residential area</td><td>Thin</td><td>08 Sep 2023 07:52:03</td><td>65.4</td><td>0</td><td>2</td><td>22 Sep 2023 13:50:19</td><td>61.0</td><td>0</td><td>1</td></tr>
<tr><td>P22</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:53:20</td><td>32.3</td><td>0</td><td>2</td><td>22 Sep 2023 13:51:40</td><td>31.5</td><td>0</td><td>1</td></tr>
<tr><td>P23</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:54:19</td><td>65.6</td><td>0</td><td>2</td><td>22 Sep 2023 13:52:47</td><td>82.9</td><td>0</td><td>1</td></tr>
<tr><td>P24</td><td class="scene">Residential area</td><td>Thin</td><td>08 Sep 2023 07:55:35</td><td>39.3</td><td>0</td><td>2</td><td>22 Sep 2023 13:58:30</td><td>32.8</td><td>0</td><td>1</td></tr>

<tr><td>Q00</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 06:41:36</td><td>63.7</td><td>20</td><td>15</td><td>22 Sep 2023 11:45:31</td><td>66.5</td><td>0</td><td>1</td></tr>
<tr><td>Q01</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 06:43:44</td><td>57.5</td><td>20</td><td>15</td><td>22 Sep 2023 11:40:25</td><td>53.4</td><td>0</td><td>1</td></tr>
<tr><td>Q02</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 06:45:01</td><td>64.0</td><td>20</td><td>15</td><td>22 Sep 2023 11:41:37</td><td>62.1</td><td>0</td><td>1</td></tr>
<tr><td>Q03</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 06:46:34</td><td>72.4</td><td>20</td><td>15</td><td>22 Sep 2023 11:43:06</td><td>68.4</td><td>0</td><td>1</td></tr>
<tr><td>Q04</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 06:47:57</td><td>36.6</td><td>20</td><td>15</td><td>22 Sep 2023 11:44:25</td><td>37.4</td><td>0</td><td>1</td></tr>
<tr><td>Q05</td><td class="scene">High street, suburban road</td><td>Thick</td><td>07 Sep 2023 06:30:12</td><td>127.7</td><td>20</td><td>15</td><td>22 Sep 2023 11:28:14</td><td>151.4</td><td>1</td><td>1</td></tr>
<tr><td>Q06</td><td class="scene">Country road</td><td>Thick</td><td>07 Sep 2023 07:23:32</td><td>93.6</td><td>10</td><td>5</td><td>22 Sep 2023 11:31:29</td><td>78.3</td><td>1</td><td>1</td></tr>
<tr><td>Q07</td><td class="scene">Suburban road</td><td>Thick</td><td>07 Sep 2023 06:34:45</td><td>21.4</td><td>20</td><td>15</td><td>22 Sep 2023 11:33:12</td><td>18.2</td><td>1</td><td>1</td></tr>
<tr><td>Q08</td><td class="scene">Suburban road</td><td>Thick</td><td>07 Sep 2023 06:38:34</td><td>23.8</td><td>20</td><td>15</td><td>22 Sep 2023 11:33:34</td><td>21.1</td><td>1</td><td>1</td></tr>
<tr><td>Q09</td><td class="scene">Suburban road, residential area</td><td>Thick</td><td>07 Sep 2023 07:25:21</td><td>62.2</td><td>10</td><td>5</td><td>22 Sep 2023 11:52:08</td><td>60.3</td><td>0</td><td>1</td></tr>
<tr><td>Q10</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:27:11</td><td>55.2</td><td>10</td><td>5</td><td>22 Sep 2023 11:53:50</td><td>49.6</td><td>0</td><td>1</td></tr>
<tr><td>Q11</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:37:54</td><td>94.2</td><td>5</td><td>5</td><td>22 Sep 2023 11:56:08</td><td>88.5</td><td>0</td><td>1</td></tr>
<tr><td>Q12</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:39:36</td><td>24.8</td><td>5</td><td>5</td><td>22 Sep 2023 11:57:43</td><td>20.1</td><td>0</td><td>1</td></tr>
<tr><td>Q13</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:40:42</td><td>45.1</td><td>5</td><td>5</td><td>22 Sep 2023 11:58:24</td><td>36.5</td><td>0</td><td>1</td></tr>
<tr><td>Q14</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:44:04</td><td>30.8</td><td>5</td><td>5</td><td>22 Sep 2023 11:59:14</td><td>30.7</td><td>0</td><td>1</td></tr>
<tr><td>Q15</td><td class="scene">Suburban road</td><td>Thick</td><td>07 Sep 2023 07:44:43</td><td>23.4</td><td>5</td><td>5</td><td>22 Sep 2023 11:59:54</td><td>23.9</td><td>0</td><td>1</td></tr>
<tr><td>Q16</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:46:56</td><td>21.6</td><td>5</td><td>5</td><td>22 Sep 2023 11:46:49</td><td>26.8</td><td>0</td><td>1</td></tr>
<tr><td>Q17</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:47:25</td><td>11.7</td><td>5</td><td>5</td><td>22 Sep 2023 11:48:30</td><td>13.3</td><td>0</td><td>1</td></tr>
<tr><td>Q18</td><td class="scene">Suburban road</td><td>Thick</td><td>07 Sep 2023 07:47:44</td><td>23.5</td><td>5</td><td>5</td><td>22 Sep 2023 11:48:51</td><td>24.0</td><td>0</td><td>1</td></tr>
<tr><td>Q19</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:49:31</td><td>53.0</td><td>5</td><td>5</td><td>22 Sep 2023 11:49:21</td><td>52.3</td><td>0</td><td>1</td></tr>
<tr><td>Q20</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:50:41</td><td>35.1</td><td>5</td><td>5</td><td>22 Sep 2023 11:50:20</td><td>40.7</td><td>0</td><td>1</td></tr>
<tr><td>Q21</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:51:24</td><td>33.9</td><td>5</td><td>5</td><td>22 Sep 2023 11:51:08</td><td>37.3</td><td>0</td><td>1</td></tr>
<tr><td>Q22</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:54:02</td><td>43.9</td><td>5</td><td>5</td><td>22 Sep 2023 11:38:59</td><td>39.4</td><td>0</td><td>1</td></tr>
<tr><td>Q23</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 07:56:46</td><td>34.0</td><td>5</td><td>5</td><td>22 Sep 2023 11:39:43</td><td>35.8</td><td>0</td><td>1</td></tr>
<tr><td>Q24</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 08:10:11</td><td>15.4</td><td>5</td><td>5</td><td>22 Sep 2023 12:01:06</td><td>15.8</td><td>0</td><td>1</td></tr>
<tr><td>Q25</td><td class="scene">Residential area</td><td>Thick</td><td>07 Sep 2023 08:10:33</td><td>50.2</td><td>5</td><td>5</td><td>22 Sep 2023 12:01:35</td><td>50.3</td><td>0</td><td>1</td></tr>

<tr><td>R00</td><td class="scene">Suburban road, country road</td><td>Thin</td><td>05 Sep 2023 07:10:42</td><td>20.3</td><td>1</td><td>1</td><td>-</td><td>-</td><td>-</td><td>-</td></tr>

</tbody>

</table>

# Folder structure of each sequence
The recorded data files of each sequence are organised in a folder that has the following structure.
```bash
Xxx_weather
├── images_colour
│   ├── image_0
│   │   ├── 000000.png
│   │   ├── 000001.png
│   │   ├── 000002.png
│   │   └── ...
│   ├── image_1
│   │   ├── 000000.png
│   │   ├── 000001.png
│   │   ├── 000002.png
│   │   └── ...
│   ├── img_timestamps.csv
│   └── img_timestamps_zeroed.csv
├── imu
│   ├── imu_data.csv
│   └── imu_timestamps.csv
└── mag
    ├── mag_data.csv
    └── mag_timestamps.csv
```
- `Xxx` is the episode:`X` represents where the data episode was recorded, and `xx` represents the number.
For example, `R00` represents the first episode recorded in Rosyth, `Q01`
represents the second episode recorded in Queensferry, and `P02` represents
the third episode recorded in Penicuik.
- `weather` represents the weather condition: `FogThin`, `FogThick`, or `Overcast`
- `image_0` (resp. `image_1`) is a folder containing the images of the left (resp. right) frame.

# Sequence thumbnails

The following table summarises the sequence thumbnails for each episode in the dataset. Each entry shows the representative image for the foggy sequence and, where available, the corresponding overcast sequence.

<table class="sequence-thumb-table">
  <thead>
    <tr>
      <th>Episode</th>
      <th>Scene</th>
      <th>Fog density</th>
      <th>Foggy</th>
      <th>Overcast</th>
    </tr>
  </thead>
  <tbody>
    <tr><td>P00</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P00_FogThick.png" alt="P00 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P00_Overcast.png" alt="P00 overcast thumbnail"></td></tr>
    <tr><td>P01</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P01_FogThick.png" alt="P01 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P01_Overcast.png" alt="P01 overcast thumbnail"></td></tr>
    <tr><td>P02</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P02_FogThick.png" alt="P02 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P02_Overcast.png" alt="P02 overcast thumbnail"></td></tr>
    <tr><td>P03</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P03_FogThick.png" alt="P03 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P03_Overcast.png" alt="P03 overcast thumbnail"></td></tr>
    <tr><td>P04</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P04_FogThick.png" alt="P04 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P04_Overcast.png" alt="P04 overcast thumbnail"></td></tr>
    <tr><td>P05</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P05_FogThick.png" alt="P05 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P05_Overcast.png" alt="P05 overcast thumbnail"></td></tr>
    <tr><td>P06</td><td>Suburban road, residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P06_FogThin.png" alt="P06 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P06_Overcast.png" alt="P06 overcast thumbnail"></td></tr>
    <tr><td>P07</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P07_FogThin.png" alt="P07 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P07_Overcast.png" alt="P07 overcast thumbnail"></td></tr>
    <tr><td>P08</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P08_FogThin.png" alt="P08 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P08_Overcast.png" alt="P08 overcast thumbnail"></td></tr>
    <tr><td>P09</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P09_FogThin.png" alt="P09 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P09_Overcast.png" alt="P09 overcast thumbnail"></td></tr>
    <tr><td>P10</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P10_FogThin.png" alt="P10 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P10_Overcast.png" alt="P10 overcast thumbnail"></td></tr>
    <tr><td>P11</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P11_FogThin.png" alt="P11 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P11_Overcast.png" alt="P11 overcast thumbnail"></td></tr>
    <tr><td>P12</td><td>Suburban road</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P12_FogThin.png" alt="P12 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P12_Overcast.png" alt="P12 overcast thumbnail"></td></tr>
    <tr><td>P13</td><td>Suburban road</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P13_FogThin.png" alt="P13 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P13_Overcast.png" alt="P13 overcast thumbnail"></td></tr>
    <tr><td>P14</td><td>Suburban road</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P14_FogThin.png" alt="P14 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P14_Overcast.png" alt="P14 overcast thumbnail"></td></tr>
    <tr><td>P15</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P15_FogThin.png" alt="P15 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P15_Overcast.png" alt="P15 overcast thumbnail"></td></tr>
    <tr><td>P16</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P16_FogThin.png" alt="P16 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P16_Overcast.png" alt="P16 overcast thumbnail"></td></tr>
    <tr><td>P17</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P17_FogThin.png" alt="P17 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P17_Overcast.png" alt="P17 overcast thumbnail"></td></tr>
    <tr><td>P18</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P18_FogThin.png" alt="P18 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P18_Overcast.png" alt="P18 overcast thumbnail"></td></tr>
    <tr><td>P19</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P19_FogThin.png" alt="P19 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P19_Overcast.png" alt="P19 overcast thumbnail"></td></tr>
    <tr><td>P20</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P20_FogThin.png" alt="P20 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P20_Overcast.png" alt="P20 overcast thumbnail"></td></tr>
    <tr><td>P21</td><td>Suburban road, residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P21_FogThin.png" alt="P21 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P21_Overcast.png" alt="P21 overcast thumbnail"></td></tr>
    <tr><td>P22</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P22_FogThin.png" alt="P22 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P22_Overcast.png" alt="P22 overcast thumbnail"></td></tr>
    <tr><td>P23</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P23_FogThin.png" alt="P23 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P23_Overcast.png" alt="P23 overcast thumbnail"></td></tr>
    <tr><td>P24</td><td>Residential area</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P24_FogThin.png" alt="P24 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/P24_Overcast.png" alt="P24 overcast thumbnail"></td></tr>
    <tr><td>Q00</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q00_FogThick.png" alt="Q00 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q00_Overcast.png" alt="Q00 overcast thumbnail"></td></tr>
    <tr><td>Q01</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q01_FogThick.png" alt="Q01 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q01_Overcast.png" alt="Q01 overcast thumbnail"></td></tr>
    <tr><td>Q02</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q02_FogThick.png" alt="Q02 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q02_Overcast.png" alt="Q02 overcast thumbnail"></td></tr>
    <tr><td>Q03</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q03_FogThick.png" alt="Q03 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q03_Overcast.png" alt="Q03 overcast thumbnail"></td></tr>
    <tr><td>Q04</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q04_FogThick.png" alt="Q04 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q04_Overcast.png" alt="Q04 overcast thumbnail"></td></tr>
    <tr><td>Q05</td><td>High street, suburban road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q05_FogThick.png" alt="Q05 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q05_Overcast.png" alt="Q05 overcast thumbnail"></td></tr>
    <tr><td>Q06</td><td>Country road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q06_FogThick.png" alt="Q06 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q06_Overcast.png" alt="Q06 overcast thumbnail"></td></tr>
    <tr><td>Q07</td><td>Suburban road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q07_FogThick.png" alt="Q07 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q07_Overcast.png" alt="Q07 overcast thumbnail"></td></tr>
    <tr><td>Q08</td><td>Suburban road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q08_FogThick.png" alt="Q08 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q08_Overcast.png" alt="Q08 overcast thumbnail"></td></tr>
    <tr><td>Q09</td><td>Suburban road, residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q09_FogThick.png" alt="Q09 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q09_Overcast.png" alt="Q09 overcast thumbnail"></td></tr>
    <tr><td>Q10</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q10_FogThick.png" alt="Q10 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q10_Overcast.png" alt="Q10 overcast thumbnail"></td></tr>
    <tr><td>Q11</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q11_FogThick.png" alt="Q11 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q11_Overcast.png" alt="Q11 overcast thumbnail"></td></tr>
    <tr><td>Q12</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q12_FogThick.png" alt="Q12 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q12_Overcast.png" alt="Q12 overcast thumbnail"></td></tr>
    <tr><td>Q13</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q13_FogThick.png" alt="Q13 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q13_Overcast.png" alt="Q13 overcast thumbnail"></td></tr>
    <tr><td>Q14</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q14_FogThick.png" alt="Q14 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q14_Overcast.png" alt="Q14 overcast thumbnail"></td></tr>
    <tr><td>Q15</td><td>Suburban road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q15_FogThick.png" alt="Q15 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q15_Overcast.png" alt="Q15 overcast thumbnail"></td></tr>
    <tr><td>Q16</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q16_FogThick.png" alt="Q16 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q16_Overcast.png" alt="Q16 overcast thumbnail"></td></tr>
    <tr><td>Q17</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q17_FogThick.png" alt="Q17 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q17_Overcast.png" alt="Q17 overcast thumbnail"></td></tr>
    <tr><td>Q18</td><td>Suburban road</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q18_FogThick.png" alt="Q18 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q18_Overcast.png" alt="Q18 overcast thumbnail"></td></tr>
    <tr><td>Q19</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q19_FogThick.png" alt="Q19 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q19_Overcast.png" alt="Q19 overcast thumbnail"></td></tr>
    <tr><td>Q20</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q20_FogThick.png" alt="Q20 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q20_Overcast.png" alt="Q20 overcast thumbnail"></td></tr>
    <tr><td>Q21</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q21_FogThick.png" alt="Q21 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q21_Overcast.png" alt="Q21 overcast thumbnail"></td></tr>
    <tr><td>Q22</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q22_FogThick.png" alt="Q22 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q22_Overcast.png" alt="Q22 overcast thumbnail"></td></tr>
    <tr><td>Q23</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q23_FogThick.png" alt="Q23 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q23_Overcast.png" alt="Q23 overcast thumbnail"></td></tr>
    <tr><td>Q24</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q24_FogThick.png" alt="Q24 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q24_Overcast.png" alt="Q24 overcast thumbnail"></td></tr>
    <tr><td>Q25</td><td>Residential area</td><td>Thick</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q25_FogThick.png" alt="Q25 foggy thumbnail"></td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/Q25_Overcast.png" alt="Q25 overcast thumbnail"></td></tr>
    <tr><td>R00</td><td>Suburban road, country road</td><td>Thin</td><td><img class="sequence-thumb" src="{{ site.baseurl }}/assets/sequence_thumbnails/R00_FogThin.png" alt="R00 foggy thumbnail"></td><td>-</td></tr>
  </tbody>
</table>
