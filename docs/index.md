---
# markdownlint-disable
# vale  off
layout: default
nav_order: 1
# tags used by AI files
description: Describes the Tune Guide API for a new user
tags: 
    - introduction
categories: 
    - tutorial
ai_relevance: high
importance: 9
prerequisites: []
related_pages: 
    - /before-you-start-a-tutorial 
    - /tutorials/add-a-new-task
    - /tutorials/enroll-a-new-user
    - /tutorials/update-a-user-by-id
examples: []
api_endpoints: []
version: "v1.0"
last_updated: "2025-10-25"
# vale  on
# markdownlint-enable
---


# Tune Guide API

Tune Guide API aggregates SiriusXM channel, music schedule, and show information.

**Note**: This is a mock API to simulate the REST interface of an imaginary service.

## What is the Tune Guide API?

TuneGuide is a Rest API that integrates music channel listings and show information into one accessible, easy-to-use API.

## What is the purpose of the Tune Guide API?

The purpose of the API is to allow users to search for music channels based on their preferred genre and find shows hosted on these channels that match their music tastes. The API does this by aggregating SiriusXM music channels genre and show scheduling information. This integration enables end users to source scheduling details for their favourite music, genres, channels, and shows.

## Who uses the Tune Guide API?

Developers integrating the TuneGuide API into music-centric applications for music-loving end users. Use cases for Tune Guide are mobile apps, car infotainment systems and music web platforms.

## What are the benefits of using the Tune Guide API?

- For developers: TuneGuide eliminates the need to scrape or manually maintain programming schedules.
- For end users: TuneGuide presents their SiriusXM music channel information in a single location, where they can filter to suit their own music taste and find shows that interest them.

## What resources does the Tune Guide API provide?

- **Channels**
  - channel number
  - channel name
  - genre
  - description
  - target_audience

- **Shows**
  - show name
  - host
  - air time PDT
  - day of week
  - duration mins
  - channel number

## How to get started

See:

- [Before you start a tutorial](tutorials/before-you-start-a-tutorial.md)
- [Tutorials](tutorials/tutorials.md)

## Learn More

You can use the Tune Guide API reference documentation for detailed descriptions of the service's resources.

The API reference docs refer to a `{base_url}` when they refer to the URL of a resource. The `{base_url}` value depends on the installation of the service.

When run locally for testing, the `{base_url}` is generally `http://localhost:3000`.

See:

- [channels resource](https:)
- [shows resource](https:)

## Contact us

**Support Email**: `tune-guide@gmail.com`

**Support Phone Number**: 1-215-693-2308

**Address**: 123 Sirius St., Seattle, WA, USA
