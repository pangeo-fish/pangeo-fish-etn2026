---
# File metadata may be provided as frontmatter YAML
title: Fish geolocation with Pangeo-Fish
subtitle: ETN Symposium 2026
description: Hands-on workshop of the European Tracking Network (ETN) Symposium 2026 on analysing biologging (archival tag and acoustic telemetry) data with pangeo-fish and the Pangeo ecosystem, running on the Pangeo@EOSC JupyterHub.
date: 2026-10-15
authors:
  - id: tinaok
    name: Tina Erica Odaka
    orcid: 0000-0002-1500-0156
    corresponding: true
    roles:
      - Pangeo-Fish
    affiliations:
      - ifremer
affiliations:
  - id: ifremer
    name: IFREMER
    city: Brest
    country: France
    url: https://www.ifremer.fr
    ror: https://ror.org/044jxhp58
tags:
  - pangeo
  - pangeo-fish
  - biologging
  - fish-tracking
  - HEALPix
thumbnail: images/pangeo-fish-logo.png
---

# Fish geolocation with Pangeo-Fish

+++ {"part":"abstract"}

Biologging tags (data storage tags, pop-up satellite tags) and acoustic telemetry produce long time series of temperature, pressure and detection events, but no direct position. [pangeo-fish](https://github.com/pangeo-fish/pangeo-fish) is an open source Python package built on the Pangeo ecosystem (Xarray, Dask, HEALPix) that reconstructs the most probable trajectory of a tagged fish by comparing the tag records with an ocean reference model. This hands-on workshop of the [ETN Symposium 2026](https://europeantrackingnetwork.org/) introduces the Pangeo ecosystem and walks participants through a complete pangeo-fish geolocation workflow, from loading a tag to visualising the estimated track, on the Pangeo@EOSC cloud platform. No installation is needed: everything runs in your web browser.

+++

# Time, location and registration

The workshop takes place on **Thursday 15 October 2026, 15:00 - 16:00 CET**, as one of the concurrent workshops of the [ETN Symposium 2026](https://europeantrackingnetwork.org/) (see the [symposium schedule](https://europeantrackingnetwork.org/sites/europeantrackingnetwork.org/files/managed/ETN%20Symposium/etn_symposium_2026_schedule_0.pdf)).

Venue: **B!NGS Copenhagen**, Vesterbrogade 149, 1620 København, Denmark.

Please follow the [registration to Pangeo@EOSC](users-getting-started) steps **before** the workshop: the approval of your enrollment is done manually and may take some time.

# Overview

In this workshop, participants will learn how to 1) navigate the Pangeo ecosystem (Xarray, Dask, HEALPix) for scalable analysis of ocean data and 2) use [pangeo-fish](https://pangeo-fish.readthedocs.io/) to geolocate a tagged fish from its biologging data (temperature, pressure) and acoustic detections, using an ocean reanalysis from the Copernicus Marine Service as reference.

All the training material is developed collaboratively and made available online with a CC-BY-4 licence. To facilitate user on-boarding, the [Pangeo@EOSC](https://pangeo-data.github.io/pangeo-eosc/) platform is made available to participants, with a ready-to-use Docker image containing pangeo-fish. However, all the information needed to set up and run the training material on other platforms is provided too.

## Learning objectives

By the end of this workshop, learners will be able to:
- Understand the Pangeo ecosystem and its role in scalable analysis of oceanographic and biologging data.
- Open, explore and visualise an ocean model (GLORYS, from the Copernicus Marine Service) with Xarray, scale the computation with Dask and save results as Zarr.
- Understand what HEALPix is (an equal-area Discrete Global Grid System), why pangeo-fish uses it, and how to convert and plot data on it with xdggs.
- Run the pangeo-fish geolocation workflow on a biologging tag: compare the tag with a reference model, build emission probabilities, add acoustic detections, optimise and visualise the estimated trajectory.

## Prerequisites

Before starting this workshop, learners should have:

- Basic knowledge of R or another programming language (no Python experience is required: the notebooks are written for R users);
- Basic knowledge of biologging / fish tracking data (data storage tags, acoustic telemetry);
- A [Copernicus Marine Service](https://data.marine.copernicus.eu/register) account (free), used by the pangeo-fish notebook to download the reference ocean model.

## Set up

If you are participating in this workshop as part of the ETN Symposium 2026, you will run the notebooks on [Pangeo@EOSC](https://pangeo-data.github.io/pangeo-eosc/). Please register following the instructions given in [Registration to Pangeo@EOSC](users-getting-started) **before the workshop**. If you wish to continue using the Pangeo@EOSC infrastructure after the workshop, you can keep using the same account.
