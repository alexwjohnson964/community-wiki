---
sidebar_position: 8
---

# Build

The `build` tag categorizes a change as one that modifies the build process of the code base.

Some examples of changes that would alter the build are as follows:

- Changing the output directory of a build
- Changing the build pipeline to include/exclude things

Basically if anything is changed that alters how the code base is built for being served then it should be given the `build` tag.

Examples:

- `build: added dockerization to build`
- `build: changed the output dir to html`