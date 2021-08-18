# Local workflow for pull requests

In this section, we'll address an issue in the
[PyGMT](https://github.com/GenericMappingTools/pygmt) repository using git
and your local development environment.

We'll address [issue 1445](https://github.com/GenericMappingTools/pygmt/issues/1445)
in the PyGMT repository while learning how to submit pull requests for changes
that you make locally.

## Making changes

1. Navigate to your PyGMT repository using `cd`.

2. Check the current repository status:

    `git status`

3. Checkout the main branch:

   `git switch main`

4. Pull the latest changes:

    `git pull`

5. Create a new branch and switch to that branch:

    `git switch -c add-alias-rose`

6. Check the current branch and status:

    `git status`

7. Open the file associated with the function that you were assigned in the
   `/pygmt/src/` directory.

8. Find the `use_alias` decorator in the file immediately above the definition
   for the function that you were assigned.

9. Add the alias(es) in your assigned task to the list of parameters
   passed to the `use_alias` decorator in the format `short_form="long_form"`.

   - **Note**: For steps 9 and 10, refer to the
     [ISO basic Latin alphabet](https://en.wikipedia.org/wiki/ISO_basic_Latin_alphabet)
     when ordering the aliases.

10. In the docstring of the function, add the aliases to the list using the
    format `{short_form}`.

## Checking the docstring updates

1. Check the docstring appearance in a Python kernel

   - Start a Python kernel (Jupyter notebook or iPython).
   - Import pygmt: `import pygmt`.
   - View the docstring for your assigned method (e.g., `help(pygmt.Figure.grdimage)`).
   - Check that the alias is included in the list of aliases and the parameters section.

## Commit your changes

1. Stage and commit your changes (replace `<your-module>` with the name of the
   module that you are working on):

   ```
   git add pygmt/src/<your-module>.py
   git commit -m "Add missing aliases to <your-module>
   ```

2. Check the status and log:

    ```
    git status
    git log
    ```

## Create a pull request

1. Push your changes to your fork (replace `<your-github-username>` with your
   GitHub username and `<branch-name>` with your branch name.):

   ```
   git push -u <your-github-username> <branch-name>
   ```

2. Make a pull request:

   - Go to your fork on GitHub, where you should see a button to create a pull
     request from your branch. Click on the "Compare & pull request" button.
   - Check the base repository, base branch, head repository, and compare
     selections.
   - Enter a descriptive pull request title.
   - Enter information about the pull request underneath `**Description of
     proposed changes**`.
   - Change `Fixes #` to `Addresses #1445`.
   - Click `Create pull request`.

Now, you're all done! A maintainer will review your pull request, either
suggesting changes or accepting the pull request and merging in your
contribution!