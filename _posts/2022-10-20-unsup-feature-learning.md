---
layout: post
title:  "Self-Supervised Feature Learning for Long-Term Metric Visual Localization"
date:   2022-10-20
categories: Publications
---
<!-- Self-supervised methods have significantly closed the gap with end-to-end supervised learning for image classification. In the case of human action videos, however, where both appearance and motion are significant factors of variation, this gap remains significant. One of the key reasons for this is that sampling pairs of similar video clips, a required step for many self-supervised contrastive learning methods, is currently done conservatively to avoid false positives. A typical assumption is that similar clips only occur temporally close within a single video, leading to insufficient examples of motion similarity. To mitigate this, we propose SLIC, a clustering-based self-supervised contrastive learning method for human action videos. Our key contribution is that we improve upon the traditional intra-video positive sampling by using iterative clustering to group similar video instances. This enables our method to leverage pseudo-labels from the cluster assignments to sample harder positives and negatives. SLIC outperforms state-of-the-art video retrieval baselines by +15.4% on top-1 recall on UCF101 and by +5.7% when directly transferred to HMDB51. With end-to-end finetuning for action classification, SLIC achieves 83.2% top-1 accuracy (+0.8%) on UCF101 and 54.5% on HMDB51 (+1.6%). SLIC is also competitive with the state-of-the-art in action classification after self-supervised pretraining on Kinetics400.


 -->

<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta property="og:site_name" content="Learning To Search in Task and Motion Planning with Streams">
    <meta property="og:title" content="Learning To Search in Task and Motion Planning with Streams">
    <meta property="og:description"
        content="Learning to predict the relevance of optimistic quantities in a Task and Motion Planning Problem.">
    <meta property="og:url" content="https://rvl.cs.toronto.edu/slic">
    <meta property="og:image" content="https://rvl.cs.toronto.edu/learning-based-tamp/teaser.jpg">
    <meta property="og:image:type" content="image/jpeg">
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Learning To Search in Task and Motion Planning with Streams">
    <meta name="twitter:description"
        content="Learning to predict the relevance of optimistic quantities in a Task and Motion Planning Problem.">
    <meta name="twitter:creator" content="@eric_heiden">
    <meta name="twitter:url" content="https://rvl.cs.toronto.edu/learning-based-tamp">
    <meta name="twitter:image:src" content="https://rvl.cs.toronto.edu/learning-based-tamp/teaser.jpg">
    <!-- <meta name="description"
        content="Learning to predict the relevance of optimistic quantities in a Task and Motion Planning Problem."> -->
    <meta name="author" content="Salar Hosseini, Yuxuan Chen, Florian Shkurti">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta3/dist/css/bootstrap.min.css" rel="stylesheet"
        integrity="sha384-eOJMYsd53ii+scO/bJGFsiCZc+5NDVN2yr8+0RDqr0Ql0h+rP48ckxlpbzKgwra6" crossorigin="anonymous">
    <link rel="icon" type="image/png" href="https://rvl.cs.toronto.edu/learning-based-tamp/favicon.ico"/>
    <link rel="icon" type="image/png" href="https://rvl.cs.toronto.edu/learning-based-tamp/favicon.ico"/>
    <style>
        div.authors p:first-of-type {
            font-size: 1.4em;
        }

        div.authors p {
            text-align: center;
        }

        div.affiliations p {
            text-align: center;
        }

        h1,
        h2 {
            margin: 1em 0;
            text-align: center;
        }

        a:link {
            text-decoration: none;
        }

        #video {
            text-align: center;
        }

        div.container {
            padding-top: 60px;
        }

        .navbar {
            padding: 0.4em 2em;
        }

        #abstract p {
            text-align: justify;
        }

        #results .label {
            margin-top: 1em;
            margin-bottom: 0.3em;
            font-weight: bold;
        }

        #results h3,
        #results h5 {
            margin-top: 2em;
        }

        .btn {
            width: 75%;
        }

        .actions .col {
            text-align: center;
        }
    </style>
