# Event Shift in Flood Prediction

A project page about flood prediction under event shift: training on one flood event and predicting another later event.

## Project Website

[View Project Site](https://mah-trigui.github.io/event-shift-in-flood-prediction/)

## Overview

This project predicts the fraction of 1km² squares flooded in Malawi during a later flood event, using training data from an earlier flood.

That makes the main challenge different from ordinary supervised learning.

The issue is not only generalization across rows.

It is generalization across events.

## Core Idea

When train and test come from different floods, some signals transfer better than others.

Event-specific rainfall detail may not generalize well from one storm to another.

Physical landscape structure is more stable:
- terrain shape
- flow direction
- roughness
- soil drainage and infiltration

So the feature strategy prioritized invariant spatial controls over the fingerprint of a single past event.

## Why it matters

- event shift is different from random train/test splitting
- physically stable features often transfer better than historical event details
- feature quality under shift depends on transferability, not only predictive power
- the principle generalizes to wildfire, drought, storm, and environmental risk modeling

## Architecture

![Architecture](images/architecture.jpg)

## Key Takeaway

**When train and test are different events, favor signals that survive the shift.**

## Public Scope

This repository shares the core modeling principle, selected implementation details, and project presentation only.
