# Jmix Firebird Tutorial

This repository contains documentation for using Firebird with Jmix 3.0 applications.

The documentation is maintained in two language branches:

* `release_firebird_3.0` — English;
* `release_firebird_3.0_ru` — Russian.

Both branches use the same Antora component, module structure, page paths, and navigation targets.

## Development

Install IntelliJ IDEA and the AsciiDoc plugin, clone the repository, check out the language branch you want to edit, and open the repository root in IntelliJ IDEA.

The documentation sources are located in `modules`:

* `modules/tutorial` contains the Jmix tutorial adapted for Firebird;
* `modules/firebird` contains Firebird setup, Liquibase, limitations, and a migration example.

The AsciiDoc plugin recognizes the Antora structure from `antora.yml` and supports navigation between cross-references.

## Building the Documentation

Install a current LTS version of [Node.js](https://nodejs.org), open a terminal in the repository root, and run:

```bash
npx antora antora-playbook.yml
```

The local playbook builds the currently checked-out branch by using `HEAD`. Open `build/site/index.html` after the build completes.

`antora-playbook.ci.yml` selects the corresponding remote language branch explicitly. The publication URL is intentionally not configured yet.
