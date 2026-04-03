# ERPNext — Umbrel Community App Store

A community Umbrel app store containing **ERPNext v15** (Frappe framework).

## Repository Structure

```
umbrel-app-store.yml          ← App store metadata
erpnext/
  umbrel-app.yml              ← App listing metadata (shown in Umbrel UI)
  docker-compose.yml          ← All service definitions
```

## How to Add This Store to Umbrel

1. Fork or push this repo to your own GitHub account (must be public).
2. In umbrelOS, go to **App Store → Community App Stores**.
3. Paste your GitHub repo URL (e.g. `https://github.com/YOUR_USERNAME/erpnext-umbrel-app-store`).
4. Click **Add**. ERPNext will appear in your app store.
5. Install — first boot takes **2–4 minutes** while the site initialises.

## Default Credentials

| Field    | Value                        |
|----------|------------------------------|
| URL      | `http://umbrel.local:8080`   |
| Username | `Administrator`              |
| Password | Set during Umbrel install    |

## Resource Requirements

ERPNext is resource-intensive. Recommended minimums for your Umbrel device:
- **CPU**: 2+ cores (ARM64 supported via `frappe/erpnext:v15`)
- **RAM**: 4 GB minimum, 8 GB recommended
- **Disk**: 10 GB free space

## Customisation

To add extra Frappe apps (HRMS, Payments, CRM, etc.), modify the
`create-site` command in `docker-compose.yml` to include
`--install-app <app_name>` and rebuild/restart the stack.

## Upstream

- **frappe_docker**: https://github.com/frappe/frappe_docker
- **ERPNext**: https://github.com/frappe/erpnext
