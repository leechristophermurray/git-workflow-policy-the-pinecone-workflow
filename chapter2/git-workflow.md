---
cover: >-
  https://images.unsplash.com/photo-1556075798-4825dfaaf498?crop=entropy&cs=srgb&fm=jpg&ixid=MnwxOTcwMjR8MHwxfHNlYXJjaHwyfHxnaXR8ZW58MHx8fHwxNjUyMjY3MTE3&ixlib=rb-1.2.1&q=85
coverY: 0
---

# chapter2/git-workflow.md

With a git-based versioning system comes many commands, functions, and possibilities. Considering these things, some have stuck with employing git under guidelines that follow particular methodologies. With skinning a cat being versioning the progress (development, improvement, and maintenance) of projects, these many ways to skin a cat are considered as workflows. A workflow may be focused around how the main version (master branch) of a project is updated, how contributors may contribute, what conditions are required for versions to be created, and many more considerations. A Workflow may even be an amalgamation of many workflows. There is no absolute standard, as workflows are best practices that at times are situational. A workflow may even require revision as time progresses and teams change.

## Main Actions <a href="#main-actions" id="main-actions"></a>

To support workflows, git commands and features are assigned with guidelines to cover considered situations a team may be faced with. With that being said, here are a few commands to be considered:

| Task                                                                 | Command    | Description                                                                                                                                                                                |
| -------------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Initializing a repository                                            | `init`     | declare the current directory as a git repository.                                                                                                                                         |
| Copy a repository locally                                            | `clone`    | to create an exact image of a repository, locally. All branches and other history artifacts and records are also copied.                                                                   |
| transit to another branch                                            | `checkout` | Switch to a different branch or restore working tree files                                                                                                                                 |
| List, create, or delete branches                                     | `branch`   | The git branch command lets you create, list, rename, and delete branches.                                                                                                                 |
| Add file contents to the index                                       | `add`      | This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit.                                                     |
| Download objects and refs/references from another/remote repository. | `fetch`    | Fetch branches and/or tags (collectively, "refs") from one or more other repositories, along with the objects necessary to complete their histories. Remote-tracking branches are updated. |
| Join two or more development histories together                      | `merge`    | Incorporates changes from the named commits (since the time their histories diverged from the current branch) into the current branch.                                                     |
| Record changes to the repository                                     | `commit`   | Stores the current contents of the index in a new commit along with a log message from the user describing the changes.                                                                    |
| Update remote refs along with associated objects                     | `push`     | Updates remote refs using local refs, while sending objects necessary to complete the given refs.                                                                                          |
| Fetch from and integrate with another repository or a local branch   | `pull`     | Incorporates changes from a remote repository into the current branch. In its default mode, git pull is shorthand for `git fetch` followed by `git merge FETCH_HEAD`.                      |

## Workflow <a href="#workflow" id="workflow"></a>

The workflow we'll be focussing on is one I've called pinecone workflow, we'll see why in just a bit. The default branch on a git repo, which is created once a repo is initialized, is the master branch. This we will consider as our live branch which is merged into from the release branch. We will have another branch called `dev`/`develop`/`development`, which will be our "hub" for where development takes place. Our develop branch will be as stable as we can get it to be- though oftentimes it will have most features being stable and others not so stable (with their sub-features being mostly stable). We will have several branches which will be per feature or per sub-feature, if necessary. Patches, hopefully, there need not be any, if absolutely necessary, will be merged to the release branch once all patch requirements are satisfied. A patch or a batch of patches can make a minor release. Feature branches, as we will call them, will be merged into our develop branch as soon as they are complete- and preferably not before. The develop branch will ONLY be merged into the release branch when it is stable enough and has met all the other conditions necessary. Any merges to the release branch are considered a release, which may be major or minor. Major releases are prepared to be labeled so when a Milestone has been reached.

It is important to note that before every push, the developer should check to see if their branch is in sync with the development branch. This will help to solve merge conflicts locally, before pushing them. Here is a basic guide on the recommended practice.

![](https://raw.githubusercontent.com/iamthinkking/git-workflow-policy-the-pinecone-workflow/master/assets/Git%20WorkFlow%20Policy-%20Push.svg)

With the top-most as the beginning and going counterclockwise, as a branch is started or whenever the developer is ready to resume work on a branch, one should fetch refs from the remote, then merge them in. After work is done on the project they should add their changes to staging and then commit them. Once all changes have been committed, another fetch and merge should be done, just in case there are changes to the remote, then they should push their changes. Fetching is done from the remote development branch, then pushed to the remote feature branch. After this, a pull request should be done to merge the feature branch into the development branch. With this procedure for pushing updates to a branch considered, the branching diagram ideally will look something like this:

![](https://raw.githubusercontent.com/iamthinkking/git-workflow-policy-the-pinecone-workflow/master/assets/Git%20WorkFlow%20Policy-%20Branching\_real.svg)

## Milestones and Labels

### Milestones

![](../.gitbook/assets/milestone-info-page.png)

Milestones are groups of issues that correspond to a project, feature, or time period. People use them in many different ways in software development. Some examples of milestones on GitHub include:

* **Beta Launch**— File bugs that you need to fix before you can launch the beta of your project. It’s a great way to make sure you aren’t missing anything.
* **October Sprint**— File issues that you’d like to work on in October. A great way to focus your efforts when there’s a lot to do.
* **Redesign**— File issues related to redesigning your project. A great way to collect ideas on what to work on.

_Our preferred approach is that milestones represent bug fixes and commits that contribute to a release._

### Labels

Labels are a great way to organize different types of issues. Issues can have as many labels as you want, and you can filter by one or many labels at once.

![](../assets/labels-1.png)
