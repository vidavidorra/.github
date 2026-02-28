# Default community files <!-- omit in toc -->

Default [community files](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions) used in all of the [vidavidorra organisation][organisation]'s projects.

- [Roadmap](https://github.com/orgs/vidavidorra/projects/2) for the [vidavidorra organisation][organisation]'s projects.
- Reusable [**GitHub**][github] Actions workflows.
- [**GitHub**][github] issue and pull request templates.
- [**Renovate**][renovate] configuration preset.
- Contributing guidelines.

---

[![Renovate enabled](https://img.shields.io/badge/Renovate-enabled-brightgreen.svg?logo=renovatebot&logoColor&style=flat-square)](https://renovatebot.com)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg?style=flat-square)](https://github.com/semantic-release/semantic-release)
[![License](https://img.shields.io/github/license/vidavidorra/.github.svg?style=flat-square)](LICENSE.md)

- [Usage](#usage)
  - [Reusable GitHub Action workflows](#reusable-github-action-workflows)
  - [Renovate](#renovate)
  - [Contributing guidelines](#contributing-guidelines)
- [Contributing](#contributing)
- [Security policy](#security-policy)
- [License](#license)

## Usage

### Reusable GitHub Action workflows

Most of the workflows in the [`.github/workflows`](.github/workflows) folder are reusable workflows. Please see each individual workflow file for it's specific usage and possible inputs. The following example shows the most basic usage in the `lint` job, as well as a little bit more advance usage, with workflow inputs, in the `build` job. Please see the [Calling a reusable workflow](https://docs.github.com/en/actions/using-workflows/reusing-workflows#calling-a-reusable-workflow) section of the [**GitHub**][github] documentation for more details.

```yml
jobs:
  lint:
    uses: vidavidorra/.github/.github/workflows/node-lint.yml
  build:
    strategy:
      matrix:
        nodeVersion: [18, 20]
    uses: vidavidorra/.github/.github/workflows/node-build.yml
    with:
      nodeVersion: ${{ matrix.nodeVersion }}
```

### Renovate

To use the configuration preset, inlcude `github>vidavidorra/.github` in the `extends` array of the [**Renovate**][renovate] configuration, as per its [documentation](https://docs.renovatebot.com/config-presets/#extending-from-a-preset).

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["github>vidavidorra/.github"]
}
```

### Contributing guidelines

In the section on contributing of the project's readme, refer to the contributing guidelines of this repository. The following text shows an example of such reference.

> Refer to the [contributing guide](https://github.com/vidavidorra/.github/blob/main/CONTRIBUTING.md) for detailed information about other contributions, like pull requests.

```
Refer to the [contributing guide](https://github.com/vidavidorra/.github/blob/main/CONTRIBUTING.md) for detailed information about other contributions, like pull requests.
```

## Contributing

Please [create an issue](https://github.com/vidavidorra/.github/issues/new/choose) if you have a bug report or feature proposal, or [create a discussion](https://github.com/vidavidorra/.github/discussions) if you have a question. If you like this project, please consider giving it a star ⭐

Refer to the [contributing guide](CONTRIBUTING.md) for detailed information about other contributions, like pull requests.

[![Conventional Commits: 1.0.0](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow?style=flat-square)](https://conventionalcommits.org)
[![XO code style](https://shields.io/badge/code_style-5ed9c7?logo=xo&labelColor=gray&style=flat-square)](https://github.com/xojs/xo)
[![Code style](https://img.shields.io/badge/code_style-Prettier-ff69b4?logo=prettier&style=flat-square)](https://github.com/prettier/prettier)

## Security policy

Please refer to the [Security Policy on GitHub](https://github.com/vidavidorra/.github/security/) for the security policy.

## License

This project is licensed under the [GPLv3 license](https://www.gnu.org/licenses/gpl.html).

Copyright © 2020-2026 Jeroen de Bruijn

<details><summary>License notice</summary>
<p>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.

The full text of the license is available in the [LICENSE](LICENSE.md) file in this repository and [online](https://www.gnu.org/licenses/gpl.html).

</details>

<!-- References -->

[organisation]: https://github.com/vidavidorra
[github]: https://github.com/
[renovate]: https://www.mend.io/renovate/
