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

Getting Started
---------------

The following will get a new processing pipeline started in a new
repository:

    python -m pip install cookiecutter
    python -m cookiecutter gh:nipreps/Cookiecutter
    # Fill in the information requested at the prompts

Reasonable defaults will be provided for all of the parameters. The
parameters are:

<dt>project_name</dt>
<dd>The name of the project, which is <i>Preps</i> preceded by a short
name or acronym for the module, by convention. Examples include
<i>fMRIPrep</i> or <i>PETPrep</i>.<dd>

<dt>project_slug</dt>
<dd>The name of the package that will be created from the module. By
convention, this is <i><project_name in lower case>prep</i>. For
example, <i>fmriprep</i> or <i>pretprep</i>.</dd>

<dt>project_description</dt>
<dd>A short (one-line) description to use in the project <i>README</i>,
and Python package documentation.</dd>

<dt>python</dt>
<dd>The minimum Python version that will be supported.</dd>

The output of the cookiecutter is a *NiPreps* processing pipeline with
a principled structure and the minimum necessary modules and files to
get started. This includes code for testing, packaging, and maintenance
and continuous integration.

As the code base is edited and grows to achieve the intended goal, it
is expected to push the new *NiPreps* pipeline code to a new repository
under the [*NiPreps* GitHub organization](https://github.com/nipreps).
Testing and Python packaging is provided via the [ITKRemoteModuleBuildTestPackageAction]
reusable GitHub Action.

To improve the discoverability of the new *NiPreps* pipeline, add
[nipreps](https://github.com/topics/nipreps) to the project's
[topics](https://help.github.com/articles/about-topics/) in the newly
created GitHub repository, together with any other relevant topics.

License
-------

This software is distributed under the Apache 2.0 license. Please see
the *LICENSE* file for details.
