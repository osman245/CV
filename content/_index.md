---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: skills
    content:
      title: Skills
      text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
      username: admin
    design:
      columns: '1'
  - block: accomplishments
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Accomplish&shy;ments'
      subtitle:
      # Date format: https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: https://www.credly.com/badges/d4f42dea-78fd-43c3-8eaa-bcb174ed1e6b/public_url
          date_end: ''
          date_start: '2023-08-12'
          description: ''
          icon: dharmachakra
          organization: Linux Foundation
          organization_url: https://www.linuxfoundation.org/
          title: Certified Kubernetes Application Developer
          url: ''
        - certificate_url: https://www.aws.training/certification
          date_end: ''
          date_start: '2024-12-15'
          description:
          icon: aws
          organization: Amazon Web Services
          organization_url:
          title: AWS Certified Developer Associate
          url: ''
        - certificate_url: https://www.aws.training/certification
          date_end: ''
          date_start: '2024-12-30'
          description: ''
          icon: aws
          organization: Amazon Web Services
          organization_url:
          title: AWS Certified Cloud Architect Associate
          url: ''
        - certificate_url: https://www.aws.training/certification
          date_end: ''
          date_start: '2024-12-12'
          description: ''
          icon: terraform
          organization: HashiCorp
          organization_url:
          title: HashiCorp Certified Terraform Associate
          url: ''

    design:
      # Choose a layout view
      view: compact
      columns: '4'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Kubernetes
          tag: kubernetes
    design:
      columns: '2'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Feel free to contact me
      # Contact (add or remove contact options as necessary)
      email: osm.warsame@gmail.com
      appointment_url: 'https://calendly.com/osm-warsame'
    autolink: true
    form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---  
