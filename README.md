# autonomous-lidar-robot
 Autonomous mobile robot with LiDAR-based mapping, systematic coverage navigation, and obstacle avoidance

# Autonomous LiDAR-Based Mobile Robot

An autonomous mobile robot prototype designed to explore systematic coverage
navigation as an alternative to random movement patterns commonly used by
robotic lawn mowers.

**Independent engineering project · 2024–2025**

---

## Overview

Many robotic lawn mowers rely on boundary infrastructure and navigation
strategies that can produce irregular trajectories and repeated passes over
the same area.

The goal of this project was to build and experimentally test a mobile robot
capable of:

- mapping its environment using 2D LiDAR;
- navigating without external boundary infrastructure;
- using wheel odometry together with LiDAR data;
- following a systematic coverage strategy based on parallel passes;
- responding to obstacles detected during navigation.

The project resulted in a functioning physical prototype, a ROS-based
navigation system, and a virtual model of the robot.

---

## Project Idea

The original motivation was simple: instead of allowing a lawn mower to move
through an area in a largely irregular pattern, could it first understand its
environment and then cover it systematically?

The intended coverage pattern resembles the parallel passes used when mowing
sports fields:

```text
┌───────────────────────────────┐
│ → → → → → → → → → → → → → │
│                           ↓   │
│ ← ← ← ← ← ← ← ← ← ← ← ← ← │
│ ↓                             │
│ → → → → → → → → → → → → → │
│                           ↓   │
│ ← ← ← ← ← ← ← ← ← ← ← ← ← │
└───────────────────────────────┘
```

This approach was intended to reduce unnecessary repeated motion while also
producing a more regular coverage pattern.
