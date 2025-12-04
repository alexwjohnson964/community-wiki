---
sidebar_position: 1
---

# Good Commits

Commiting style is a very important component of working on any group based project and crucial when working in the industry.

This portion of the Git commits guide aims to describe good commiting practices while also giving an introduction to the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) style of commiting since this has become a major commiting style in the industry as well as the style that will be adheared to for community projects.

## Conventional Commits

Conventional commits is a style of commiting that aims to provide clear but simple descriptions of changes in the code base that improve the overall readability of commits while also improving the ability to perform code review by providing a framework of categorizing commits into different purposes.

Conventional commits use the following main template for Git commits:

`<tag>(<scope>): <message>`

Where:
- `tag` (Required): One of the categorical tags as mentioned in the following pages of this section
- `scope` (Optional): A section of the code base or project that is affected by the changes in the Git commit
- `message` (Required): A simple but complete description of what the change accomplishes

Some examples are given below to help describe the usefulness of this commiting style.

Example: The change implements a card component for the front end that can be used in multiple areas of the code
`feat: implemented reusable card component`

Example: The fix addresses a bug with showing/hiding the password of a user using the login page
`fix(login): fixed state being properly updated for showing and hiding password`

## Modular Commits

One of the biggest issues seen in early developers is that they pack too many things into a single commit leading to it being difficult to summarize into a concise yet descriptive git commit message.

That is where things like Conventional Commits aims to help curb; the tagging system encourages that different changes not be made in the same commit since the message should not contain multiple flags.

Example: The developer adds additional functionality to a component while also working on a fix for a different aspect of the component.

- Incorrect Commit: `added x functionality and fixed issue with component y`
    - This way of commiting can make it hard to test that both items are working as intended independent of each other and can be more confusing to understand if it becomes to packed with different things done since it may not be clear what changes were made to handle each issue

- Correct Commits: `feat: added x functionality`, `fix: fixed issue with component y`
    - This keeps all changes for each different item in seperate commits so it is easy to test their independent functionality and clearly define what issue each change in the code base aims to achieve

By ensuring that each message is clear and consice it will aid in better readability of the commit history while also granting a far greater amount of control over how to handle different methods of code review prior to merging.

## Good Messages

While the tagging system helps greatly with being able to address modular commits, it is still very important to have a solid foundation of what makes a good Git commit message.

The message should be descriptive enough to describe what the commit changes while also not being so descriptive that it becomes a chore to read through when reviewing changes.

Examples:

- Too Short: `fix: fixed logging bug`
    - This message does not clearly describe what about the logging was fixed and where the bug was found

- Too Long: `fix: fixed logging issue in the create resource route of the API by correctly stating the scope of the logger to info rather than warning`
    - This message is very descriptive but long to read and could be easily condensed down

- Just Right: `fix(create-resource): set logger to info from warning`
    - This message clearly and precisely describes the fix and where in the code the fix is being implemented without being too descriptive or not descriptive enough

