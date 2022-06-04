## Contributing 👥

<!--toc-->

- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
  - [`src/`](#src)
  - [`src/public/`](#srcpublic)
  - [`src/services/`](#srcservices)
  - [`docs/`](#docs)
- [Creating a contributor entry](#create-a-contributor-entry)

## Tech stack ⚛️

This desktop application is built with [Electron](https://www.electronjs.org/). \
[Bootstrap](https://getbootstrap.com/) is used for styling on both the [download website](http://www.downloadmysnapchatmemories.com) and the application itself.

## Project structure 📂

### `src/`

The UI and brains of the application are containd in this directory.

The application UI is defined within [`src/public`](#srcpublic). \
The memory downloading logic is in [`src/memoryDownloader.js`](/src/memoryDownloader.js), which utilizes several services found in [`src/services`](#srcservices).

### `src/public/`

Files in this directory are served as the static frontend of the electron application.

### `src/services/`

Many of the helpful services (i.e., [download services](/src/services/downloadServices.js)) are contained in this directory.

### `docs/`

Contents in this directory are served via the download website, [downloadmysnapchatmemories.com](http://www.downloadmysnapchatmemories.com).

### Version bumping

In order for contributions to be approved, they must include a version bump. This includes contributions that only make changes to the docs.

To bump the app version, run the [npm version](https://docs.npmjs.com/cli/v8/commands/npm-version) command with the appropriate version increase.

```bash
npm version <major|minor|patch>
```

Follow basic [semantic versioning](https://semver.org/#introduction) guidelines when incrementing the application version.

### Create a Contributor entry 🧑‍💻

Contributor entries are JSON objects stored in array in `docs/contributors.json`. They must follow the pattern below.

```json
{
  "name": "John Smith",
  "role": "Collaborator",
  "links": {
    "GitHub": "https://github.com/jsmith",
    "Youtube": "https://www.youtube.com/channel/johnsmith",
    "Website": "https://www.johnsmith.io"
  }
}
```

Contributor entries without a linked GitHub profile will **not** be accepted. \
`Youtube` and `Website` links are optional.
