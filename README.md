# NiPreps Project Template

## Overview

This repository contains a template to be used as a starting point for a new *NiPrep* processing pipeline. 

A *NiPreps* project named `{{project_name}}` (e.g. `MyPrep`) will typically have the following structure:

```
{{project_slug}}/
├── .github/
│   └── ...
├── .maint/
│   └──  ...
├── docs/
│   └── ...
├── tests/
│   └──  ...
├── {{project_slug}}/
│   ├── cli/
│   │   ├── __init__.py
│   │   ├── parser.py
│   │   ├── run.py
│   │   ├── version.py
│   │   └── workflow.py
│   ├── data/
│   │   ├── __init__.py
│   │   └── ...
│   ├── interfaces/
│   │   ├── __init__.py
│   │   └── ...
│   ├── utils/
│   │   ├── __init__.py
│   │   └── bids.py
│   ├── workflows/
│   │   └── base.py
│   ├── __init__.py
│   ├── __main__.py
│   ├── config.py
│   └── conftest.py
├── ...
├── Dockerfile
├── ...
├── pyproject.toml
├── README.md
└── tox.ini
```

where `{{project_slug}}` corresponds to the all lowercase name of the project to be used as the root directory to host
the relevant processing source code (e.g. `myprep`).
