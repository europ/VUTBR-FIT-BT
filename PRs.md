## Brno University of Technology - Faculty of Information Technology<br>Bachelor's Thesis - Implementation<br>2017/2018

### Pull requests

1. [Pronto integration](https://github.com/ManageIQ/miq_bot/pull/406)
    * (dependence) [Fix for syntax error discarding](https://github.com/prontolabs/pronto-rubocop/pull/35)
    * (enhancement) [Fixed class name of YAMLLintRunner](https://github.com/pauliusm/pronto-yamllint/pull/2)
2. [Miq-Bot's Pronto Formatter](https://github.com/ManageIQ/miq_bot/pull/424)
3. [Request for pull request review command](https://github.com/ManageIQ/miq_bot/pull/408)
    * (enhancement) [Command add_reviewer supports multiple users](https://github.com/ManageIQ/miq_bot/pull/419)
4. [Remove a request for pull request review command](https://github.com/ManageIQ/miq_bot/pull/411)
    * (dependence) [Delete a pull request review request](https://github.com/octokit/octokit.rb/pull/990)
    * (unplanned) [Fix of issues in remove_reviewer command](https://github.com/ManageIQ/miq_bot/pull/416)
    * (completed) [Remove_reviewer implemented without dependence](https://github.com/ManageIQ/miq_bot/pull/420)
5. [GitHub Status API Integration](https://github.com/ManageIQ/miq_bot/pull/412)
6. [Branch status notification via Gitter](https://github.com/ManageIQ/miq_bot/pull/413)
7. [Remove unnecessary unmergeable comments](https://github.com/ManageIQ/miq_bot/pull/415)
8. (canceled) [Automated request of codeowner for PR review](https://github.com/ManageIQ/miq_bot/pull/417)
9. [Unassign command](https://github.com/ManageIQ/miq_bot/pull/422)

### Issues

* [Problem with yamllint configuration file](https://github.com/ManageIQ/miq_bot/issues/421)
* [Undocumented detail in the setup of settings.yml](https://github.com/ManageIQ/miq_bot/issues/407)
* [Wrong example in documentation](https://github.com/octokit/octokit.rb/issues/988)
    * (the fixing pull request) [Command example fix in documentation](https://github.com/octokit/octokit.rb/pull/989)

### Feedback

A feedback was given by [Jason Frey](https://github.com/Fryguy) - the principal architect of the [ManageIQ](https://github.com/ManageIQ) project, related to the [pull requests](#pull-requests).

1. *The Pronto integration is a huge benefit to the functionality of the miq_bot. Previously, miq_bot had custom integrations for a handful of linters, but maintaining that list is overwhelming. Moving to pronto opens up dozens of new linters, while moving the maintenance burden to the pronto community. More linters should improve the PR reviews across the ManageIQ community by limiting some of the human review burden.*
2. *The Pronto formatter is also a very useful feature, as it takes the results of the various linters and combines them into a single presentation. The single presentation is useful when compared to per-line comments, because it allows the author to be notified in one place and with one email. Additionally, as the author pushes new changes, it removes old comments. The PR author can then incrementally make changes, which eases their workflow.*
3. *The various bot commands (request reviewer, remove reviewer, and unassign) are extremely useful because they enable parts of GitHub’s interface to users without those users needing explicit permission. Being able to change PR review has been one of the more requested features, and now users can do this directly without asking someone else to change it for them. Although we have yet been unable to get the remove reviewer functionality into the dependent library, octokit, the miq_bot framework allowed for having a temporary workaround.*
4. *See 3.*
5. *The GitHub status API brings a very useful feature to PR reviewers, because, at a glance, they can see if there are still issues with PRs, even if all of the tests have passed. Previously, a PR could look mergeable, but still have problems, and it was the burden of the PR reviewer to double-check. With the status API, the PR will be marked as not mergeable, which removes that extra double-checking burden from the reviewer, and should make their final reviews faster.*
6. *The branch status notification via Gitter turned out to be a feature that was not as useful as first thought, because most of the benefits are already a part of Gitter itself. Many Gitter users don’t like the Gitter feature as it produces too many comments, which are distracting. However, the work for the bot feature was not useless, because in order to implement the feature, the deeper feature of having the bot communicate with Gitter was required. That underlying bot-Gitter bridge can be used for many other future features on the bot.*
7. *The removal of “old” comments saying the PR is unmergeable is very useful. The old comments confuse users and PR readers because it appears that the PR is still unmergeable, even though it is later made mergeable. This removal feature eliminates that confusion.*
8. 
9. *See 3.*
