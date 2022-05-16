---
cover: >-
  https://images.unsplash.com/photo-1556075798-4825dfaaf498?crop=entropy&cs=srgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHwyfHxnaXR8ZW58MHx8fHwxNjUyMjY3MTE3&ixlib=rb-1.2.1&q=85
coverY: 0
---

# chapter3/syntax.md

## #issues

One of the more interesting ways to use GitHub Issues is to reference issues directly from commits. Include the issue number inside of the commit message.

![](<../.gitbook/assets/Screenshot 2022-05-16 100423.png>)

By prefacing your commits with “Fixes”, “Fixed”, “Fix”, “Closes”, “Closed”, or “Close” when the commit is merged into master, it will also automatically close the issue.

References make it possible to deeply connect the work being done with the bug being tracked, and are a great way to add visibility into the history of your project.

## @mentions

mentions are the way that we reference other GitHub users inside of GitHub Issues. Inside of the description or any comment of the issue, include the @username of another GitHub user to send them a notification. This works very similar to how Twitter uses @mentions.

We like to use the`/cc`syntax (an abbreviation for carbon copy) to include people in issues:

> It looks like the new widget form is broken on Safari. When I try and create the widget, Safari crashes. This is reproducible on 10.8, but not 10.9. Maybe a browser bug?
>
> /cc @kneath @jresig

This works great if you know the specific users to include, but many times we’re working across teams and don’t really know who might be able to help us. @mentions also work for Teams within your GitHub organization. If you create a Team called\_browser-bugs\_under the @acmeinc organization, you can reference the team with @mentions:

> /cc @acmeinc/browser-bugs

This will send notifications to every member of the browser-bugs team.
