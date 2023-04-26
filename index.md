---
layout: docs
title: "Documentation Site Guide to Managing Content"
---

## Purpose

This is a guide to managing RAC documentation, including adding to a RAC GitHub repository, converting content to the Markdown format, and editing in Markdown. For the policy that defines the approval process by which documentation is selected, designated as internal or external, and added to docs.rockarch.org, refer to the [Rockefeller Archive Center Documentation Site Content Approval Policy](https://docs.rockarch.org/docs-policy/).

## Platform Structural Overview

The RAC Documentation Site is a[ static website](https://techterms.com/definition/staticwebsite). RAC staff will add documentation to the site via a repository on the[ RAC’s GitHub](https://github.com/RockefellerArchiveCenter) that is designated for that set of documentation. A static site generator called[ Jekyll](https://jekyllrb.com/) converts the raw text files that comprise the documentation (ie. Markdown files) to HTML, and the site files will be deployed. There are three relevant URLs where content is deployed:
1. https://docs.rockarch.org/: the public site which is available on the open web and does not include any internal documentation.
2. https://docs-internal.rockarch.org/: the internal site which is only available on RAC networks, and contains internal-facing documentation. Traffic sent to this URL from outside the RAC network will be re-routed to the public site.
3. https://docs-internal.dev.rockarch.org/: the internal development site, used primarily as a preview for changes made to documentation.

GitHub is a web-based hosting service that enables version-control of content, meaning that it records and saves the changes to files over time and enables users to recall specific versions of those files. See [Using GitHub](using-github) for more information on Git and GitHub.
