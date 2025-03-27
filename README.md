# Ansible Role Cookiecutter

[Cookiecutter](https://github.com/audreyr/cookiecutter) is a command-line utility that creates projects from project templates - this is one such template for creating Ansible Roles for the IG team.

## Installation

Install Cookiecutter from PyPy

    pip install cookiecutter

## Usage

You can use this cookiecutter straight from the repo (provided you have working gitlab credentials the first time).

    mkdir my-new-role
    cookiecutter -o my-new-role git@gitlab.tssg.org:infrastructure-group/ansible-role.git

The cookiecutter will then ask you a bunch of questions that will set up the role.

For convenience, the cookiecutter will be cached in '~/.cookiecutters/' so cloning isn't required every time you want to make a new project. If there are updates to the template, Cookiecutter will pick these up the next time you use the template.

Additionally, you can use a '~/.cookiecutterrc' file to make calling a cookiecutter much shorter.

```
default_context:
    full_name: "<User Name>"
    email: "<username>@tssg.org"
    github_username: "<username>"
abbreviations:
    gl: git+ssh://git@gitlab.tssg.org/<username>/{0}.git
    glig: git+ssh://git@gitlab.tssg.org/infrastructure-group/{0}.git
```

This shortens the above call to 

    cookiecutter glig:ansible-role
    
Much better :)

## Features of the Templated Role

The templated role will give you the following:

- README.md: a file like this to describe content and usage of the role
- whatever ansible-galaxy gives you

## License

&copy;  Walton Institute, South East Technological University, 2023-02-22
## Contribution


- Post an issue to the [issue tracker](http://gitlab.tssg.org/infrastructure-group/ansible-role/issues) 
- Fork the repo, make some changes and submit a [Merge Request](http://gitlab.tssg.org/infrastructure-group/ansible-role/merge_requests/new)
- Patches, docs, tutorials and feedback are all welcome.

John Ronan <john.ronan@waltoninstitute.ie>
