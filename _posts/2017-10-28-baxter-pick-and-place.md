---
date: 2017-10-28
title: Baxter Pick and Place
video_id: t8z_xwegc10
description: ITTP Project
categories:
  - deployment
resources:
  - name: "Source Code"
    link: https://github.com/BetaS/baxter_grip_object
type: Video
set: getting-started
set_order: 1
---

This is a project I with two students from South Korea through the ITTP program. I had a great time working with Minsu Kim and Yohanna Nah.

Thanks to our advisior: [Nilanjan Chakraborty](http://me.eng.sunysb.edu/people/faculty/Chakraborty_Nilanjan.html)

## Project Goals

The goal of this project was to have baxter perform pick and place operations with objects on a table. We designed an algorithm to identify red and blue objects and then allow the user to select which object to begin grasping. The algorithm then solves then uses inverse kinematics to determine the path of configurations and the pregrasp configuration. Baxter then grips the object at the center and places it at the marker location at the center of the table. This project was developed using ROS and python.

## Skills

Robot Kinematics, Redundant Manipulators, Manipulation, Computer Vision, Robot Control, Python, ROS, Baxter Research Robot.
