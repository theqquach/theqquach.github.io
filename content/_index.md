---
# Leave the homepage title empty to use the site title
title: 'Home'
date: 2024-10-24
type: landing

sections:
  - block: resume-biography
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text:
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: background.png
          filters:
            brightness: 0.4
          size: cover
          position: center
          parallax: false
  - block: markdown
    content:
      title: 'About me'
      subtitle: ''
      text: |-
        I am a student at the University of British Columbia where I am currently majoring in Statistics & Economics.

        My areas of interests include:

        - Financial Economics
        - Data Science
        - Political Economy and Public Policy
        - Environmental Economics and Sustainability
        - Econometrics and Quantitative Methods

        I'm passionate about using a data-driven approach to explore relationships, answer questions, and provide meaningful recommendations. Although I am most experienced working with financial data, I am always excited to work with different datasets and learn about different industries and projects, as I believe in lifelong learning.
    design:
      columns: '1'
      spacing:
          is_fullscreen: true
          padding: ['50px', '0px', '50px', '0px']
  - block: cta-button-list
    content:
      buttons:
        - text: Download CV
          url: /uploads/resume.pdf
    design:
      columns: '1'
      spacing:
          is_fullscreen: true
          padding: ['50px', '0px', '50px', '0px']
---
