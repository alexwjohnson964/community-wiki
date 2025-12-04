---
sidebar_position: 12
---

# Breaking Changes (!)

The breaking change tag `!` is a special tag as it is the only tag that can be appended to any other commit tag described in this documentation.

The breaking change tag categorizes a change as one that leads to a break in some form of functionality of the code and will always lead to a new issue being created if the break in the code is one that can be fixed within the code base. There will be situations where a breaking change can't be fixed within the code (such as a no longer supported version of something) in which case the break need only be documented.

Some examples of changes that would count as breaking changes are as follows:

- The change causes an API call to fail
- The change causes a version of another software to no longer be supported

Basically if anything crucial to the functionality of the code or its usability in certain enviornments becomes broken/unoperable then the breaking change flag should be appended to the end of the already provided tag.

Examples:

- `feat(api)!: send an email to the customer when a product is shipped`
- `chore!: drop support for Node 6`