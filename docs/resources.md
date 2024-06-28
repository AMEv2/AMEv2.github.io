---
layout: default
title: Resources
nav_order: 3
has_children: false
mathjax: true
permalink: /docs/resources
---

# Resources
{: .no_toc }
Links to useful information regarding DIY annealers.

1. TOC
{:toc}

# Links to useful information
 - <a href="https://forum.accurateshooter.com/threads/induction-brass-annealer-redux.3908353/" target="_blank">Accurateshooter Forum topic about DIY Annealer builds</a>
- <a href="https://spaco.org/Blacksmithing/ZVSInductionHeater/1000Watt12to48VoltZVSInductionHeaterTroubleshootingGuide.htm" target="_blank">1000W 20A Annealer Troubleshooting</a>

# Anneal Time Calculator

Formula as demonstrated by Youtuber [Reese on the Range](https://www.youtube.com/@reeseontherange) to calculate the time required to anneal brass given a temperature.<br>
$$t2=t1 * exp(\frac{-E}{B}*(\frac{1}{T1} - \frac{1}{T2}))$$
<br>

where:

`B` = 1.38065x10^-23 (Boltzmann constant)<br>
`E` = 0.327x10^-18 (constant for the material, in this case brass)<br>
`t1` = 3600 seconds (the time required to anneal brass at temperature `T1`)<br>
`T1` = 644 Kelvin (700 Fahrenheit)<br>
`T2` = Target Temperature<br>
`t2` = Time required to anneal brass at target temperature

<br><br>
Enter Target temperature, click calculate to calculate time required at that temperature to anneal brass.

<head>
<body>
<script>
    function runCalc() {
      var T2_raw = document.getElementById("T2").value;
      var t1 = 3600;
      var T1 = 644;
      var B = 1.38065 * Math.pow(10, -23);
      var E = 0.327 * Math.pow(10, -18);
      var T2 = T2_raw;
      var unit = document.querySelector('input[name="unit"]:checked').value;
      if (unit === 'celsius') {
        T2 = Number(T2_raw) + Number(273.15);
      } else if (unit === 'fahrenheit') {
        T2 = (T2_raw - 32) * (5/9) + 273.15;
      }
      var t2 = t1 * Math.exp(-E / B * ((1 / T1) - (1 / T2)));
      document.getElementById("t2").value = t2;
    }
  </script>
  <div id="annealTimeForm">
  <label for="unit">Select Unit:</label>
  <div>
    <input type="radio" id="celsius" name="unit" value="celsius" checked>
    <label for="celsius">Celsius</label>
  </div>
  <div>
    <input type="radio" id="fahrenheit" name="unit" value="fahrenheit">
    <label for="fahrenheit">Fahrenheit</label>
  </div>
  <div>
    <input type="radio" id="kelvin" name="unit" value="kelvin">
    <label for="kelvin">Kelvin</label>
  </div>
  <label for="T2">Target Temperature (T2):</label>
  <input id="T2" type="number"/>
  <button id="btnCalculate" type="button" onclick='runCalc()'>Calculate</button><br>
  <label for="t2">Required Anneal Time (t2)(s):</label>
  <input id="t2" type="number" readonly>
  </div>
  </body>