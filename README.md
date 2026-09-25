<p align="center">
    <a href="https://github.com/lupaxa-security-toolbox">
        <img src="https://raw.githubusercontent.com/the-lupaxa-project/brand-assets/master/logos/organisations/security-toolbox/readme-logo.png" alt="Organisation Logo" />
    </a>
</p>

<h1 align="center">Git Crypt Demo Repository</h1>

This repository is protected using [**GCM — Git-Crypt Manager**](https://github.com/lupaxa-security-toolbox/git-crypt-manager).

All sensitive files in this repository are encrypted at rest using
[`git-crypt`](https://github.com/AGWA/git-crypt). Only approved users with
properly trusted GPG keys can decrypt and modify protected content.

- Public project metadata and documentation remain readable
- Source code and configuration files are encrypted
- Access changes are tracked in secure logs

## 🔑 Access Requirements

To decrypt this repository, you **must**:

1. Have your GPG key added via:

```bash
gcm add-users
````

2. Have imported and trusted your private key locally:

```bash
gpg --import <private-key.asc>
gpg --edit-key <KEYID>
trust   # select "Full trust"
quit
```

3. Unlock encryption:

```bash
git-crypt unlock
```

If your key is not approved, encrypted files will appear as binary gibberish.

<a href="https://github.com/the-lupaxa-project">
    <img src="https://raw.githubusercontent.com/the-lupaxa-project/brand-assets/master/logos/components/footer-for-child-orgs.svg" alt="The Lupaxa Project Footer" width="100%" />
</a>
