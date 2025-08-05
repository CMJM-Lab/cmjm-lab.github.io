---
layout: default
title: Home
---

<!-- Hero Section with Latest News Side by Side -->
<section class="bg-light py-12">
  <div class="container d-flex flex-wrap">
    <!-- Image Section -->
    <div class="col-md-10 text-center">
    <img src="{{ '/assets/img/home/summary.png' | relative_url }}" alt="Lab Summary" class="img-fluid my-4" style="max-width: 80%; height: auto; display: block; margin: 0 auto;">
    <p class="lead">The Computational Multidata Junction in Medicine (CMJM, led by Prof. Chen, Mei-Ju May) Lab is dedicated to advancing human health through integrative bioinformatics and cutting-edge research. 
    We are proudly affiliated with the International College of National Taiwan University, specializing in Smart Medicine and Health Informatics. 
    Our work spans multi-omics data analysis (DNA, RNA, epigenetics, proteomics), single-cell and spatial transcriptomics, AI-driven healthcare solutions, and multimodal data integration. 
    By combining computational innovation with biomedical applications, we strive to propel precision medicine and translational research forward. 
    At CMJM Lab, we harness advanced technologies and machine learning to address complex biomedical challenges, with a particular emphasis on human cancer, ceRNA networks, and immuno-oncology, transforming data into actionable medical insights.</p>
    <p class="lead">Our team thrives in a dynamic, international environment, collaborating with members and partners from around the world. With English as our primary language of communication, we ensure seamless collaboration across diverse areas of expertise. 
    We are actively seeking passionate individuals to join our team, including research assistants, master's students, PhD candidates, and postdoctoral researchers. 
    If you are eager to contribute to groundbreaking biomedical research in a vibrant setting, we encourage you to connect with us and explore the opportunities available.</p>     
    </div>

    <!-- Latest News Section -->
    <div class="col-md-2 bg-light p-3" style="border-left: 2px solid #ddd;">
    <div class="text-center">
        <p class="lead">We are actively seeking talented individuals!
        <a href="javascript:void(0);" onclick="this.href='mailto:' + 'mjmchen' + '@' + 'g.ntu.edu.tw';" class="btn btn-primary" style="background-color: rgb(45, 159, 161); border-color: rgb(45, 159, 161);">Join Us</a>    </p>
    </div>
    <h2>Latest News</h2>
    <ul>
        {% for item in site.data.news %}
        <li>
            <strong>{{ item.date }}</strong>: {{ item.title }}
        </li>
        {% endfor %}
    </ul>
    </div>
  </div>
</section>
