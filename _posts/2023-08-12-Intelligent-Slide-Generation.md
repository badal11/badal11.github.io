---
layout: post
title: Video to Slides Converter, Transform Video Lectures into Slide Presentations
date: 2023-07-12 09:56:00-0400
description: This is a simple video-to-slide converter application that aims to obtain slide images (or pdf) given slide or lecture videos.
tags: project
categories: Deep_Learning
giscus_comments: false
related_posts: false
featured: true
# related_publications: einstein1950meaning, einstein1905movement
---

# Video to Slides Converter: Transform Video Lectures into Slide Presentations

This is a simple video-to-slide converter application that aims to obtain slide images (or pdf) given slide or lecture videos.

This is highly useful when one wishes to have a video lecture(with or without animations) in the form of slides – either a ppt or pdf. However, more often than not, slides are not provided when such video lectures are hosted on platforms like YouTube. This project aims to build a robust application that can convert video lectures into corresponding slides using techniques such as basic frame differencing and statistical background subtraction models such as **KNN** or **GMG**.

This project converts video frames into slide PDFs. Here's a step-by-step explanation of how the code works:

1. **Argument Parsing:**
    - The script uses the `argparse` module to handle command-line arguments. Various parameters, such as the input video path (`video_path`), output directory (`out_dir`), background subtraction type (`type`), hash function (`hash-func`), hash size (`hash-size`), similarity threshold (`threshold`), queue length (`queue-len`), and flags for post-processing (`no_post_process`) and PDF conversion (`convert_to_pdf`), can be specified.

2. **Argument Validation:**
    - The script validates certain arguments, such as ensuring that the queue length is positive and handling the case where it's not. It also checks if the provided video path is a valid URL or an existing file.

3. **Video Download (if URL provided):**
    - If the provided video path is a URL, the script attempts to download the video using the `download_video` function. If successful, it sets a flag (`temp_file`) to indicate that a temporary file was created.

4. **Output Directory Creation:**
    - The script creates the output directory for storing the resulting slides. The directory is created based on the input video path and the chosen background subtraction type.

5. **Background Subtraction and Slide Capture:**
    - Depending on the specified background subtraction type, the script calls either `capture_slides_frame_diff` (for frame differencing) or `capture_slides_bg_modeling` (for Gaussian Mixture Model - GMG or K-Nearest Neighbors - KNN background subtraction).

6. **Post-Processing (Duplicate Removal):**
    - If post-processing is not disabled (`no_post_process` is not set), the script performs post-processing using difference hashing to identify and remove duplicate slides.

7. **PDF Conversion (Optional):**
    - If the `convert_to_pdf` flag is set, the script converts the captured slides in the output directory to a PDF file using the `convert_slides_to_pdf` function.

8. **Temporary File Cleanup (if created):**
    - If a temporary file was created during video download (`temp_file` is set), it is removed after processing.

The script utilizes modular functions from other Python files (`config.py`, `download_video.py`, `bg_modeling.py`, `frame_differencing.py`, `post_process.py`, and `utils.py`) for specific tasks like downloading videos, capturing slides, performing background modeling, and post-processing. 