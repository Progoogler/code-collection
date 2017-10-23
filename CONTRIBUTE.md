# Introduction

You can contribute to code-collection by opening a Pull Request.

If your are new to git or github, the following articles may help you:

* See "Using Pull Requests":https://help.github.com/articles/using-pull-requests for more information about Pull Requests.

* See <a href="http://help.github.com/forking/">Fork A Repo</a> for an introduction to forking a repository and creating branches.

* See "Refining patches using git":https://github.com/erlang/otp/wiki/Refining-patches-using-git for an introduction to cleaning up git branches.


# Adding new resources

* In most cases, pull requests for new resources should be based on the @master@ branch.

* It is important to write a good commit message explaining **why** the resource is needed. We prefer that the information is in the commit message, so that anyone that want to know two years later why a particular feature can easily find out. It does no harm to provide the same information in the pull request (if the pull request consists of a single commit, the commit message will be added to the pull request automatically).

# Before you submit your pull request


* Make sure that your branch contains clean commits:
   * Follow the guidelines for [[Writing good commit messages]](https://chris.beams.io/posts/git-commit/).
   * Make separate commits for separate changes. If you cannot describe what the commit does in one sentence, it is probably a mix of changes and should be separated into several commits.
   * Don't merge @maint@ or @master@ into your branch. Use @git rebase@ if you need to resolve merge conflicts or include the latest changes.
   * To make it possible to use the powerful @git bisect@ command, make sure that each commit can be compiled and that it works.
   * Check for unnecessary whitespace before committing with @git diff --check@.

* Check your coding style:
  * Make sure your changes follow the coding and indentation style of the code surrounding your changes.
  * Do not commit commented-out code or files that are no longer needed. Remove the code or the files.
