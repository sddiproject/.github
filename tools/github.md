---
parent: Tools
---

# GitHub

* TOC
{:toc}

SDDI working groups generally use GitHub for code hosting and issue management. GitHub organizations for hosted working groups are owned and administered by the Linux Foundation staff, including the Linux Foundation release engineering team, to ensure the sustainability of the infrastructure. 

This document outlines project policies and procedures using GitHub for collaboration. In addition, the Linux Foundation release engineering team maintains [documentation](https://docs.releng.linuxfoundation.org/en/latest/) on its services, policies, and procedures.

## New project or repository

When a new working group or repository is to be added, please [submit a request][] to facilitate the process.

## Settings

Generally, the following settings apply to all hosted project repositories and organizations.

### DCO

By default, all GitHub repositories have both the [GitHub DCO App][] installed and [commit signoffs enabled][GitHub commit signoff policy]. DCO guidelines for hosted working groups are outlined in the [contributing guidelines](/process/contributing#Code+License+Identification).

### Permissions

Working groups should define a COMMITTERS.* file for indicating committers that can merge in code to a repository. The list of committers is generally approved by the working group or the committers, aligning with the requirements described in the project's governance. Permissions are managed using GitHub teams, where the working group or committers will have a team, and that team will be given ['maintain' permission](https://docs.github.com/en/github/setting-up-and-managing-organizations-and-teams/repositoriesitory-permission-levels-for-an-organization#permission-levels-for-repositoriesitories-owned-by-an-organization) on the repositories.

The best process for adding a new committer is to have that committer issue a pull request to add their name to the COMMITTERS.* file, where the required number of working group members or committers can +1 the request, and the working group chairperson can merge in it and can add the individual to the team.

### Adding read-only members to an organization

By default, hosted project GitHub organizations and repositories have enabled the [invite-contributors](https://probot.github.io/apps/invite-contributors/) GitHub app installed, which will automatically send an invite to anyone with a successful merged pull request to join the organization as a member. The *member* permission is read-only by default, but this enables members to have issues and pull requests assigned to them and be tagged inside of issues and pull requests.

### Branch protection

The below branch protection settings on the `master` or `main` branch are enabled by default.

![](./assets/branch_protection.png)

## Issue management

Generally, working groups leverage GitHub Issues for issue management. While each project is encouraged to develop its issue management strategy, below are some best practices for issue management.

### Issue and pull request templates

Using an issue or pull template request helps ensure the project maintainers have the right context and information to process these requests. More information on how to set this up is in the [GitHub issue and pull request documentation](https://docs.github.com/en/github/building-a-strong-community/about-issue-and-pull-request-templates).

### CODEOWNERS

Defining a CODEOWNERS makes an automated process for assigning new pull requests to the right committers for review. Read more in the [GitHub CODEOWNERS documentation.](https://docs.github.com/en/github/creating-cloning-and-archiving-repositoriesitories/about-code-owners#about-code-owners)

### Project boards

Issue triaging can be complicated and overwhelming, especially when managing a project to a release point. For working groups that utilize an organization, having a single view of open issues across repositories is also very helpful in release management.

GitHub has the functionality for doing either a [single repository project board](https://docs.github.com/en/github/managing-your-work-on-github/creating-a-project-board#creating-a-repositoriesitory-project-board) or a [multiple repository project board](https://docs.github.com/en/github/managing-your-work-on-github/creating-a-project-board#creating-an-organization-wide-project-board). Automation capabilities can also be leveraged to aid in using project boards.

## Using GitHub

GitHub can be daunting for the new user, but contributing becomes much easier once you get the right tools in place. Here's a guide for getting started.

1. Create a [GitHub Account](https://github.com).
2. Go to the repository of choice you are looking to contribute to.
3. Contributing to GitHub may be more accessible by using [GitHub Desktop](https://desktop.github.com/).

### Working with Markdown files

Markdown files (.md) are commonly used on GitHub for documentation and other non-code assets. They look similar to a document but have markings to allow for formatting. It can be easier to work with Markdown by using tools. You can find information on the types of elements used in GitHub Markdown here: https://guides.github.com/features/mastering-markdown/.

There are also various tools you can use to help you see how your Markdown file will look when uploaded to GitHub. The list below is incomplete but is meant to provide some examples.

- [Macdown](https://macdown.uranusjr.com/)
- [Typora](https://typora.io/)
- [StackEdit](https://stackedit.io/)
- [Dillinger](https://dillinger.io/)
- [Markdown Editor (for Visual Studio)](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.MarkdownEditor)
- [Draft](https://draftin.com/)
- [Ulysses](https://ulysses.app/)
- [iA Writer](https://ia.net/writer)
- [Dimer](https://dimerapp.com)
- [Quiver](http://happenapps.com/)
- [Mou](http://25.io/mou/)
- [VSCode](https://code.visualstudio.com/docs/languages/markdown)

## Best practices for hosting collaboation on GitHub

These practices will help you improve your GitHub presence to help you attract more participants to your working group, secure your account, be precise about licensing, and maintain good housekeeping. Please issue a PR to add new recommendations or update existing ones.

* Use the [REPOLINTER](https://github.com/todogroup/repolinter) tool created by the TODO Group to identify common issues in GitHub repositories. 
* Ensure that every repo includes a LICENSE file. 
* Add a README file to your repositories welcoming new community members to the project and explaining why the project is useful and how to get started. Follow the guidelines in the [README checklist](https://github.com/ddbeck/readme-checklist) to create an excellent README file.
* Add a CONTRIBUTING file to your repositories explaining to other developers and your community of users how to contribute to the project. At a high level, the file would explain what types of contributions are needed and how the process works.
* Add the CODEOWNERS file to define individuals or teams responsible for code in a repository.
* Add a CODE_OF_CONDUCT file that sets the ground rules for participants’ behavior and helps facilitate a friendly, welcoming environment. While not every project has a CODE_OF_CONDUCT file, its presence signals that this is a welcoming project to contribute to and defines standards for engaging with the project’s community. working groups should leverage the default [Code of Conduct][] unless an alternate Code of Conduct is approved.
* Provide documentation on the release methodology, cadence, criteria, etc.
* Document your project governance and make it available on the project’s repo.
* Setup [issue templates and pull request templates](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates) that help you customize and standardize the information you'd like contributors to include when they open issues and pull requests in your repository.
* Use English as the default universal language for anything you publish on GitHub. You can support a second language, but English should be the primary language of communication to a universal audience.

## FAQs

### Why don't project members have `admin` permission on repositories or organizations?

As working group communities and members look for the SDDI to provide a vendor-neutral space for collaboration, the staff are here to ensure that the fair and transparent governance that the project has put in place is adhered to. This can add a bit of overhead, but the tradeoff of showcasing transparent and consistent processes generally is considered a benefit to working groups, and this also lowers the burden for a project to manage on its own.

If there are concerns about this, feel free to [submit a request][].

[submit a request]: https://servicedesk.sddiproject.org
[Code of Conduct]: /code_of_conduct
