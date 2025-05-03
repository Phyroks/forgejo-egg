# Forgejo

[Forgejo](https://forgejo.org/) is a lightweight, self-hosted software forge. It's easy to install, low-maintenance, and provides a full platform for hosting Git repositories.

## Supported Versions

You can set the version to install using the `Version` variable. The following values are supported:

- `latest`  – latest stable release (default)
- `nightly` – current nightly build
- `x.y.z`   – specific Forgejo version (e.g., `1.20.4`)

## Server Ports

The server uses the following default ports:

| Port | Default |
|------|---------|
| App  | 3000    |
| SSH  | 20815   |

## Startup Command

The server starts with the following command:

```bash
./forgejo web -p {{SERVER_PORT}} -c ./app.ini
```

## Configuration

Configuration is handled via the `custom/app.ini` file. This file is automatically created during the initial installation if it does not already exist.

### Key Configuration Values:

- `LOCAL_ROOT_URL` – Base URL of the instance
- `DOMAIN` – Domain or IP address of the server
- `DISABLE_SSH` – Disable SSH feature (true/false)
- `SSH_PORT` – Port used for Git+SSH access

## Installation (Pterodactyl Egg)

The installation script automatically fetches the latest version and correct architecture (`amd64` or `arm64`) and installs Forgejo in the server environment. For more technical details, see the provided Egg.

## License

Forgejo is licensed under the [MIT License](https://forgejo.org/#license).
