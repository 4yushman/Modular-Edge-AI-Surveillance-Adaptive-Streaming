# Modular Edge-AI Framework for Surveillance and Adaptive Video Transmission

A proposed modular edge-AI layer for traffic analytics and adaptive video representation using compatible video sources.

## Problem

Existing recording systems may lack the traffic analytics needed for a particular application. Sending complete video can also consume bandwidth on regions that are less relevant. This project explores adding configurable analytics and selecting relevant video tiles without replacing a compatible camera.

## Proposed architecture

The initial prototype uses the same recorded video in two branches:

1. **Traffic analytics:** YOLOv8n vehicle detection, ByteTrack tracking, and configurable counting, direction and wrong-way rules.
2. **Adaptive tiles:** bitrate and temporal features with fixed and adaptive thresholds and logistic regression for tile selection. A Tiny GRU is an optional extension.

The intended outputs are an annotated full-frame video and a tile-filtered representation. Modules may run sequentially or time-share the laptop. A visual tile mask alone does not demonstrate bandwidth savings: encoded output sizes must be measured.

## Current status

The synopsis has been submitted. Prototype development is planned; no implementation or performance results are claimed yet. The development target is a laptop using recorded video; compatibility with live sources can be explored later.

## Planned technology

Python, YOLOv8n, ByteTrack, OpenCV and FFmpeg; HEVC tiling and lightweight classifiers will be evaluated as the prototype develops.

## Setup

Setup and run instructions will be added once the prototype and its dependencies have been verified.

## Scope and evaluation

The project will evaluate traffic analytics, tile preservation, encoded data volume and computational cost. It does not guarantee real-time performance, universal camera compatibility or Raspberry Pi performance. Server and storage integration are outside the main demo.

## Synopsis

The submitted synopsis is available at `docs/synopsis/Submitted-Synopsis.pdf`.
