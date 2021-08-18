# GitHub workflow for pull requests

For some changes, it can be simpler and quicker to submit a pull request using
only [GitHub](https://github.com/) rather than using git and your local development
environment. In this section, we'll edit the documentation for a repository
that you do not have cloned locally ([GMT](https://github.com/GenericMappingTools/gmt)) on GitHub.

We'll address [issue 5653](https://github.com/GenericMappingTools/gmt/issues/5653)
in the GMT repository while learning how to submit pull requests on GitHub.
The workshop leaders will assign each participant one of the files to change.
We'll complete the steps together and you can reference the instructions below.

## Creating a pull request by editing documentation on GitHub

1. Go to [GMT issue 5653 on GitHub](https://github.com/GenericMappingTools/gmt/issues/5653).
2. Click on the module link on the section that you have been assigned to go to
   the relevant documentation page ①.

   ![Click the link at the start of the section assigned](/images/doc-page.png)

3. Click the `Edit on GitHub` link in the upper-right corner ②.

   ![Click the edit on GitHub link from the documentation page](/images/edit-link.png)

4. Scroll down to the section where the are several lines with contents similar to
   `[ |SYN_OPT-*| ]`

5. Add `[ |SYN_OPT-s| ]` in a new line  immediately below a line similar to
  `[ |SYN_OPT-q| ]` (to keep alphabetical order) ③.

   ![Add -s to the synopsis message](/images/add-synopsis-s.png)

6. Scroll to the bottom of the page and enter a descriptive commit message in
   the text box below the **Propose changes** heading ④. For more instructions
   on how to write descriptive commit messages, see
   [Chris Beams's guide](https://chris.beams.io/posts/git-commit/).

    ![Write a descriptive commit message, chose email, and propose changes](/images/propose-changes.png)

7. If you have multiple email addresses associated with your account, check
   that you are using the correct address ⑤.

8. Click the `Propose changes` button ⑥.

9. Write a short description about your pull request under the
   `**Description of proposed changes**` header ⑦.

   ![Add pull request description and link to issue](/images/submit-pull-request.png)

10. Change `Fixes #` to `Addresses #5653` in order to link to the issue without
   closing it ⑧.

11. Click `Create pull request`.

## Committing more changes to a pull request using GitHub

Now, we will add the -s option to the arguments section of the documentation.
Normally, you may have added these changes to your first commit but
we want to demonstrate how to add commits to an existing pull request.

1. Navigate to the source branch for your pull request. One option for
   navigating to the source branch is to click on the *source-branch* name in the
   statement '*username* wants to merge 1 commit into *target-branch* from
   *source-branch*', below the PR title ①.

   ![Link to source branch under PR title](/images/navigate-branch.png)

2. Click on the `doc` directory, then the `rst` directory, then the `source`
   directory in the file browser on GitHub.

3. Click on the `.rst` file associated with the module that you are working on.

   - If you are working on the mask or histogram module, click on the
     `mask_common.rst_` file or `histogram_common.rst_` file, respectively,
     rather than `mask.rst` or `histogram.rst` files.

4. Click on the `edit this file button` in the upper-left corner of the file
   browser ②.

   ![Edit this file button on upper-left corder of file browser](/images/edit-file.png)

5. Add a blank line and a line containing "`.. include:: explain_-s.rst_`" after
   the line similar to "`.. include:: explain_-q.rst_`" ③.

   ![Add -s option to the list of arguments](/images/add-argument-s.png)

6. Scroll to the bottom of the page and write a descriptive commit message in
   the text box ④.

   ![Add commit message, check branch name, commit changes](/images/commit-edit.png)

7. Check that the commit will be made to the correct branch ⑤.

8. Click the `Commit changes` button ⑥.

Now, you're all done! A maintainer will review your pull request, either
suggesting changes or accepting the pull request and merging in your
contribution!