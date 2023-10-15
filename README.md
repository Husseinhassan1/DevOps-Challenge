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

A Git `commit-msg` hook is in place to enforce the commit message format. If you attempt to commit with an invalid format, the hook will prevent the commit and display an error message that lists the valid commit types and provides examples of valid commit messages.

## Explanation of How the Solution Works

1. The `commit-msg` hook checks each commit message against the specified regular expression to ensure it matches the expected format.

2. If the commit message does not match the format, the hook displays an error message and prevents the commit.

3. The error message includes a list of valid commit types and provides examples of properly formatted commit messages for reference.

### To make the Git hook work, follow these steps:

1. Navigate to your local Git repository.

2. Inside the repository, navigate to the `.git/hooks` directory.

3. If the `commit-msg` file doesn't exist, you can create it. You can also copy the provided `commit-msg` script into this directory.

4. Make the `commit-msg` script executable by running the following command:
   `chmod +x .git/hooks/commit-msg`

