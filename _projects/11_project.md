---
layout: page
title: R Activity Methylation
description: This project analyzes IDAT files using R to visualize epigenetic patterns through bar and density plots.
img: assets/img/R_Activity_Methylation_Project.png
importance: 11
category: work
---

---

### Data set

---

[View the dataset on NCBI GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE252130)

---

### Update Data set

---

To use another dataset modify the line.
```R
dir_idat = "{idat_folder_path}"
``` 

Replace **{idat_folder_path}** with the path corresponding to the folder containing the IDAT files of the dataset.

Also modify the line 
```R
targets <- read.metharray.sheet(dir_idat, pattern="{sampleSheet_name}")
``` 
Replace **{sampleSheet_name}** with the name of the appropriate SampleSheet file, and make sure that the file is located in the same folder as the IDAT files.

---

### Results

---

{% include figure.liquid loading="eager" path="assets/img/barplot.png" title="Categories" class="img-fluid_customized rounded z-depth-1" %}

---

{% include figure.liquid loading="eager" path="assets/img/densityplot.png" title="Categories" class="img-fluid_customized rounded z-depth-1" %}


---

<!-- Button to GitHub Repo -->
<div style="text-align:left; margin-bottom: 20px;">
  <a href="https://github.com/felixsuarez0727/Activity-R-Methylation" target="_blank">
    <button id="github-repo-button" style="padding: 10px 20px; color: white; border: none; border-radius: 5px; cursor: pointer;">
      View Repository on GitHub
    </button>
  </a>
</div>