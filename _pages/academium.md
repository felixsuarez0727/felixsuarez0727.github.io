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
                <div class="card-body p-0 d-flex flex-column">
                    <!-- Project Image (Now above) -->
                    <div class="project-image-container mb-0">
                        {% include figure.liquid 
                            loading="eager" 
                            path="assets/img/arcos-lab.png" 
                            title="ARCOS-LAB Humanoid Robot" 
                            class="img-fluid w-100 h-100 object-cover rounded-start" 
                        %}
                    </div>

                    <!-- Project Details -->
                    <div class="p-4" style="color: var(--global-text-color);">
                        <div class="mb-3">
                            <span class="badge mb-3" style="background-color: var(--global-theme-color);">
                                Featured Project
                            </span>
                            <h2 class="h3 mb-3" style="color: var(--global-theme-color);">
                                Humanoid Robot Integration
                            </h2>
                            <h3 class="h5 mb-3">
                                Integración del hardware y software del robot humanoide del ARCOS-LAB de la EIE
                            </h3>

                            <div class="project-metadata mb-4">
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Author:</strong> 
                                    Félix David Suárez Bonilla
                                </p>
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Institution:</strong> 
                                    Universidad de Costa Rica, Facultad de Ingeniería
                                </p>
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Date:</strong> 
                                    February 2017
                                </p>
                            </div>

                            <p class="project-description">
                                Comprehensive research exploring the intricate integration of hardware 
                                and software components for an advanced humanoid robot developed at 
                                ARCOS-LAB, pushing the boundaries of robotics technology.
                            </p>
                        </div>

                       <!-- Button -->
                        <div class="mt-4" style="text-align:left; margin-bottom: 20px;">
                            <a href="/assets/docs/Trabajo_Final_Licenciatura_Felix_Suarez_A45276.pdf" target="_blank">
                                <button id="download-project-button" style="
                                    padding: 10px 20px;
                                    color: white; /* White text */
                                    border: none; /* No border */
                                    background-color: var(--global-theme-color); /* Solid background color */
                                    border-radius: 5px;
                                    cursor: pointer;
                                    transition: all 0.3s ease;
                                    margin-left: 0;
                                ">
                                    Download Research Paper
                                </button>
                            </a>
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

    .card {
        box-shadow: 0 10px 25px rgba(0,0,0,0.1) !important;
    }

    .card-body {
        padding: 0;
    }

    .p-0 {
        padding: 0 !important;
    }

    .mb-3 {
        margin-bottom: 1rem !important;
    }

    .row {
        margin-left: 0;
        margin-right: 0;
    }

    /* Button hover effect */
    #download-project-button:hover {
        background-color: var(--global-hover-bg-color); /* Change background color on hover */
        color: var(--global-hover-text-color); /* Change text color on hover */
    }
</style>
