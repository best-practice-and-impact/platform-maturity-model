# Analysis platform maturity model

A maturity model for platforms that support development of Reproducible Analytical Pipelines (RAP).

This is a **draft** model that draws on [the RAP miminum viable product definition](https://github.com/best-practice-and-impact/rap_mvp_maturity_guidance/blob/master/Reproducible-Analytical-Pipelines-MVP.md), [the Duck Book guidance for good practices in analysis and research](https://best-practice-and-impact.github.io/qa-of-code-guidance/intro.html) and [the current industry standard - indernal development platforms](https://internaldeveloperplatform.org/).

## Minimum requirements

Access to all supported versions of [Python](https://endoflife.date/python) and [R](https://developer.r-project.org/)

Dedicated technical support for Python, R and their toolchains

Users are able to create their own virtual environments with the necessary programming language version

Virtual environments persist between sessions in the same workspace

Access to Git software, for version control

Access to GitHub, for version control, continuous integration (GitHub Actions) and open sourcing code (public repositories)

Access to public and internal hosting for documentation, for example GitHub Pages

Access to standard integrated developments environments (IDE), such as Visual Studio Code for Python and Rstudio for R

Access to the public internet (given the standard department proxy restrictions) for coding resources. It must be possible to directly use code snippets from the web or local code examples in code development on the platform.

For development environments it should be possible to copy and paste text into and out of the environment

For exploratory environments it should be possible to copy and paste into the environment

Access to standard package repositories for Python and R, for example, via Artifactory mirrors. A reasonable baseline is PyPI, CRAN, Debian and conda.

Package security should be assessed automatically (e.g. using JFrog X-ray), rather than by a manual request and review

Access to distributed computing resources and tools for working with these, for example Apache Spark

Access to a pipeline orchestration tool, for example Apache Airflow

Distinct development, research and production workspaces that can be created by self-service. The development workspace must not have access to sensitive data assets. The tooling requirements might be best met by defining a default workspace for each environment type (e.g. via Terraform).

Timely access to projects and environments for new project members or reviewers

For movement and storage of data additional requirements are:

* Read-only storage of raw data assets

* Support for relational database and support for designing their architecture

* Programmatic access to big data storage

* Programmatic access to individual and shared bucket-style storage, for intermediate data

* Standardised automated data ingest and egress routes giving timely access to data


## Medium maturity requirements

Support for creating reproducible environments for deploying analysis into production, for example using Docker. This may be met by supporting mature projects to adjust the default environment configuration for their workspaces.

Tools for automated deployment of production systems

Support for creating external-facing servers to host end-products, such as web applications or APIs. These servers may be open for the public or authenticated for internal use only.


## Higher maturity requirements

A request route for adding access and support for other open source tools

Ability to SSH tunnel into workspaces, to use a local instance of an IDE to edit and execute code in a cloud environment

Ability to request access for external collaborators to specific projects on the platform, for example other civil servants or external experts. This will facilitate cross-government projects and external review and audit of analyses.

Support for creating reproducible infrastructure for deploying analysis into production, for example using Terraform
