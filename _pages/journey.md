---
layout: page
title: Journey
permalink: /journey/
description: Academic and Professional Timeline
nav: true
nav_order: 5
---

<style>
  /* Base de la línea de tiempo */
  .timeline {
    position: relative;
    max-width: 900px;
    margin: 0 auto;
    padding: 40px 0;
  }

  /* Eje de tiempo vertical */
  .timeline::after {
    content: '';
    position: absolute;
    width: 4px;
    background-color: var(--global-theme-color);
    top: 0;
    bottom: 0;
    left: 50%;
    margin-left: -2px;
    border-radius: 2px;
    z-index: 1;
  }

  /* Marcadores de años en el eje */
  .year-marker {
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    align-items: center;
    z-index: 2;
  }

  .year-marker-line {
    width: 10px;
    height: 2px;
    background-color: var(--global-theme-color);
  }

  .year-label {
    padding: 2px 6px;
    background-color: var(--global-theme-color);
    color: white;
    border-radius: 10px;
    font-size: 0.75rem;
    margin-left: 5px;
    white-space: nowrap;
  }

  /* Elementos de la línea de tiempo */
  .timeline-item {
    padding: 10px 40px;
    position: relative;
    width: 50%;
    box-sizing: border-box;
    margin: 30px 0;
  }

  /* Círculos en la línea de tiempo */
  .timeline-item::after {
    content: '';
    position: absolute;
    width: 16px;
    height: 16px;
    background-color: var(--global-theme-color);
    border: 3px solid var(--global-bg-color);
    border-radius: 50%;
    top: 28px;
    z-index: 2;
    transition: all 0.3s ease;
  }
  
  .timeline-item:hover::after {
    transform: scale(1.2);
    box-shadow: 0 0 10px rgba(var(--global-theme-color-rgb), 0.5);
  }

  /* Indicador de rango en el eje temporal */
  .year-range {
    position: absolute;
    width: 4px;
    background-color: var(--global-theme-color);
    opacity: 0.0; 
    left: 50%;
    margin-left: -2px;
    border-radius: 2px;
    transition: all 0.3s ease;
    z-index: 1;
  }
  
  .timeline-item:hover .year-range {
    opacity: 0.6;
    width: 8px;
    margin-left: -4px;
  }

  /* Colores específicos para cada rango */
  .year-range-1 { background-color: var(--global-highlight-color); }
  .year-range-2 { background-color: var(--global-highlight-color); }
  .year-range-3 { background-color: var(--global-highlight-color); }
  .year-range-4 { background-color: var(--global-highlight-color); }
  .year-range-5 { background-color: var(--global-highlight-color); }
  .year-range-6 { background-color: var(--global-highlight-color); }
  .year-range-7 { background-color: var(--global-highlight-color); }

  /* Conector desde el rango hasta el elemento */
  .range-connector {
    position: absolute;
    height: 2px;
    background-color: var(--global-theme-color);
    opacity: 0.4;
    z-index: 0;
    transition: opacity 0.3s ease;
  }
  
  .timeline-item:hover .range-connector {
    opacity: 0.8;
  }

  /* Periodo de tiempo en el contenido */
  .timeline-period {
    display: inline-block;
    background-color: var(--global-theme-color);
    color: white;
    padding: 3px 10px;
    border-radius: 12px;
    font-size: 0.8rem;
    font-weight: bold;
    margin-bottom: 8px;
    transition: all 0.3s ease;
  }
  
  .timeline-item:hover .timeline-period {
    transform: scale(1.05);
    box-shadow: 0 2px 5px rgba(0,0,0,0.15);
  }

  /* Colores para cada etiqueta de período que correspondan con los rangos */
  .period-color-1 { background-color: var(--global-theme-color); }
  .period-color-2 { background-color: var(--global-theme-color); }
  .period-color-3 { background-color: var(--global-theme-color); }
  .period-color-4 { background-color: var(--global-theme-color); }
  .period-color-5 { background-color: var(--global-theme-color); }
  .period-color-6 { background-color: var(--global-theme-color); }
  .period-color-7 { background-color: var(--global-theme-color); }

  /* Elementos a la izquierda */
  .timeline-item:nth-child(odd) {
    left: 0;
    text-align: right;
  }
  .timeline-item:nth-child(odd)::after {
    right: -8px;
  }
  .timeline-item:nth-child(odd) .range-connector {
    right: -8px;
    top: 36px;
    width: 40px;
  }

  /* Elementos a la derecha */
  .timeline-item:nth-child(even) {
    left: 50%;
    text-align: left;
  }
  .timeline-item:nth-child(even)::after {
    left: -8px;
  }
  .timeline-item:nth-child(even) .range-connector {
    left: -8px;
    top: 36px;
    width: 40px;
  }

  /* Estilo del contenido */
  .timeline-content {
    padding: 20px;
    background-color: var(--global-card-bg-color);
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.08);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
    border-right: 3px solid var(--global-theme-color);
    backdrop-filter: blur(5px);
  }

  .timeline-item:nth-child(even) .timeline-content {
    border-right: none;
    border-left: 3px solid var(--global-theme-color);
  }

  .timeline-content:hover {
    box-shadow: 0 8px 20px rgba(0,0,0,0.12);
    transform: translateY(-2px);
  }

  .timeline-content h3 {
    margin-top: 0;
    color: var(--global-theme-color);
    font-weight: 600;
    font-size: 1.1rem;
  }

  /* Estilo de la institución */
  .institution-container {
    position: relative;
    display: inline-block;
    width: 100%;
    margin-top: 5px;
  }

  .institution {
    display: inline-block;
    max-width: 100%;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
    color: var(--global-text-color);
    font-style: italic;
    font-size: 0.92rem;
    position: relative;
    cursor: help;
    padding: 2px 4px;
    transition: all 0.2s ease;
  }
  
  .institution::after {
    content: "";
    position: absolute;
    width: 100%;
    height: 1px;
    bottom: 0;
    left: 0;
    background-color: var(--global-theme-color);
    transform: scaleX(0);
    transform-origin: bottom right;
    transition: transform 0.3s ease;
    opacity: 0.5;
  }
  
  .institution-container:hover .institution::after {
    transform: scaleX(1);
    transform-origin: bottom left;
  }

  .institution-tooltip {
    visibility: hidden;
    width: auto;
    max-width: 250px;
    background-color: rgba(0, 0, 0, 0.75);
    color: #fff;
    text-align: center;
    border-radius: 6px;
    padding: 6px 12px;
    position: absolute;
    z-index: 5;
    bottom: 125%;
    left: 50%;
    transform: translateX(-50%);
    opacity: 0;
    transition: opacity 0.3s, transform 0.3s;
    transform: translateX(-50%) translateY(10px);
    pointer-events: none;
    font-size: 0.85rem;
  }

  .institution-tooltip::after {
    content: "";
    position: absolute;
    top: 100%;
    left: 50%;
    margin-left: -5px;
    border-width: 5px;
    border-style: solid;
    border-color: rgba(0, 0, 0, 0.75) transparent transparent transparent;
  }

  .institution-container:hover .institution-tooltip {
    visibility: visible;
    opacity: 1;
    transform: translateX(-50%) translateY(0);
  }

  /* Divisor */
  .divider {
    width: 100%;
    text-align: center;
    margin: 50px 0;
    position: relative;
    clear: both;
  }

  .divider-text {
    display: inline-block;
    padding: 6px 20px;
    background-color: var(--global-bg-color);
    color: var(--global-theme-color);
    font-weight: bold;
    position: relative;
    z-index: 2;
    border: 2px solid var(--global-theme-color);
    border-radius: 20px;
    transition: all 0.3s ease;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  }
  
  .divider-text:hover {
    box-shadow: 0 4px 8px rgba(0,0,0,0.15);
    transform: translateY(-1px);
  }

  .divider::before {
    content: '';
    position: absolute;
    top: 50%;
    left: 0;
    right: 0;
    height: 1px;
    background-color: var(--global-theme-color);
    z-index: 1;
  }

  /* Diseño responsivo */
  @media screen and (max-width: 768px) {
    .timeline::after {
      left: 31px;
    }
    
    .timeline-item {
      width: 100%;
      padding-left: 70px;
      padding-right: 25px;
      left: 0 !important;
      text-align: left !important;
    }
    
    .timeline-item::after {
      left: 21px !important;
      right: auto !important;
    }
    
    .timeline-item .timeline-content {
      border-left: 3px solid var(--global-theme-color) !important;
      border-right: none !important;
    }
    
    .range-connector {
      left: 21px !important;
      right: auto !important;
      width: 40px !important;
      top: 36px !important;
    }
    
    .year-marker {
      left: 31px !important;
      transform: translateX(0) scale(0.9);
    }
    
    .year-label {
      font-size: 0.7rem;
      padding: 1px 5px;
    }
    
    .year-range {
      left: 31px !important;
      width: 4px;
      margin-left: -2px;
    }
    
    .timeline-item:hover .year-range {
      left: 31px !important;
      width: 8px;
      margin-left: -4px;
    }
  }
  
  /* Ajustes para modo oscuro */
  @media (prefers-color-scheme: dark) {
    .timeline-content {
      box-shadow: 0 4px 10px rgba(0,0,0,0.2);
    }
    
    .institution-tooltip {
      background-color: rgba(30, 30, 30, 0.9);
    }
    
    .institution-tooltip::after {
      border-color: rgba(30, 30, 30, 0.9) transparent transparent transparent;
    }
  }
