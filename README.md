# git hooks

Hooks for git.

## Usage

If you want to use it per repo just copy hooks you want to `.git/hooks/` and make then executable.

For global hooks do the following:

```
mkdir -p ~/.git-templates/hooks
```

Copy hooks you want to use to this new directory. Then do:

```
git config --global init.templatedir '~/.git-templates'
```

It will work for new repositories. For already existing repositories you need to also reinitialize repository:

```
git init
```

## Hooks

### prepare-commit-msg

Checks branch name and if there's jira task mentioned in the branch it will paste it in the first line.

### commit-msg

Checks if any jira tasks are mentioned in the commit msg and for each adds link to the end of the commit msg. The links will be nicely formated on github
