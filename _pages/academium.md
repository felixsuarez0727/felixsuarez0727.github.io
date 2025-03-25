---
layout: page
title: Academium
permalink: /academium/
description: Explore a selection of final graduation projects, showcasing academic research and innovation.
nav: true
nav_order: 5
horizontal: true
---

<div class="container-fluid academium-page py-5">
    <div class="row justify-content-center">
        <div class="col-lg-10">
            <!-- Featured Project Card -->
            <div class="card border-0 shadow-lg mb-5" style="background-color: var(--global-card-bg-color);">
                <div class="card-body p-0">
                    <div class="row g-0 align-items-stretch">
                        <!-- Project Image -->
                        <div class="col-md-5 project-image-container">
                            {% include figure.liquid 
                                loading="eager" 
                                path="assets/img/arcos-lab.png" 
                                title="ARCOS-LAB Humanoid Robot" 
                                class="img-fluid w-100 h-100 object-cover rounded-start" 
                            %}
                        </div>
                        
                        <!-- Project Details -->
                        <div class="col-md-7">
                            <div class="p-4 d-flex flex-column h-100" style="color: var(--global-text-color);">
                                <div class="mb-auto">
                                    <span class="badge mb-3" style="background-color: var(--global-theme-color);">
                                        Featured Project
                                    </span>
                                    <h2 class="h3 mb-3" style="color: var(--global-theme-color);">
                                        Humanoid Robot Integration
                                    </h2>
                                    <h3 class="h5 mb-3">
                                        Integración del hardware y software del robot humanoide del ARCOS-LAB de la EIE
                                    </h3>

                                    
                               
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</div>

<style>
    .object-cover {
        object-fit: cover;
        width: 100%;
        height: 100%;
    }

    .project-image-container {
        min-height: 400px;
        max-height: 600px;
        overflow: hidden;
    }

    .card {
        box-shadow: 0 10px 25px rgba(0,0,0,0.1) !important;
    }
</style>