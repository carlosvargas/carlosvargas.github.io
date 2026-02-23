
  ---
  layout: post
  date: 2026-02-22 20:40 -0800  
  title: Using Django ORM Without a Project 
  linkblog: true
  tags: [db]
  ---
  
Paulo has a post about using [Django ORM Standalone](https://www.paulox.net/2026/02/20/django-orm-standalone-database-inspectdb-query/). 
This is a pretty ingenious idea. You still need to install Django since you need some of the core libraries, but you don't need to initialize a project, admin, etc. It allows you to do some reverse engineering to generate Django models and then query the data using these models.