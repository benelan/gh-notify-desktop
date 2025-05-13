# gh-notify-desktop

A `gh` extension for showing new GitHub notifications on your desktop.

GitHub's notifications endpoint is polled responsibly by using the `Last-Modified` and `X-Poll-Interval` headers, as mentioned in their [api reference](https://docs.github.com/en/rest/activity/notifications?apiVersion=2022-11-28).

## Installation

1. Install one of the required notification utilities:

- `dunst` - **Recommended** for linux users because the notifications will have [actions](https://dunst-project.org/documentation/#ACTIONS) to mark the thread as "read", "done", or "unsubscribed".
- `notify-send` - Secondary option for linux users
- `osascript` - Apple's builtin notification utility (it should already be installed on Macs)

2. Install the GitHub CLI, for example:

   - **Homebrew**

     ```sh
     brew install gh
     ```

   - **DNF**

     ```sh
     sudo dnf install gh
     ```

   - ... For other package managers, see the `gh` [installation docs](https://github.com/cli/cli#installation)

3. Authenticate with the GitHub CLI:

   ```sh
   gh auth login
   ```

4. Install this extension:

   ```sh
   gh extension install benelan/gh-notify-desktop
   ```

## Usage

This extension is designed to run automatically in a crontab, systemd timer, or other task scheduling tool.

For example, to schedule a job in your crontab, first run:

```sh
crontab -e
```

Next, add the following line, which will poll for notifications every two minutes:

```cron
*/2 * * * * bash -l -c 'gh notify-desktop -p'
```

Lastly, save the file and exit your editor.

When using the `-p` flag, you will only be notified for threads where you are a [participant](https://docs.github.com/en/account-and-profile/managing-subscriptions-and-notifications-on-github/setting-up-notifications/configuring-notifications#about-participating-and-watching-notifications).

## Contributing

Contributions to `gh-notify-desktop` are welcome! Please read [CONTRIBUTING](./CONTRIBUTING.md) before submitting pull requests or opening issues.

### Acknowledgements

A special thanks goes out to [`gh-notify`](https://github.com/meiji163/gh-notify) for its notification parsing logic.
