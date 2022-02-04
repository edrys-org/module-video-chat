# Edrys Module Template

This is a basic bare-bones Edrys Module, it is a good staring point for creating your own modules.

- Visit the [Edrys Modules documentation](https://github.com/edrys-org/edrys/wiki/2.-Modules) for more infromation
- Click "Use this template" in the top right to get started


## Tech Stack

While Modules can be written in any combination of frontend technologies, we use and recommend the following:

- [Alpine.js](https://alpinejs.dev/) for UI (An alternative to JQuery, React or Vue)
- [Water.css](https://watercss.kognise.dev/) for styles (A tiny CSS reset with no classes)
- [Open Iconic](https://useiconic.com/open) for icons

This combination results in lightweight, fast modules with very easy to read code that is largely free of framework boilerplate, and requires no build step. You also don't need to spent any time learning these frameworks as they are very easy to pick up.

## Development

Serve the module on localhost and add it to an Edrys class, then use any editor to modify the module. We recommend:

- [VS Code Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) which allows you to see your changes live as you make them
- [VS Code Alpine.js Intellisense](https://marketplace.visualstudio.com/items?itemName=adrianwilczynski.alpine-js-intellisense) for highlighting Alpine.js code

## Deployment

To use the module, you need to serve it from somewhere and paste its link into your Edrys class settings. One convenient solution is [GitHub Pages](https://pages.github.com/). Alternatives includes Netlify, GitLab pages, or placing the module in the Edrys static directory.

When releasing a module on GitHub, you can tag it with `edrys` and `edrys-module` to make it easy for others to find.
