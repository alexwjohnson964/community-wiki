---
sidebar_position: 6
---

# Actions

Github actions are CI/CD pipelines that can be added to Github repositories to handle specific tasks that can be automated to improve the quality/testing/building of projects.

Github actions are usually only managed by the owner/lead of the repository but in some cases will be interacted with by contributors of the repository.

<!-- TODO: Add any useful actions that can be included in future projects -->

## Quality Actions

This section outlines pre-developed actions that improve the overall quality of the Github repository

## Testing Actions

This section outlines pre-developed actions that handle testing of the Github repository

## Build Actions

This section outlines pre-developed actions that handle building of the Github repository

## Deployment Actions

This section outlines pre-developed actions that handle deployment of the Github repository

## Github Workflows

Github workflows are the defined pipelines that run when specific github actions on the repository when certain criteria are met.

These workflows are housed in the repository's `.github/workflows` folder and are created using `yml` files.

An example of a workflow can be seen below which does the follow:
- Names the workflow
- Selects on what Git/Github events trigger the workflow to run
- Outlines a build action pipeline that does the following:
    - Runs on an ubuntu virtual machine
    - Builds a base docker image
    - Sets up a specific JDK on the virtual machine
    - Builds the java project which runs tests and creates a final docker image using the base image and built java project

```
# This workflow will build a Java project with Maven, and cache/restore any dependencies to improve the workflow execution time
# For more information see: https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-java-with-maven

# This workflow uses actions that are not certified by GitHub.
# They are provided by a third-party and are governed by
# separate terms of service, privacy policy, and support
# documentation.

name: Java CI with Maven

on:
  push:
    branches: [ "**" ]
  pull_request:
    branches: [ "**" ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - name: build base image
      run: docker build -t idp-server-base ./src/main/docker-base
    - name: Set up JDK 21
      uses: actions/setup-java@v4
      with:
        java-version: '21'
        distribution: 'temurin'
        cache: maven
    - name: Build with Maven
      run: mvn clean -B package --file pom.xml

    # Optional: Uploads the full dependency graph to GitHub to improve the quality of Dependabot alerts this repository can receive
    # - name: Update dependency graph
    #   uses: advanced-security/maven-dependency-submission-action@571e99aab1055c2e71a1e2309b9691de18d6b7d6
```
