---
layout: docs
title: "Documentation Site Guide | Add and Edit Content"
---

## Add and Edit Content

Prior to adding or editing content, all additions and changes must be approved as specified in the [Rockefeller Archive Center Documentation Site Content Approval Policy](https://docs.rockarch.org/docs-policy/). All public content must be approved by the Director of Archives and President.

1. Create a new RAC GitHub repository for the documentation if one does not exist. Contact a RAC employee with administrative access to the RAC GitHub to enable this action. See [Create a Repo](/docs-guide/using-github#create-a-repo).
2. Create a branch called `development` in the target repository.
3. Commit new content or changes to the `development` branch.
4. Review the changes on the RAC development server at docs.dev.rockarch.org, which will pull in new content from the `development` branch every few minutes. When a repository is first created, it has to be manually added to the development server. See the [Documentation Site Info Sheet](http://docs.rockarch.org/systems-info-sheets/documentation-site-info-sheet).
5. Submit a pull request to merge `development` to the `master` branch of the GitHub repo.
6. As per the *Content Approval Policy*, each pull request will be reviewed by the relevant Assistant Director and the Director of Archives, as necessary. If a determination is made to either convert documentation from public to private, or to remove it completely, the Assistant Director for Digital Programs or any other RAC employee with administrative access to the RAC GitHub account should be notified to enable this action.
7. Once a pull request is reviewed and approved, merge the branch into the `master` branch where it will be incorporated into docs.rockarch.org. See the [Documentation Site Info Sheet](http://docs.rockarch.org/systems-info-sheets/documentation-site-info-sheet) for directions on adding the master branch to the production server.

## Required Elements

* [ ] index.md
* [ ] README.md
* [ ] LICENSE.md
* [ ] \_config.yml

### Index.md

Documentation will be created in or converted to the Markdown format (see [Using Markdown](/docs-guide/using-markdown)) to be leveraged by Jekyll to build the website. Add simple documentation like a short policy or one-page informational sheet to the GitHub repository as a single Markdown file (named `index.md`).

#### Page Title and Layout

At the beginning of each Markdown file that is part of the documentation, include a title and the type of layout. This is the title that will be displayed as the title of the webpage.


`---`

`layout: docs`

`title:  "Guide to Processing Collections"`

`---`

The title of the page is Header 1. Note that Header 2s (##) in Markdown appear as the side navigation display on the webpages.

#### Acknowledgements

Any institution or other’s work that we relied on in drafting our own documentation should be credited on the `index.md` page.

### Readme

Every GitHub repository requires a `README.md` file that includes information about what is in the repo, how to access and use the content, and defines documentation authorship. The README should be formatted in Markdown and include a link to docs.rockarch.org.

### License

All RAC documentation that is shared publicly on this platform will be made available under a [Creative Commons Zero](https://creativecommons.org/publicdomain/zero/1.0/) (CC0) public domain dedication, and all project-associated code is made available on the RAC organizational GitHub under an [MIT License](https://opensource.org/licenses/MIT). For public content, choose a CC0 License for the GitHub repository. Do not select a license for private content.


To add a license after the repo is created:

1. Navigate to the repository page on GitHub
2. Choose "Create new file"
3. Name the file `LICENSE.md.`
4. Copy the Markdown formatted text of the [CC0 1.0 Universal License](https://github.com/idleberg/Creative-Commons-Markdown/edit/master/4.0/zero.markdown) into the new file.
5. Commit the new file.

###  \_config.yml

Create a file called `_config.yml`. See the [docs-build README](https://github.com/RockefellerArchiveCenter/docs-build/blob/master/README.md#repository-configuration) for the specific variables required in `_config.yml`. This configuration file provides information to determine whether the documentation in the repo is designated as public or private, the title and description, associated tags, and pages information that is used to create the side navigation table of contents for each set of documentation.

* The title in the config file should match the title in `index.md`, for example “Collection Policy” or “Guide to Processing Collections”.
* Designate the documentation as private using `public: false` until it has been approved for public access by the Director of Archives and President.

## Optional Elements for Longer Documentation

* Documentation files (in addition to `index.md`).
* Description. 1-2 sentences summarizing what the documentation is and any additional contextual information on `index.md`.

### Documentation Files

More complicated documentation might be more appropriately split into multiple files, which will translate into a corresponding number of web pages. In deciding how to divide the documentation, structure and present the content in a way that enhances navigation and use.

For example, in addition to an index.md file, the [Rockefeller Archive Center Guide to Processing Collections ](http://docs.rockarch.org/processing_manual/) includes two other Markdown files that represent as two different pages on docs.rockarch.org: Planning and Processing. All files should be in the root directory (no subfolders). The exception is if there are images, which should be in a subfolder titled `img`.

Filenames should be short with no special characters or spaces. Use a hyphen between words instead of spaces. The filename will be part of the url of the site, so simple and concise are best.

Note that Header 2s (##) in Markdown appear as the side navigation display on the webpages.

Add links between documents and sections using the format:

`This is a link to [another section](#header-name) in the same document`

`This is a link to [another file](/repo-name/file-name) in the same repository`

## Additional Formatting

The [docs-build](https://github.com/RockefellerArchiveCenter/docs-build) repo contains the CSS stylesheets for docs.rockarch.org. However, it is possible to add HTML and CSS markup directly into a Markdown file.

To style text as an example that will be set apart from the other text, assign the block of text a <div> tag and css class "docs-example." As specified in our custom CSS for the site, this will change the style to set the text apart.

`<div class="docs-example"><p> This is some example text </p> </div>`

<div class="docs-example"><p> This is some example text </p> </div>
