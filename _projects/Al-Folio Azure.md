---
layout: page
title: Al-Folio Azure Deployment
description: This website's deployment to Azure Static Web Apps
img: assets/img/code.jpg
importance: 2
category: work
---

Needing a personal website as a portfolio as well as a place to document projects, I evaluated two options: a custom-built website or a sufficiently powerful template. After exploring <a href="https://github.com/alshedivat/al-folio">Al-Folio</a>, I determined that it was exactly what I needed.

I chose to deploy it on Azure Static Web Apps to gain hands-on experience with the platform while taking advantage of the free tier. Since this wasn't a documented deployment method for Al-Folio, it presented an interesting technical challenge.

## What went wrong

After creating my <a href="https://github.com/AdaVoden/personal_website">personal website repository</a> and configuring Azure Static Web Apps, I encountered issues with Oryx (Azure's build tool). Every Build and Deploy job in GitHub Actions failed with the error: "Could not find either 'build' or 'build:azure' node under 'scripts' in package.json."

Adding the build command to `package.json` didn't resolve the issue. Instead, it introduced a new error where Oryx was unable to install the gemfiles necessary to build the Jekyll site.

## How I figured it out

I spent time learning how GitHub Actions worked while troubleshooting the Oryx build failures. When I noticed the failing command was pulling a build action from Microsoft's Azure GitHub repository, I went directly to the source documentation.

The documentation revealed I could disable Oryx entirely using the `skip_app_build` flag and rely on Al-Folio's existing build action instead. I merged the two workflows and disabled Oryx's build process. This yielded the result you are looking at now, success.

## What I learned

This project taught me a substantial amount about Github Actions and how automated builds with Docker and Github Actions works in general. I'm proud that I was able to deploy this site with an undocumented method by exploring documentation, logs and experimenting with different approaches.
