            - name: Upload a Build Artifact
  uses: actions/upload-artifact@v6.0.0
  with:
    # Artifact name
    name: # optional, default is artifact
    # A file, directory or wildcard pattern that describes what to upload
    path: 
    # The desired behavior if no files are found using the provided path.
Available Options:
  warn: Output a warning but do not fail the action
  error: Fail the action with an error message
  ignore: Do not output any warnings or errors, the action does not fail

    if-no-files-found: # optional, default is warn
    # Duration after which artifact will expire in days. 0 means using default retention.
Minimum 1 day. Maximum 90 days unless changed from the repository settings page.

    retention-days: # optional
    # The level of compression for Zlib to be applied to the artifact archive. The value can range from 0 to 9: - 0: No compression - 1: Best speed - 6: Default compression (same as GNU Gzip) - 9: Best compression Higher levels will result in better compression, but will take longer to complete. For large files that are not easily compressed, a value of 0 is recommended for significantly faster uploads.

    compression-level: # optional, default is 6
    # If true, an artifact with a matching name will be deleted before a new one is uploaded. If false, the action will fail if an artifact for the given name already exists. Does not fail if the artifact does not exist.

    overwrite: # optional, default is false
    # If true, hidden files will be included in the artifact. If false, hidden files will be excluded from the artifact.

    include-hidden-files: # optional, default is false
          # Contributing

This page provides more detailed instructions on the offline contribution process. Due to the size of this repository, we highly recommend using the online options outlined in [README.md](README.md).

## Setting up Git

The first step to contributing is to install Git. GitHub has thorough documentation for setting up [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) and [Git LFS](https://docs.github.com/en/repositories/working-with-files/managing-large-files/installing-git-large-file-storage). On macOS, we recommend using [Homebrew](https://brew.sh/).

If you are new to Git, see [Git Guides](https://github.com/git-guides/) for explanations and tutorials. For a quick refresher on Git commands, see the [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf).

If you want to avoid the command line, a Git client like [GitHub Desktop](https://desktop.github.com) can perform all the operations on this page---cloning, branching, displaying diffs, and committing---but use whichever tool you prefer.

## Forking and Cloning

Instead of just cloning this repository, [fork it](https://docs.github.com/en/get-started/quickstart/fork-a-repo#forking-a-repository) on GitHub. Then [clone your fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo#cloning-your-forked-repository):

```shell
git clone https://github.com/your-username/your-fork.git
```

For instructions on keeping your fork in sync with `Roblox/creator-docs` over time, see [Syncing a fork](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/syncing-a-fork).

## Creating a New Branch

After you clone your fork, create a new branch with a unique name. Creating branches keeps your work organized and discrete and helps avoid merge conflicts when you sync your fork with `Roblox/creator-docs`.

Because you eventually want to merge into the `main` branch, use it as the basis for your new branch.

1. First, navigate to the repository root:

   ```shell
   cd creator-docs
   ```

1. Then switch to the `main` branch (if you're not already on it):

   ```shell
   git checkout main
   ```

1. Finally, create your new branch:

   ```shell
   git checkout -b your-new-branch
   ```

## Opening Pull Requests

When you're happy with your changes, commit them to your branch. Include a short summary and longer description:

```shell
git commit -m "summary" -m "description"
```

```shell
git push origin your-branch
```

Then open [`Roblox/creator-docs`](https://github.com/Roblox/creator-docs/pulls) on GitHub and click **New Pull Request**. Choose **main** as the _base_ branch and your branch as the _compare_ branch.

Add a title and description of your changes, confirm that the contribution is your own, original work that you have the right to submit, and create the pull request.
