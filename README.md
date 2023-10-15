# Project Commit Message Format and Git Hook

This repository enforces a standardized commit message format and uses a Git `commit-msg` hook to ensure consistent and well-formatted commit messages.

## Commit Message Format

Commit messages in this project should follow the format:

 `<type>: <description>`

- `<type>` represents the type of the commit and should be one of the following:
  - `feature`: for new feature additions.
  - `fix`: for bug fixes.
  - `refactor`: for code refactoring.
  - `wip`: for work in progress commits that will be pushed later.

- `<description>` should provide a brief and concise description of the changes made in the commit, limited to a maximum of 50 characters.

Examples of a valid commit message:

- `feature: Add user registration functionality`
- `fix: Fix issue with login validation`
- `refactor: Simplify database query code`
- `wip: Implement user profile page`

## Using the Git Hook

A Git `commit-msg` hook is included in this repository to enforce the commit message format. The hook is located in the `.githooks` directory.

To set up the Git hook and maintain consistent commit messages, follow these steps:

1. Clone this repository to your local development environment:

```console
user@user:~$ git clone https://github.com/Husseinhassan1/DevOps-Challenge
```

2. Change your working directory to the cloned repository:
```console
user@user:~$ cd your-repo
```

3. Configure Git to use the hook in the `.githooks` directory:

```console
user@user:~$ git config core.hooksPath .githooks
```

4. Make the `commit-msg` script executable by running the following command:
```console
user@user:~$ chmod +x .githooks/commit-msg
```


With these steps, the `commit-msg` hook will be enabled for your local clone of the repository, ensuring that a consistent and well-organized commit messages is maintained.

## Explanation of How the Solution Works

1. The `commit-msg` hook checks each commit message against the specified regular expression to ensure it matches the expected format.

2. If the commit message does not match the format, the hook displays an error message and prevents the commit.

3. The error message includes a list of valid commit types and provides examples of properly formatted commit messages for reference.



