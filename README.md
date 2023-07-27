# Reproduction for Github Dependabot groups rebasing all same ecosystem PRs

Reproduction Steps:

- Set up a monorepo with a multiple modules, with each module running on the npm package ecosystem.
- Set up Dependabot to do dependency updates to each module in separate pull requests, each defined as a separate group.
- Make changes to the target branch of one module.
- Observe that Dependabot rebases all the pull requests, even for other modules that do not have conflicts with the updated target branch.

Example

- After merging the dependabot PR to update the backend module
https://github.com/PetroSilenius/grouped-dependabot-rebases-all/pull/1

- The frontend module dependabot PR was rebased
https://github.com/PetroSilenius/grouped-dependabot-rebases-all/pull/2