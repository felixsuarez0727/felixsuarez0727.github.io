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
        <div class="col-lg-10 col-md-12 px-3 px-md-4">
            <!-- Featured Project Card -->
            <div class="card border-0 shadow-lg mb-5" style="background-color: var(--global-card-bg-color);">
                <div class="card-body p-0">
                    <!-- Project Image -->
                    <div class="project-image-container">
                        {% include figure.liquid 
                            loading="eager" 
                            path="assets/img/arcos-lab.png" 
                            title="ARCOS-LAB Humanoid Robot" 
                            class="img-fluid w-100 object-cover rounded-top" 
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
                                Integration of the hardware and software of the humanoid robot from ARCOS-LAB of the EIE.
                            </h3>

                            <div class="project-metadata mb-4">
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Author:</strong> 
                                    Félix David Suárez Bonilla
                                </p>
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Institution:</strong> 
                                    University of Costa Rica, Faculty of Engineering
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
                        <div class="mt-4 text-left mb-3">
                            <a href="/assets/docs/Trabajo_Final_Licenciatura_Felix_Suarez_A45276.pdf" target="_blank" class="btn-download">
                                Download Research Paper
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- New Project: Business Plan for DevDen -->
            <div class="card border-0 shadow-lg mb-5" style="background-color: var(--global-card-bg-color);">
                <div class="card-body p-0">
                    <div class="project-image-container">
                        {% include figure.liquid 
                            loading="lazy" 
                            path="assets/img/devden-business-plan.png" 
                            title="DevDen" 
                            class="img-fluid w-100 object-cover rounded-top" 
                        %}
                    </div>
                    <div class="p-4" style="color: var(--global-text-color);">
                        <div class="mb-3">
                            <span class="badge mb-3" style="background-color: var(--global-theme-color);">
                                Business Plan
                            </span>
                            <h2 class="h3 mb-3" style="color: var(--global-theme-color);">
                                Business Plan for DevDen
                            </h2>
                            <h3 class="h5 mb-3">
                                Master's Final Project
                            </h3>

                            <div class="project-metadata mb-4">
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Author:</strong> 
                                    Félix Suárez Bonilla
                                </p>
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Institution:</strong> 
                                    Polytechnic University of Valencia
                                </p>
                                <p class="mb-2">
                                    <strong style="color: var(--global-theme-color);">Date:</strong> 
                                    July 2024
                                </p>
                            </div>

                            <p class="project-description">
                                This document presents the business plan for DevDen, an academic initiative in the field of specialized technology education. The master's final project details the structure, strategy, and projections of DevDen as an integrated training program for Full Stack developers.
                            </p>
                        </div>

                        <!-- Button -->
                        <div class="mt-4 text-left mb-3">
                            <a href="/assets/docs/Trabajo_Final_Master_Felix_Suarez.pdf" target="_blank" class="btn-download">
                                Download Research Paper
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    /* Base styles */
    .academium-page {
        padding-top: 2rem;
        padding-bottom: 2rem;
    }
    
    .object-cover {
        object-fit: cover;
        width: 100%;
        height: 300px;
    }
    
    .card {
        overflow: hidden;
        box-shadow: 0 10px 25px rgba(0,0,0,0.1) !important;
        transition: transform 0.3s ease;
    }
    
    .card:hover {
        transform: translateY(-5px);
    }
    
    /* Text and content formatting */
    .project-description {
        font-size: 1rem;
        line-height: 1.6;
    }
    
    /* Download button styling */
    .btn-download {
        display: inline-block;
        padding: 10px 20px;
        color: white;
        background-color: var(--global-theme-color);
        border-radius: 5px;
        text-decoration: none;
        font-weight: 500;
        transition: all 0.3s ease;
    }
    
    .btn-download:hover {
        background-color: var(--global-hover-color, #0056b3);
        text-decoration: none;
        color: white;
        transform: translateY(-2px);
        box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    
    /* Badges */
    .badge {
        padding: 0.5rem 1rem;
        font-weight: 500;
        font-size: 0.85rem;
        display: inline-block;
    }
    
    /* Responsive adjustments */
    @media (max-width: 768px) {
        .object-cover {
            height: 200px;
        }
        
        .card {
            margin-left: 10px;
            margin-right: 10px;
        }
        
        h2.h3 {
            font-size: 1.5rem;
        }
        
        h3.h5 {
            font-size: 1.1rem;
        }
        
        .project-metadata p {
            font-size: 0.9rem;
        }
    }
    
    @media (max-width: 576px) {
        .object-cover {
            height: 150px;
        }
        
        .p-4 {
            padding: 1rem !important;
        }
        
        .btn-download {
            width: 100%;
            text-align: center;
        }
        
        h2.h3 {
            font-size: 1.3rem;
        }
    }
</style>