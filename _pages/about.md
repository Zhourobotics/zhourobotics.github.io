---
layout: about
title: Home
permalink: /
# subtitle: <a href='#'>Affiliations</a>. Address. Contacts. Moto. Etc.

# profile:
#   align: right
#   image: prof_pic.jpg
#   image_cicular: false # crops the image to make it circular
#   address: >
#     <p>555 your office number</p>
#     <p>123 your address street</p>
#     <p>Your City, State 12345</p>

news: false  # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true  # includes social icons at the bottom of the page
---


<!-- ************** Carousel ************** -->
<div id="carouselExampleIndicators" class="carousel slide carousel-fade" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#carouselExampleIndicators" data-slide-to="0" class="active"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="1"></li>
<!--     <li data-target="#carouselExampleIndicators" data-slide-to="2"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="3"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="4"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="5"></li>
    <li data-target="#carouselExampleIndicators" data-slide-to="6"></li> -->
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="assets/img/labmempic.jpg">
    </div> 
    <div class="carousel-item ">
      <img class="d-block w-100" src="assets/img/airground1.jpg">
    </div>
    <div class="carousel-item ">
      <img class="d-block w-100" src="assets/img/modalaidrone.png">
    </div> 
    <!-- <div class="carousel-item ">
      <img class="d-block w-100" src="assets/img/huskydrone.png">
    </div>   -->
    <div class="carousel-item">
      <img class="d-block w-100" src="assets/img/autodrive.jpg">
    </div>
    <div class="carousel-item ">
      <img class="d-block w-100" src="assets/img/robotarm.jpg">
    </div>  

</div>
<a class="carousel-control-prev" href="#carouselExampleIndicators" role="button" data-slide="prev">
  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
  <span class="sr-only">Previous</span>
</a>
<a class="carousel-control-next" href="#carouselExampleIndicators" role="button" data-slide="next">
  <span class="carousel-control-next-icon" aria-hidden="true"></span>
  <span class="sr-only">Next</span>
</a>
</div>


<div class="row">
    <div class="col-md-12">
        <span style="display: block; margin-bottom: 1em"></span>
        <h4> About </h4>
        The Drexel Zhou Lab aims to advance the robustness, reliability, and scalability of robotics and multi-robot systems. Our research integrates robotics and foundation models, and is driven by real-world challenges in environmental monitoring, disaster response, precision agriculture, urban mobility, and robotic manipulation. 
    </div>
</div>

<div class="row">
    <div class="col-md-12">
        <span style="display: block; margin-bottom: 1em"></span>
        <h4> News </h4>
        <div class="table-responsive">
            <table class="table table-sm table-borderless">
                <tr>
                    <th scope="row" style="padding-top: 0.1em">June 15, 2025</th>
                    <td style="padding-top: 0em; padding-left: 0">
                        Our paper on <a href="https://arxiv.org/pdf/2409.11230">resilient multi-robot tracking</a> has been accepted to IROS 2025! 
                    </td>
                </tr>
                <tr>
                    <th scope="row" style="padding-top: 0.1em">May 6, 2025</th>
                    <td style="padding-top: 0em; padding-left: 0">
                        Our paper on <a href="https://ieeexplore.ieee.org/abstract/document/10989573">game-theoretic robot allocation</a> has been accepted to TRO! 
                    </td>
                </tr>
                <tr>
                    <th scope="row" style="padding-top: 0.1em">April 14, 2025</th>
                    <td style="padding-top: 0em; padding-left: 0">
                        Our paper on <a href="https://openaccess.thecvf.com/content/CVPR2025W/WDFM-AD/html/Chahe_ReasonDrive_Efficient_Visual_Question_Answering_for_Autonomous_Vehicles_with_Reasoning-Enhanced_CVPRW_2025_paper.html">Finetuning chain-of-thought of small vision-language models for autonomous driving</a> has been accepted to <a href = "https://wdfm-ad.github.io/">CVPR 2025 WDFM-AD Workshop</a>! 
                    </td>
                </tr>
                <tr>
                    <th scope="row" style="padding-top: 0.1em">Mar 15, 2025</th>
                    <td style="padding-top: 0em; padding-left: 0">
                        Our paper on <a href="https://openaccess.thecvf.com/content/WACV2025W/LLVMAD/html/Chahe_Query3D_LLM-Powered_Open-Vocabulary_Scene_Segmentation_with_Language_Embedded_3D_Gaussians_WACVW_2025_paper.html">LLM-powered open-vocabulary scene segmentation with language embedded 3D Gaussians</a> won the <strong>Best Paper Award</strong> at the  <a href = "https://llvm-ad.github.io/WACV_2025/">WACV 2025 LLVM-AD Workshop</a>! 🎉
                    </td>
                </tr>                
            </table>
        </div>
    </div>
</div>

<div class="row">
    <div class="col-md-12">
        <span style="display: block; margin-bottom: 0.5em"></span>
        <h4> Sponsors </h4>
        <span style="display: block; margin-bottom: 1em"></span>
        <div class="row">
            <div class="col-md-5">
                {% include figure.html path="assets/img/arl.jpg" title="example image" class="img-fluid rounded z-depth-1" width="92%" %}
                <!-- <div class="caption">
                    <a href= "https://www.dcist.org/">ARL CRA DCIST</a>: Resilient and safe target tracking with heterogeneous multi-robot teams. 
                </div>     -->
            </div>
            <div class="col-md-4">
                {% include figure.html path="assets/img/faa.png" title="example image" class="img-fluid rounded z-depth-1" width="85%" %}
            </div>
            <div class="col-md-3">
                {% include figure.html path="assets/img/harmoni.png" title="example image" class="img-fluid rounded z-depth-1" width="43%" %}
            </div>     
        </div>
    </div>
</div>

<span style="display: block; margin-bottom: 0.5em"></span>

<div class='container'>
    <header class="masthead text-center">
      <span style="display: block; margin-bottom: 4em"></span>
      <i class="fab fa-youtube"></i> <a href= "https://www.youtube.com/channel/UCPw3Yjm2b7bioxqOJbdVrEA" target="_blank"> ZhouLab </a> &nbsp;&nbsp;&nbsp;
      <i class="fab fa-linkedin"></i> <a href= "https://www.linkedin.com/in/lifeng-zhou-18135aa6/" target="_blank"> Lifeng Zhou </a> &nbsp;&nbsp;&nbsp;
      <i class="fab fa-twitter"></i> <a href= "http://twitter.com/lfzhou917" target="_blank"> lfzhou917 </a> &nbsp;&nbsp;&nbsp;
      <i class="fab fa-github"></i> <a href= "https://github.com/Zhourobotics" target="_blank"> ZhouLab </a>
      <br>

      <a href= "https://drexel.edu/engineering/academics/departments/electrical-computer-engineering/"> Department of Electrical and Computer Engineering </a> at <a href= "https://drexel.edu/">Drexel University</a><br>
      506 Bossone Research Building, 3140 Market Street, Philadelphia, PA 19104
      <span style="display: block; margin-bottom: 3em"></span>
    </header>
</div>