# talend-playground

This is my playground for learning Talend Open Studio, an open-source version of Talend's commercial software Studio.

**Only public datasets are used. Code is for demonstration only.**

## Setup

1. Download Talend Open Studio from [here](https://www.talend.com/products/talend-open-studio/).
1. Install Talend on your local machine.
1. Once it's installed, you can navigate to the application root directory, which we will refer to as `TALEND_ROOT_DIR`.

  ```bash
  $ cd "${TALEND_ROOT_DIR}"
  $ ls -l
  ...
  p2
  plugins
  workspace
  ```

1. The subdirectory `workspace` is where Talend Studio saves its projects.
1. Clone this repo in the workspace.

   ```bash
   $ cd workspace
   $ git clone git@github.com:cybersamx/talend-playground.git
   ```

1. Launch Talend Open Studio, you should now see TALEND_PLAYGROUND as a project. Open it. If you don't see it, you can select Import to import the project.

### Local Repo Setup

Talend Open Studio doesn't support git or any version control system in its UI. However we can initialize a directory such as a Talend project into a git local repo and then push the workspace (or directory) to Github or a remote git repo. Here are the steps to do that:

1. Go to Github and create a repo call `MyDemo`. Copy the URL for cloning.
1. Launch Talend Open Studio, create a new project say `MyDemo` or use one of their demo projects.
1. Name the project and click Finish. This should create a directory in `${TALEND_ROOT_DIR}/workspace`.
1. Go to your shell and run the following:

   ```
   $ cd "${TALEND_ROOT_DIR}/workspace/MyDemo"
   $ git init
   $ git remote add origin <REMOTE_REPO_URL>
   ```

1. Do some work and then check in code.

## Further Investigation

* Understand how and where Java code is generated.
* This is a low-code environment. Is there a clean separation between the presentation layer and code?
* Branch out, make changes, and create a PR. Evaluate code review and merging.
* Probably need to update `.gitignore`, might have checked in superfluous code.
* Understand deployment of the code (after we have checked in the code).
* Do a spike on Github Actions. May be a way to automate testing?

## Reference

* [Talend Resource Center](https://www.talend.com/resources)
