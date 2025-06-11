---
title: Distributed Fractals
date: 2025-06-10 12:00:00 -0300
categories: [Computer graphics, tool]
tags: [
    tool, 
    computer graphics, 
    fractal,
    mpi,
    c++,
    cmake,
    open source,
    parallel programming]     
description: Clustered fractal renderer

image:
  path: /assets/distributed_fractals/sample.gif
---

Distributed fractals is a command-line application for rendering fractals (Such as Mandelbrot and Julia) using CPU-based parallelism with MPI. This approach makes it suitable for both local and distributed rendering setups. You can find the [source code on GitHub](https://github.com/FrancoYudica/DistributedFractals).

![](/assets/distributed_fractals/horizontal.png)

I've always wanted to learn about fractal rendering and with this project, I finally did. I was also eager to explore cluster programming and MPI, so I decided to combine both goals into a single challenge.

What I learned:
- Applying [MPI](https://www.open-mpi.org/) in a real-world project.
- Setting up and managing a compute cluster.
- Implementing a Master-Worker architecture with dynamic task pulling for improved load balancing.
- Exploring fractal mathematics and coloring techniques.
- Understanding the impact of numerical precision limits at high zoom levels.
- Leveraging [`mpfr`](https://www.mpfr.org/) for arbitrary-precision arithmetic.
- Profiling performance using tools like [`perf`](https://perfwiki.github.io/main/), [`Score-P`](https://www.vi-hps.org/projects/score-p/), and visualizing results with [`vampir`](https://vampir.eu/).

I've also written a [whitepaper](https://github.com/FrancoYudica/DistributedFractals-Whitepaper/releases) detailing the project (in Spanish).

## Sample video
{% include embed/youtube.html id='RaeWO0s3MXI' %}

