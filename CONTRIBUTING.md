
# Contributing to ss-keel-addons

The base contributing guide — workflow, commit conventions, PR guidelines, and community standards — lives in the [ss-community](https://github.com/slice-soft/ss-community/blob/main/CONTRIBUTING.md) repository. Read it first.

This document covers only what is specific to this repository.

---

## Scope of This Repository

`ss-keel-addons` is only the alias registry used by the Keel CLI.

In this repository, addon PRs should only update `registry.json` entries with:

- `alias`
- `repo`
- `description`
- `source`
- `tags`

Do not submit addon implementation code in this repository.

## Submit an Addon for Official Keel Ecosystem Integration

If you created an addon and want it officially listed in the Keel ecosystem, follow this process:

1. **Use a public repository**  
   Your addon repository must be publicly accessible.

2. **Follow the template standards**  
   Your addon should follow the structure and conventions from [ss-keel-addon-template](https://github.com/slice-soft/ss-keel-addon-template).  
   You can bootstrap your addon from that template (CI/CD is already prepared there). For setup details, read the template README.

3. **Prepare a stable version**  
   Make sure your addon has a clear, versioned release and passes its tests in its own repository.

4. **Open a PR in this repository (`ss-keel-addons`)**  
   Include:
   - The alias registration/update in `registry.json`.
   - Links to test evidence from the addon repository.
   - Official addon documentation details in the PR description.

5. **Optionally add documentation in `ss-keel-docs`**  
   You can also open a docs PR in `ss-keel-docs` and include a link to your addon repository.

6. **Request community review (Discord + PR review)**  
   Share your PR in Discord so maintainers can review it with context.  
   All PRs are reviewed, and entries that meet the standards are added to the official list.