</style>

<div class="timeline">
  <!-- Year markers on vertical axis - now properly aligned with starting years -->
  <div class="year-marker" style="top: 8%;">
    <div class="year-label">2005</div>
  </div>
  <div class="year-marker" style="top: 20%;">
    <!-- <div class="year-label">2010</div> -->
  </div>
  <div class="year-marker" style="top: 20.1%;">
    <!-- <div class="year-label">2011</div> -->
  </div>
  <div class="year-marker" style="top: 23.2%;">
    <div class="year-label">2012</div>
  </div>
  <div class="year-marker" style="top: 37.1%;">
    <div class="year-label">2016</div>
  </div>
  <div class="year-marker" style="top: 58.8%;">
    <div class="year-label">2015</div> 
  </div>
  <div class="year-marker" style="top: 72.6%;">
    <div class="year-label">2019</div>
  </div>
  <div class="year-marker" style="top: 86.2%;">
    <div class="year-label">2024</div>
  </div>
  <div class="year-marker" style="top: 87.9%;">
    <!-- <div class="year-label">2025</div> -->
  </div>
  
  <!-- Time range indicators - adjusted to match actual timeline items -->
  <!--  <div class="year-range year-range-1" style="top: 7.4%; height: 9.2%;"></div> <!-- Bachelor's (2005-2009) -->
  <!-- <div class="year-range year-range-2" style="top: 22.4%; height: 35.9%;"></div> <!-- Licentiate (2012-2017) -->
  <!-- <div class="year-range year-range-3" style="top: 35%; height: 29%;"></div>  Master's in Chemistry (2011-2016) -->
  <!-- <div class="year-range year-range-4" style="top: 36%; height: 28%;"></div> <!-- Master in EE (2016-2019) -->
  <!--  <div class="year-range year-range-5" style="top: 59%; height: 41%;"></div> <!-- PhD (2011-2016) -->
  <!--  <div class="year-range year-range-6" style="top: 59%; height: 41%;"></div> <!-- Postdoc Bristol (2017-2025) -->
  <!-- <div class="year-range year-range-7" style="top: 59%; height: 41%;"></div> <!-- Postdoc ICMol (2017-2025) -->
  <!-- <div class="year-range year-range-8" style="top: 59%; height: 41%;"></div> <!-- Senior Researcher (2017-2025) -->

  <!-- Timeline items -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-1">2005 - 2009</div>
      <h3>Bachelor's Degree in Electrical Engineering</h3>
      <div class="institution-container">
        <div class="institution">University of Costa Rica</div>
        <span class="institution-tooltip">University of Costa Rica, Costa Rica</span>
      </div>
    </div>
  </div>
  
  <!-- Master's in Theoretical Chemistry -->
  <!-- <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-2">2011 - 2016</div>
      <h3>Master's in Theoretical Chemistry</h3>
      <h3>PhD in Theoretical Chemistry</h3>
      <div class="institution-container">
        <div class="institution">University of Valencia</div>
        <span class="institution-tooltip">University of Valencia, Spain</span>
      </div>
    </div>
  </div> -->

   <!-- Licentiate in Electrical Engineering -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-3">2012 - 2017</div>
      <h3>Licentiate in Electrical Engineering</h3>
      <div class="institution-container">
        <div class="institution">University of Costa Rica</div>
        <span class="institution-tooltip">University of Costa Rica, Costa Rica</span>
      </div>
    </div>
  </div>

  <!-- Master in Electrical Engineering -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-4">2016 - 2019</div>
      <h3>Master in Electrical Engineering</h3>
      <div class="institution-container">
        <div class="institution">University of Costa Rica</div>
        <span class="institution-tooltip">University of Costa Rica, Costa Rica</span>
      </div>
    </div>
  </div>
  

  
  <div class="divider">
    <span class="divider-text">Recent Years</span>
  </div>
  
  <!-- Postdoctoral Researcher -->
  <!-- <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-5">2017 - 2025</div>
      <h3>Postdoctoral Researcher</h3>
      <div class="institution-container">
        <div class="institution">University of Bristol</div>
        <span class="institution-tooltip">University of Bristol, UK</span>
      </div>
    </div>
  </div> -->
  <!-- Intel: Product Developer Engineer -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-5">2012 - 2015</div>
      <h3>Product Developer Engineer</h3>
      <div class="institution-container">
        <div class="institution">Intel</div>
        <span class="institution-tooltip">Intel, Costa Rica</span>
      </div>
    </div>
  </div>

  <!-- Intel: Senior Software Engineer -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-5">2015 - 2019</div>
      <h3>Senior Software Engineer</h3>
      <div class="institution-container">
        <div class="institution">Intel</div>
        <span class="institution-tooltip">Intel, Costa Rica</span>
      </div>
    </div>
  </div>
    
  <!-- Botco AI (optional addition) -->
  <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-6">2019 - 2024</div>
      <h3>Full Stack Developer</h3>
      <div class="institution-container">
        <div class="institution">Botco AI</div>
        <span class="institution-tooltip">Botco AI, Costa Rica</span>
      </div>
    </div>
  </div>
  
  <!-- Senior Researcher -->
  <!-- <div class="timeline-item">
    <div class="range-connector"></div>
    <div class="timeline-content">
      <div class="timeline-period period-color-7">2017 - 2025</div>
      <h3>Senior Researcher</h3>
      <div class="institution-container">
        <div class="institution">ProtoQSAR, Ltd.</div>
        <span class="institution-tooltip">ProtoQSAR, Ltd. - Computational Chemistry Solutions</span>
      </div>
    </div>
  </div>
</div> -->

<script>
  // Script to connect ranges with items visually
  document.addEventListener('DOMContentLoaded', function() {
    const timelineItems = document.querySelectorAll('.timeline-item');
    const yearRanges = document.querySelectorAll('.year-range');
    
    timelineItems.forEach((item, index) => {
      if (index < yearRanges.length) {
        item.addEventListener('mouseenter', () => {
          yearRanges[index].style.opacity = '0.6';
          yearRanges[index].style.width = '8px';
          yearRanges[index].style.marginLeft = '-4px';
        });
        
        item.addEventListener('mouseleave', () => {
          yearRanges[index].style.opacity = '0.0';
          yearRanges[index].style.width = '4px';
          yearRanges[index].style.marginLeft = '-2px';
        });
      }
    });
  });
</script>