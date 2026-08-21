---
layout: profiles
permalink: /team/
title: Team
nav: true
nav_order: 2

profiles:
  # if you want to include more than one profile, just replicate the following block
  # and create one content file for each profile inside _pages/
  - align: left
    image: portraits/harsh/01-0086-07032026 cropped.jpg
    alt: "Portrait of Prof. Harsh Bhundiya"
    content: team/harsh.md
    image_circular: false # crops the image to make it circular
    more_info: >
      <span style="font-size: 1.25rem; font-weight: 700;">Harsh Bhundiya</span> <br>
      **Assistant Professor** <br>
      <a href="/assets/pdf/HarshBhundiyaCV.pdf" target="_blank" rel="noopener">Curriculum Vitae</a>
      <a href="mailto:bhundiya@umd.edu">bhundiya@umd.edu</a> <br>

  - align: left
    image: portraits/current/JoseMorel_NASA.jpeg
    alt: "Portrait of PhD student José Morel"
    content: team/josemorel.md
    image_circular: false
    more_info: >
      <span style="font-size: 1.25rem; font-weight: 700;">José Morel</span> <br>
      **PhD Student** <br>

  - align: left
    image: portraits/current/SamOndrusek.jpg
    alt: "Portrait of PhD student Sam Ondrusek"
    content: team/samondrusek.md
    image_circular: false
    more_info: >
      <span style="font-size: 1.25rem; font-weight: 700;">Sam Ondrusek</span> <br>
      **PhD Student** <br>
    
  # ADD STUDENTS

_styles: |
  @media (min-width: 576px) {
    .profile {
      width: 20%;
      max-width: 180px;
    }
  }
  /* Mobile: ensure 50% width override applies */
  @media (max-width: 575.98px) {
    .profile {
      width: 40% !important;
      max-width: 180px;
    }
  }
---