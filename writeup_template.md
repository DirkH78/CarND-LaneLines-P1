# **Finding Lane Lines on the Road** 

## Writeup

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of following steps:
1) the picture is converted to grayscale
2) a triangular shaped part of the picture is defined as relevant. The rest of the picture is "grayed-out".
3) a gaussian blur filter is utilized
4) a canny is applied
5) hough transformation. It performs the following steps
        a) regular calculation of hough-lines (as done in the exercises)
        b) the lines are once again filtered with the line slope in mind and a slope-threshold is implemented


### 2. Identify potential shortcomings with your current pipeline


A major disadvantage is the fact that the irrelevant part of the picture is grayed-out. If a different roud surface will appear (fresh black tar for example) the difference between the relevant and the irrelevant area might create unwanted additional edges.


### 3. Suggest possible improvements to your pipeline

A "smooth" transition betweeen these areas could be implemented by using a vertical filter on the gray image mask before multiplying both images.
