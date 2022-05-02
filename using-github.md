---
layout: docs
title: "Documentation Site Guide | Using GitHub"
---

## Using GitHub

A GitHub repository is a central storage space to save all the files associated with a set of documentation, and where all of the versions of those files can be accessed. Each set of documentation will be added to its own GitHub repository, which will be leveraged by the[ ](https://github.com/RockefellerArchiveCenter/docs-theme)[docs-build](https://github.com/RockefellerArchiveCenter/docs-build) repository to create the docs.rockarch.org site and enable us to separate public and private documentation.

To add and manage files in a GitHub repository, become familiar with the principles of version control and Git. Here are some helpful outside resources to get started:

[A Visual Introduction to Git](https://medium.com/@ashk3l/a-visual-introduction-to-git-9fdca5d3b43a). A visual guide from Ashley Keller.

[Understanding the GitHub Flow](https://guides.github.com/introduction/flow/). GitHub guide to the basic workflow

[Learn Git](https://www.codecademy.com/learn/learn-git). Code Academy course to learn the basics of the Git workflow

[A Beginner’s Guide to Git — How to Write a Good Commit Message](https://www.freecodecamp.org/news/a-beginners-guide-to-git-how-to-write-a-good-commit-message/). Short post on the basics of writing meaningful commit messages.

## Get Started with GitHub

To work with GitHub:
1. Create or have an existing GitHub account. [Sign up for GitHub](https://github.com/).
2. Send the username to a member of the Digital Programs Team to add the new user as a member to the [RAC GitHub](https://github.com/RockefellerArchiveCenter) Organization.
3. Work with GitHub in one of three ways: directly in the browser, locally using GitHub Desktop, or from the command line:
  * [Guide to using GitHub in the browser](https://pixelpioneers.co/blog/2017/using-github-without-the-command-line)
  * [Install GitHub Desktop](https://help.github.com/desktop/guides/getting-started-with-github-desktop/installing-github-desktop/) to work with GitHub from a user interface on a computer desktop.
  * [Install Git](https://git-scm.com/) to work from the command line

## Create a Repo

[Create a Repo Instructions](https://help.github.com/articles/create-a-repo/) from GitHub.

1. Choose a template: use `RockefellerArchiveCenter/docs-template`.
2. Designate the owner as the Rockefeller Archive Center.
3. Format the name using lowercase letters and dashes between words "short-name" (e.g. processing-manual).
4. Add a short description of the documentation.
5. Choose to make the repo public or private based on its pre-approved designation (see the [Rockefeller Archive Center Documentation Site Content Approval Policy](http://docs.rockarch.org/docs-policy/)). The designation must be approved by the RAC Assistant Director for the relevant function area, and documentation that is made publicly available must also be approved by the Director of Archives.
6. Add a [GitHub Webhook](https://docs.github.com/en/developers/webhooks-and-events/webhooks/about-webhooks) to the repository. Webhooks are added in the Settings page of a repository. The Webhook listens for `push` events which push the updates to the development and production servers, and it should point to the AWS API Gateway endpoint for the `build_docs_site_api`. Contact the Head of Digital Strategies for the token and AWS Gateway endpoint URL you will need as part of the webhook configuration. For more information, see the [Documentation Site Info Sheet](https://docs.rockarch.org/systems-info-sheets/documentation-site-info-sheet/).
7. Add the documentation to the [docs-build repositories.yml](https://github.com/RockefellerArchiveCenter/docs-build/blob/base/repositories.yml) file so that the documentation will be built. If the documentation is not approved for the public site, add it only under the `private` list in the repositories.yml file. If it is approved to be public, add it under both the `private` and `public` lists in the repositories.yml file. Documentation should be added to the repositories.yml file as RockefellerArchiveCenter/(name of the documentation).
8. A [README file](/docs-guide/add-content#readme), as specified in this documentation, is included in the template.
9. A [License](/docs-guide/add-content#license), as specified in this documentation, is included in the template.
