## Clone / Initialize this repository

There are two ways of initializing this repository:
* Clone this repository with "git clone --recursive".

or

* Run "git clone" and then "git submodule update --init --recursive". This will
bring in all the needed dependencies.

## Build information

### Build flags

* Consult layers/meta-balena/README.md for info on various build flags (setting
up serial console support for example) and build prerequisites. Build flags can
be set by using the build script (barys) or by manually modifying `local.conf`.

See below for using the build script.

### Build this repository

* Run the build script:
  `./balena-yocto-scripts/build/barys`

* You can also run barys with the -h switch to inspect the available options

### Custom build using this repository

* Run the build script in dry run mode to setup an empty `build` directory
    `./balena-yocto-scripts/build/barys --remove-build --dry-run`

* Edit the `local.conf` in the `build/conf` directory

* Prepare build's shell environment
    `source layers/poky/oe-init-build-env`

* Run bitbake (see message outputted when you sourced above for examples)

## Contributing

### Issues

See [Issues](../../issues) section

### Pull requests

To contribute send github pull requests targeting this repository.

Please refer to: [Yocto Contribution Guidelines](https://wiki.yoctoproject.org/wiki/Contribution_Guidelines#General_Information) and try to use the commit log format as stated there. Example:
```

<component>: Short description

I'm going to explain here what my commit does in a way that history
would be useful.

Changelog-entry: User facing description of the issue
Signed-off-by: Joe Developer <joe.developer@example.com>
```

The header and the subject of each commit must be separated by an empty line.

The subject and the footer of each commit must be separated by an empty line.

Every pull request must contain at least one commit annotated with the `Changelog-entry` footer. The messages contained in these footers will be used to automatically fill the changelog on every new version.

If your PR fixes an open issue, make sure you mention the issue addressed by the PR. See:
* https://help.github.com/articles/autolinked-references-and-urls/#issues-and-pull-requests
* https://help.github.com/articles/closing-issues-via-commit-messages/#closing-an-issue-in-a-different-repository
