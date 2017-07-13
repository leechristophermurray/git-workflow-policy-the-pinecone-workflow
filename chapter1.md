# Git Workflow

With a git-based versioning system comes many commands, functions, and possibilities. Considering these things, some have stuck with employing git under guidelines which follow particular methodologies. With skinning a cat being versioning the progress \(development, improvement and maintenance\) of projects, these many ways to skin a cat are considered as workflows. A workflow may be focused around how the main version \(master branch\) of a project is updated, how contributors may contribute, what conditions are required for versions to be created, and many more considerations. A Workflow may even be an amalgamation of many workflows. There is no absolute standard, as workflows are best practices that at times are situational. A workflow may even require revision as time progresses and teams change.

#### Main Actions

To support workflows, git commands and features are assigned with guidelines to cover considered situations a team may be faced with. With that being said, here are a few commands to be considered:

| Task | Command | Description |
| :--- | :--- | :--- |
| Initializing a repository | `init` | declare the current directory as a git repository. |
| Copy a repository locally | `clone` | to create an exact image of a repository, locally. All branches and other history artifacts and records are also copied. |
| transit to another branch | `checkout` | Switch to a different branch or restore working tree files |
| List, create, or delete branches | `branch` | The git branch command lets you create, list, rename, and delete branches. |
| Add file contents to the index | `add` | This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit. |
| Download objects and refs/references from another/remote repository. | `fetch` | Fetch branches and/or tags \(collectively, "refs"\) from one or more other repositories, along with the objects necessary to complete their histories. Remote-tracking branches are updated. |
| Join two or more development histories together | `merge` | Incorporates changes from the named commits \(since the time their histories diverged from the current branch\) into the current branch. |
| Record changes to the repository | `commit` | Stores the current contents of the index in a new commit along with a log message from the user describing the changes. |
|  | `push` |  |
|  | `pull` |  |



