# Contributing guidelines

We welcome any kind of contribution to our software, from simple comment or question to a full fledged [pull request](https://help.github.com/articles/about-pull-requests/). Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.md).

A contribution can be one of the following cases:

1. you have a question;
1. you think you may have found a bug (including unexpected behavior);
1. you want to make some kind of change to the code base (e.g. to fix a bug, to add a new feature, to update documentation);
1. you want to make a new release of the code base.

The sections below outline the steps in each case.

## You have a question

1. use the search functionality [here](https://github.com/NLeSC/nlesc_mdash/issues) to see if someone already filed the same issue;
2. if your issue search did not yield any relevant results, make a new issue;
3. apply the "Question" label; apply other labels when relevant.

## You think you may have found a bug

1. use the search functionality [here](https://github.com/NLeSC/nlesc_mdash/issues) to see if someone already filed the same issue;
1. if your issue search did not yield any relevant results, make a new issue, making sure to provide enough information to the rest of the community to understand the cause and context of the problem. Depending on the issue, you may want to include:
    - the [SHA hashcode](https://help.github.com/articles/autolinked-references-and-urls/#commit-shas) of the commit that is causing your problem;
    - some identifying information (name and version number) for dependencies you're using;
    - information about the operating system;
1. apply relevant labels to the newly created issue.

## You want to make some kind of change to the code base

1. (**important**) announce your plan to the rest of the community *before you start working*. This announcement should be in the form of a (new) issue;
1. (**important**) wait until some kind of consensus is reached about your idea being a good idea;
1. if needed, fork the repository to your own Github profile and create your own feature branch off of the latest main commit. While working on your feature branch, make sure to stay up to date with the main branch by pulling in changes, possibly from the 'upstream' repository (follow the instructions [here](https://help.github.com/articles/configuring-a-remote-for-a-fork/) and [here](https://help.github.com/articles/syncing-a-fork/));
1. install dependencies (see the [development documentation](README.dev.md#development_install));
1. make sure the existing tests still work by running ``pytest``;
1. add your own tests (if necessary);
1. update or expand the documentation;
1. update the `CHANGELOG.md` file with your change;
1. [push](http://rogerdudler.github.io/git-guide/) your feature branch to (your fork of) the nlesc_mdash repository on GitHub;
1. create the pull request, e.g. following the instructions [here](https://help.github.com/articles/creating-a-pull-request/).

In case you feel like you've made a valuable contribution, but you don't know how to write or run tests for it, or how to generate the documentation: don't let this discourage you from making the pull request; we can help you! Just go ahead and submit the pull request, but keep in mind that you might be asked to append additional commits to your pull request.

## You want to make a new release of the code base

To create a release you need write permission on the repository.

1. Check the author list in [`CITATION.cff`](CITATION.cff)
1. Bump the version using `bump-my-version bump <major|minor|patch>`. For example, `bump-my-version bump major` will increase major version numbers everywhere it's needed (code, meta, etc.) in the repo. Alternatively the version can be manually changed in nlesc_mdash/__init__.py, pyproject.toml, CITATION.cffand docs/conf.py (and other places it was possibly added).
1. Update the `CHANGELOG.md` to include changes made
1. Go to the [GitHub release page](https://github.com/NLeSC/nlesc_mdash/releases)
1. Press draft a new release button
1. Fill version, title and description field
1. Press the Publish Release button
<!--
For projects that automatically publish to PyPI using a release or publish workflow, something like the following could be useful to add (make sure to replace the names and links):

1. Wait until [PyPi publish workflow](https://github.com/NLeSC/nlesc_mdash/actions/workflows/publish.yml) has completed
1. Verify new release is on [PyPi](https://pypi.org/project/matchms/#history)
-->
<!--
For projects that also build conda packages, e.g. on conda-forge or Bioconda, something like the following could be useful to add (example taken from matchms, make sure to replace the names and links):

1. Wait until new release is also on Bioconda (https://anaconda.org/bioconda/nlesc_mdash) via a automaticly created PR on [bioconda recipes repo](https://github.com/bioconda/bioconda-recipes/pulls?q=is%3Apr+is%3Aopen+nlesc_mdash)
1. Test nlesc_mdash from bioconda by manually running [Conda verify](https://github.com/NLeSC/nlesc_mdash/actions/workflows/conda_verify.yml) workflow
-->


