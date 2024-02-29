---
# Leave the homepage title empty to use the site title
title: UNSW Bioinformatics and Computational Biology
date: 2023-02-08
type: landing

sections:
  - block: hero
    content:
      title: |
        Bioinformatics and Computational Biology
        Research Group
      image:
        filename: welcome.jpg
      text: |
        <br>
        
        The **Bioinformatics and Computational Biology Research Group** has been a center of excellence for bioinformatics research, teaching, and practice since its founding in 2023. Our team comprises of multiple groups who are passionate about bioinformatics and computational biology. We are involved in a number of research projects (links), and offer projects for both honors students (link) and post-graduate students (links). We are key contact people for the Bioinformatics Degree at UNSW (link to teaching), and are happy to speak at external events (e.g., high school and career events).
    design:
      view: card 
      columns: '2'

  - block: collection
    content:
      title: Research Areas
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'
  
  - block: markdown
    content:
      title: News
      subtitle: ''
      text:
    design:
      columns: '2'
      background:
        image: 
          filename: coders.jpg
          filters:
            brightness: 1
          parallax: false
          position: center
          size: cover
          text_color_light: true
      spacing:
        padding: ['20px', '0', '20px', '0']
      css_class: fullscreen
  
  - block: markdown
    content:
      title:
      subtitle:
      text: |
        {{% cta cta_link="./people/" cta_text="Meet the team →" %}}
    design:
      columns: '2'
---