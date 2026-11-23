# Copilot Instructions

## Repository

This repository contains small Bash scripts for managing Linux user accounts:

- `create_users.sh` creates home directories and users from a hard-coded username array.
- `add_users_to_group.sh` adds those users to the `students` group.
- `delete_users.sh` removes users and their home directories.
- `set_passwords.sh` interactively sets passwords for those users.

## Working conventions

- Keep changes focused and use Bash arrays and quoted variable expansions for usernames.
- Preserve the scripts' explicit, easy-to-follow style; avoid adding dependencies without a clear need.
- Account names, groups, and system operations are sensitive inputs. Do not execute these scripts as a test: they modify the machine's user accounts and may prompt for elevated privileges.
- Validate shell changes with `bash -n <script>` (or `bash -n *.sh` for all scripts). Use ShellCheck if it is available, but do not install it just for a routine edit.
- There is no test suite or build system currently documented in this repository.