# A Next.js app and pi in a browser tab

A Next.js app from elette's Next.js template, served by `npm run dev`, with the [pi](https://www.npmjs.com/package/@earendil-works/pi-coding-agent) coding agent beside it, in [elette](https://elette.dev/): a Linux machine in your browser tab. Nothing is installed on your computer.

**Open it:** https://elette.dev/?import_gh=rbbydotdev/elette-nextjs-demo

elette clones this repository into a new project and opens three panes:

| Pane | What it runs |
|---|---|
| server | `egg create-app next site` the first time, then `npm run dev` in `site/` |
| pi | `npx -y --ignore-scripts @earendil-works/pi-coding-agent`: the coding agent, in this project |
| preview | the app on port 3000 |

The first start makes the app and installs its packages, which takes a few minutes. Edit the app in the editor or ask pi to; the dev server reloads the preview.

## Make your own

The panes are files in `.egg/autostart/`, one [XDG autostart](https://specifications.freedesktop.org/autostart-spec/latest/) entry per pane, started in name order:

- A terminal pane: `Terminal=true` and the command in `Exec`.
- A preview pane: `X-Eggshell-Preview=PORT/PATH`.
- A file pane: `X-Eggshell-File=PATH`.

The layout, files, pi and preview side by side with the terminal below, is `.egg/config.json`: arrange the panes, then Views, Save layout writes it.
