---
layout: default  # Or another layout if you have one
title: Photometric Calibration
permalink: /photometric_calibration/ 
---
<style>
.wrapper { max-width: 1200px; padding-left: 24px; padding-right: 24px; }
</style>

<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']],
      processEscapes: true
    },
    svg: {
      fontCache: 'global'
    }
  };
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js"></script>

The atmospheric scattering model operates in the **radiance** domain.
However, the ZED 2i camera features an onboard ISP and can only save the digitally post-processed intensity data, but not the raw radiance data.
Therefore, for the on-road data that we recorded, we have to *infer* the **radiance** values from the **intensity** values.
This process requires the photometric parameters of the camera to be known, and we achieve this by performing a photometric calibration in a controlled laboratory where the radiance values can be measured by an optical power meter.

Our calibration process focuses on recovering the parameters of **gamma correction**, which introduces the largest amount of **non-linearity** in the mapping between radiance and intensity.
We use $g : [0, 255] \to \mathbb{R}^{+}$ to denote a mapping from pixel intensity $I$ to radiance $L$:

$$
g(I) = \alpha I^{\gamma} + \zeta \text{,}
$$

where $\alpha \in \mathbb{R}_{++}$, $\gamma > 1$ and $\zeta \in \mathbb{R}$ are the parameters that jointly characterise $g$.

More details of our photometric calibration can be found in Section IV-B of our [paper](https://ieeexplore.ieee.org/document/11218959) and Section I-B of our [supplementary material](https://ieeexplore.ieee.org/document/11218959/media#media).
In the following table we summarise the estimated photometric parameters for all eight combinations of the gain and the exposure time.
They are also specified in our [code](https://github.com/SenseRoboticsLab/estimating-fog-parameters/blob/main/src/FogEstimation.cc#L86-L142).
Given any sequence of images listed in the [Data episodes and sequences]({{ site.baseurl }}/overview/#data-episodes-and-sequences) section, these photometric parameters facilitate the mapping from the intensity domain to the radiance domain, in which the atmospheric scattering model can be correctly deployed according to the atmospheric scattering model equation.

<style>

table {
  border-collapse: collapse;
  text-align: center;
  font-size: 14px;
  min-width: 980px;
}

.table-scroll {
  overflow-x: auto;
  -webkit-overflow-scrolling: touch;
  margin: 1rem 0;
}

th, td {
  border: 1px solid black;
  padding: 5px 8px;
  font-size: 13px;
  white-space: nowrap;
}

.num {
  text-align: right;
  font-family: "Courier New", monospace;
  font-size: 12.5px;
}
</style>

<div class="table-scroll">
<table>
<thead>
<tr>
<th rowspan="2">Gain</th>
<th rowspan="2">Exp.</th>
<th rowspan="2">Target bench<br>sep. (mm)</th>

<th colspan="3">Red</th>
<th colspan="3">Green</th>
<th colspan="3">Blue</th>
<th colspan="3">Gray</th>

<th rowspan="2">No. imgs</th>
</tr>

<tr>
<th>\(\alpha\)</th>
<th>\(\zeta\)</th>
<th>\(\gamma\)</th>

<th>\(\alpha\)</th>
<th>\(\gamma\)</th>
<th>\(\zeta\)</th>

<th>\(\alpha\)</th>
<th>\(\gamma\)</th>
<th>\(\zeta\)</th>

<th>\(\alpha\)</th>
<th>\(\gamma\)</th>
<th>\(\zeta\)</th>
</tr>
</thead>

<tbody>

<tr>
<td>0</td>
<td>1</td>
<td rowspan="5">283</td>

<td class="num">7.87e-02</td>
<td class="num">1.701</td>
<td class="num">-25.999</td>

<td class="num">2.006e-01</td>
<td class="num">1.467</td>
<td class="num">7.043</td>

<td class="num">3.093e-01</td>
<td class="num">1.321</td>
<td class="num">-23.872</td>

<td class="num">1.198e-01</td>
<td class="num">1.580</td>
<td class="num">-2.477</td>

<td rowspan="5">20</td>
</tr>

<tr>
<td>0</td>
<td>2</td>

<td class="num">9.125e-01</td>
<td class="num">1.044</td>
<td class="num">-36.017</td>

<td class="num">9.402e-02</td>
<td class="num">1.494</td>
<td class="num">4.053</td>

<td class="num">2.637e-01</td>
<td class="num">1.218</td>
<td class="num">-15.370</td>

<td class="num">1.344e-01</td>
<td class="num">1.407</td>
<td class="num">-4.047</td>
</tr>

<tr>
<td>0</td>
<td>3</td>

<td class="num">1.794e-01</td>
<td class="num">1.278</td>
<td class="num">-14.429</td>

<td class="num">1.142e-01</td>
<td class="num">1.364</td>
<td class="num">0.740</td>

<td class="num">2.224e-02</td>
<td class="num">1.618</td>
<td class="num">-1.360</td>

<td class="num">1.010e-01</td>
<td class="num">1.380</td>
<td class="num">-3.239</td>
</tr>

<tr>
<td>1</td>
<td>1</td>

<td class="num">1.026e-01</td>
<td class="num">1.633</td>
<td class="num">-27.295</td>

<td class="num">1.742e-01</td>
<td class="num">1.493</td>
<td class="num">7.142</td>

<td class="num">3.553e-01</td>
<td class="num">1.284</td>
<td class="num">-24.601</td>

<td class="num">1.316e-01</td>
<td class="num">1.584</td>
<td class="num">-2.267</td>
</tr>

<tr>
<td>5</td>
<td>5</td>

<td class="num">2.001e-03</td>
<td class="num">2.005</td>
<td class="num">3.299</td>

<td class="num">8.037e-03</td>
<td class="num">1.751</td>
<td class="num">4.909</td>

<td class="num">5.032e-04</td>
<td class="num">2.199</td>
<td class="num">5.288</td>

<td class="num">3.984e-03</td>
<td class="num">1.874</td>
<td class="num">4.408</td>

<tr>
<td>5</td>
<td>10</td>
<td>495</td>

<td class="num">3.120e-03</td>
<td class="num">1.788</td>
<td class="num">0.046</td>

<td class="num">1.082e-02</td>
<td class="num">1.557</td>
<td class="num">1.134</td>

<td class="num">8.394e-04</td>
<td class="num">1.975</td>
<td class="num">1.318</td>

<td class="num">5.737e-03</td>
<td class="num">1.669</td>
<td class="num">0.797</td>

<td>19</td>
</tr>

<tr>
<td>10</td>
<td>5</td>
<td>283</td>

<td class="num">1.706e-03</td>
<td class="num">2.001</td>
<td class="num">3.075</td>

<td class="num">7.655e-03</td>
<td class="num">1.727</td>
<td class="num">4.213</td>

<td class="num">5.052e-04</td>
<td class="num">2.166</td>
<td class="num">4.471</td>

<td class="num">3.715e-03</td>
<td class="num">1.854</td>
<td class="num">3.831</td>

<td>17</td>
</tr>

<tr>
<td>20</td>
<td>15</td>
<td>567</td>

<td class="num">3.894e-04</td>
<td class="num">2.018</td>
<td class="num">0.724</td>

<td class="num">1.448e-03</td>
<td class="num">1.777</td>
<td class="num">1.187</td>

<td class="num">1.306e-04</td>
<td class="num">2.160</td>
<td class="num">1.021</td>

<td class="num">7.607e-04</td>
<td class="num">1.889</td>
<td class="num">1.013</td>

<td>14</td>
</tr>
