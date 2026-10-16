# OpenCode Codex Switch

Manage and switch saved OpenAI OAuth accounts in OpenCode with `/switch-codex`.

## Install

```sh
opencode plugin add opencode-codex-switch
```

## Usage

1. Run `/switch-codex` or select **Switch Codex account** in the command palette.
2. Select an account with `Enter`.
3. Choose **Switch to this account**, **Rename**, or **Remove from OpenCode**.

The active account is marked **Active account**. Selecting a row opens its actions;
it does not switch immediately. Press `Esc` to dismiss a selection dialog.

## Add an account

1. Select **Add or import account**.
2. Choose an OAuth sign-in method.
3. Follow the displayed instructions and open the authorization URL in your browser.
4. Choose **Check authorization** after authorizing, or enter the requested code.

Check the **Active account** marker afterward and switch explicitly if needed.

## Notes

- Only saved OpenAI OAuth accounts appear, not API keys or other providers.
- Switching changes the active OpenCode account, not the session's model.
- Account changes can affect other sessions using the same OpenCode server.
- Removing an account requires confirmation; it does not revoke access at OpenAI.
- Existing `codex-switch.json` accounts appear as import options when available.
  Importing copies credentials into OpenCode and leaves the original file intact.
  Keep that file private: it contains access and refresh tokens.

## License

MIT
