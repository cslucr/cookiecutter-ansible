# cookiecutter-ansible

[Cookiecutter](https://cookiecutter.rtfd.io) template to generate an Ansible role layout.

## Usage

Install *Cookiecutter*:

```
python3 -m pip install cookiecutter
```

Generate the project using *Cookiecutter*:

```
cookiecutter https://github.com/cslucr/cookiecutter-ansible.git
```

## Layout

This repository provides the following file tree layout:

```
ansible/
├── defaults
│   └── main.yml
├── doc
│   ├── requirements.txt
│   ├── source
│   │   ├── author.rst
│   │   ├── compatibility.rst
│   │   ├── conf.py
│   │   ├── description.rst
│   │   ├── index.rst
│   │   ├── license.rst
│   │   ├── links.rst
│   │   ├── requirements.rst
│   │   ├── _static
│   │   │   └── .gitkeep
│   │   ├── uml.rst
│   │   ├── usage.rst
│   │   └── variables.rst
│   └── uml
│       └── class.mmd
├── docthis.sh
├── .github
│   └── workflows
│       └── github-ci.yml
├── .gitignore
├── .gitlab
│   └── issue_templates
│       ├── Bug.md
│       └── Feature.md
├── .gitlab-ci.yml
├── img
│   ├── author.png
│   ├── avatar.png
│   └── class.png
├── LICENSE
├── meta
│   └── main.yml
├── molecule
│   └── default
│       ├── converge.yml
│       └── molecule.yml
├── README.rst
├── .readthedocs.yml
├── tasks
│   └── main.yml
└── .travis.yml
```

## License

GPL 3. See the [LICENSE](https://git.beta.ucr.ac.cr/cslucr/plantillas/cookiecutter-ansible/raw/master/LICENSE) file for more details.

## Links

  - [Github repository](https://github.com/cslucr/cookiecutter-ansible).
  - [Gitlab repository](https://git.beta.ucr.ac.cr/cslucr/plantillas/cookiecutter-ansible).

## Author Information

[![cslucr](https://git.beta.ucr.ac.cr/cslucr/plantillas/cookiecutter-ansible/raw/master/img/author.png)](https://git.beta.ucr.ac.cr/cslucr)

Comunidad de Software Libre de la Universidad de Costa Rica