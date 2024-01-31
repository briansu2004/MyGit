# Handel multiple git IDs

Tips:

- Keep a global setting for the main email (with the `--global` flag)
- For each important repo, ensure the correct email with a local setting (with the `--local` flag)

```bash
cd /path/to/your/git/repository
git config user.email "your-new-email@example.com"
```

### How to change git config user.email?

You can change the Git configuration for your email address by using the `git config` command. You can set or change your email address at different levels: system-wide, user-specific, or project-specific. Here's how to change your user-specific email address using the `--global` flag as an example:

```bash
git config --global user.email "your-new-email@example.com"
```

Replace `"your-new-email@example.com"` with your desired email address. This command will update your user-specific Git configuration with the new email address, and it will affect all your Git repositories.

If you want to change the email address for a specific Git repository (project-specific), navigate to the root directory of that repository and use the `--local` flag (or simply omit any flag, as this is the default behavior):

```bash
cd /path/to/your/git/repository
git config user.email "your-new-email@example.com"
```

Again, replace `"your-new-email@example.com"` with your desired email address. This command will change the email address for that specific Git repository.

If you ever need to change the email address in the system-wide configuration (which affects all users on the system), use the `--system` flag:

```bash
sudo git config --system user.email "your-new-email@example.com"
```

Make sure you have the necessary permissions to modify system-wide Git configurations.

After running one of these commands, Git will use the new email address you provided in the specified context. Remember that you should use the correct context (system, global, or local) depending on where you want to make the change.