</head>
<body>
    <nav class="navbar navbar-expand-md navbar-light fixed-top bg-light">
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarToggle">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end position-relative" id="navbarToggle">
            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <a class="nav-link" href="#" target="_self">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#abstract" target="_self">Abstract</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#video" target="_self">Video</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#results" target="_self">Results</a>
                </li>
            </ul>
        </div>
    </nav>
    <div class="container">
        <!-- <h1>Learning to Search in Task and Motion Planning with Streams</h1> -->
        <div class="row authors">
            <div class="col">
                <p>
                    <a href="https://sherrychen127.github.io">Yuxuan Chen</a>
                </p>
            </div>
            <div class="col">
                <p>
                    <a href="http://asrl.utias.utoronto.ca/~tdb/">Timothy D. Barfoot</a>
                </p>
            </div>
        </div>
        <div class="row affiliations">
            <div class="col">
                <p><sup>1</sup>University of Toronto </p>
            </div>
            <!-- <div class="col">
                <p><sup>2</sup></p> -->
            <h2>Abstract</h2>
            Visual localization is the task of estimating camera pose in a known scene, which is an essential problem in robotics and computer vision. However, long-term visual localization is still a challenge due to the environmental appearance changes caused by lighting and seasons. While techniques exist to address appearance changes using neural networks, these methods typically require ground-truth pose information to generate accurate image correspondences or act as a supervisory signal during training. In this paper, we present a novel self-supervised feature learning framework for metric visual localization. We use a sequence-based image matching algorithm across different sequences of images (i.e., experiences) to generate image correspondences without ground-truth labels. We can then sample image pairs to train a deep neural network that learns sparse features with associated descriptors and scores without ground-truth pose supervision. The learned features can be used together with a classical pose estimator for visual stereo localization. We validate the learned features by integrating with an existing Visual Teach & Repeat pipeline to perform closed-loop localization experiments under different lighting conditions for a total of 22.4 km.
        </div>
    <div class="container" id="abstract">
        <div class="row actions">
            <div class="col"><a href="https://ieeexplore.ieee.org/abstract/document/9976214" target="_blank"
                    class="btn btn-primary ">Paper</a></div>
            <!-- <div class="col"><a href="https://github.com/rvl-lab-utoronto/video_similarity_search" class="btn btn-primary col">Code</a></div> -->
            <div class="col"><a href="#" data-bs-toggle="modal" data-bs-target="#citationModal"
                    class="btn btn-primary col">Citation</a></div>
        </div>
    </div>
    <div class="modal fade" id="citationModal" tabindex="-1" role="dialog" aria-labelledby="citationModalTitle">
        <div class="modal-dialog modal-dialog-centered" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="citationModalLongTitle">Citation</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <pre>
@ARTICLE{9976214,
  author={Y. Chen and Barfoot, Timothy D.},
  journal={IEEE Robotics and Automation Letters}, 
  title={Self-Supervised Feature Learning for Long-Term Metric Visual Localization}, 
  year={2023},
  volume={8},
  number={2},
  pages={472-479},
  doi={10.1109/LRA.2022.3227866}
}
                    </pre>
                </div>
            </div>
        </div>
    </div>
    <!-- <div class="container" id="video">
        <h2>Video</h2>
        <div class="row justify-content-md-center">
            <div class="ratio ratio-16x9 w-75">
                <iframe src="https://www.youtube.com/embed/c6fsZtD7mNg" title="YouTube video player" frameborder="0"
                    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                    allowfullscreen></iframe>
            </div>
        </div>
    </div> -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta3/dist/js/bootstrap.bundle.min.js"
        integrity="sha384-JEW9xMcG8R+pH31jmWH6WWP0WintQrMb4s7ZOdauHnUtxwoG2vI5DkLtS3qm9Ekf"
        crossorigin="anonymous"></script>
