## [2.0.1](https://github.com/vidavidorra/.github/compare/v2.0.0...v2.0.1) (2023-03-11)

### Continuous Integration

- run release on Node.js 18 ([e59ea87](https://github.com/vidavidorra/.github/commit/e59ea87c4e31d0d7091c95ca2aa0d090f5f8874a))

## [2.0.0](https://github.com/vidavidorra/.github/compare/v1.3.0...v2.0.0) (2023-03-11)

### ⚠ BREAKING CHANGES

- **node-test:** rename `node-version` input to `nodeVersion`, defaulting to 18

### Features

- **node-build:** add `nodeVersion` input, defaulting to 18, to reusable workflow ([f699207](https://github.com/vidavidorra/.github/commit/f699207b4abf7c1c22fa020e6be74ebd6d71c1b6))
- **node-lint:** add `nodeVersion` input, defaulting to 18, to reusable workflow ([4bc4a83](https://github.com/vidavidorra/.github/commit/4bc4a837202fedbe704d1429ea6849d73cf5bedb))
- **node-test:** rename `node-version` input to `nodeVersion`, defaulting to 18 ([16cf09e](https://github.com/vidavidorra/.github/commit/16cf09e5a375f4d82dc7ba46341bd01ee1fef7af))

## [1.3.0](https://github.com/vidavidorra/.github/compare/v1.2.4...v1.3.0) (2022-08-15)

### Features

- add reusable workflow to triage issues ([830f413](https://github.com/vidavidorra/.github/commit/830f413460a1644a25889e651715f338ebb3f563))

## [1.2.4](https://github.com/vidavidorra/.github/compare/v1.2.3...v1.2.4) (2022-07-05)

### Continuous Integration

- add `configFile` input to reusable `lint-commit-messages` workflow ([5547b5d](https://github.com/vidavidorra/.github/commit/5547b5df5620636c36de41a311b42a4e4587dee2))

### [1.2.3](https://github.com/vidavidorra/.github/compare/v1.2.2...v1.2.3) (2022-05-04)

### Continuous Integration

- add reusable workflow to test a Node.js project ([0e1c44e](https://github.com/vidavidorra/.github/commit/0e1c44e7da3da1bb39b542c98cb3915d66b328c8))

### [1.2.2](https://github.com/vidavidorra/.github/compare/v1.2.1...v1.2.2) (2022-04-05)

### Continuous Integration

- add reusable workflow to build a Node.js project ([aa29202](https://github.com/vidavidorra/.github/commit/aa29202a7ab69942ec52369021fc887a41f7ccd3))
- add reusable workflow to lint a Node.js project ([7224f1a](https://github.com/vidavidorra/.github/commit/7224f1afbc8e770b5041df8b1a30228d5d48434c))
- add reusable workflow to setup and install a Node.js project ([e078528](https://github.com/vidavidorra/.github/commit/e0785281ea1fed28818f6acb1c7ab1d29e98ea31))
- don't reuse workflow for `lint-commit-messages` reusable workflow ([a5faaa9](https://github.com/vidavidorra/.github/commit/a5faaa9657b5e513af249d4f9bdc118c310d3ffa))
- don't run Node.js build workflow locally as we don't have a `build` script ([d8104d4](https://github.com/vidavidorra/.github/commit/d8104d4f606429fee9f98aacdd5a1342d4a750d2))
- reference local reusable workfliw with extension ([f2fd19d](https://github.com/vidavidorra/.github/commit/f2fd19df69a6bfe0d7c4cabd80b6e3e3e49889f6))
- use reusable `node-lint` workflow in the build workflow ([f2569ee](https://github.com/vidavidorra/.github/commit/f2569eeed83a4a3b14da381933cb88cd9c1bca16))

### [1.2.1](https://github.com/vidavidorra/.github/compare/v1.2.0...v1.2.1) (2022-03-29)

### Continuous Integration

- make the lint commit message workflow reusable by adding the `workflow_call` trigger ([4d4b891](https://github.com/vidavidorra/.github/commit/4d4b8918e5a5d17797148e06c0e2e4178ce5ce72))

## [1.2.0](https://github.com/vidavidorra/.github/compare/v1.1.0...v1.2.0) (2022-03-15)

### Features

- **renovate:** extend `helpers:pinGitHubActionDigests` to pin `github-action` digests ([c2e0885](https://github.com/vidavidorra/.github/commit/c2e0885bc417d3b0aaf5d3792069e815f5f4c700))

## [1.1.0](https://github.com/vidavidorra/.github/compare/v1.0.8...v1.1.0) (2021-03-02)

### Features

- **renovate:** update vidavidorra's packages without waiting for stability ([e0986f2](https://github.com/vidavidorra/.github/commit/e0986f2ff36ee24acf8445ea22d2857954a30705))

### Styles

- add ESLint ignore file to enable linting of dotfiles ([5d2f18f](https://github.com/vidavidorra/.github/commit/5d2f18f4e530714d57b1181eafbfbc8c6c31e451))

### [1.0.8](https://github.com/vidavidorra/.github/compare/v1.0.7...v1.0.8) (2021-02-25)

### Bug Fixes

- **renovate:** auto-merge all non-major updates, including GitHub Actions ([f259596](https://github.com/vidavidorra/.github/commit/f259596b31310d7224cf4e79387a93b2d432cdae))

### [1.0.7](https://github.com/vidavidorra/.github/compare/v1.0.6...v1.0.7) (2021-02-10)

### Continuous Integration

- hide `chore` commits from changelog generation ([d9845dd](https://github.com/vidavidorra/.github/commit/d9845ddaa0c299e3691705b4398415a921b7764f))

### [1.0.6](https://github.com/vidavidorra/.github/compare/v1.0.5...v1.0.6) (2021-02-10)

### Documentation

- add 2021 to license ([fa11e02](https://github.com/vidavidorra/.github/commit/fa11e025a85fe1e90b4975fd2c55497fc783800a))

### [1.0.5](https://github.com/vidavidorra/.github/compare/v1.0.4...v1.0.5) (2021-02-10)

### Continuous Integration

- remove `chore` commit type from changelog (generation) ([21607f8](https://github.com/vidavidorra/.github/commit/21607f8759589883b0158eda47ea2fa4b25db5f6))

### [1.0.4](https://github.com/vidavidorra/.github/compare/v1.0.3...v1.0.4) (2021-02-10)

### Continuous Integration

- create sharable Renovate configuration ([13f629c](https://github.com/vidavidorra/.github/commit/13f629cebd8ea35b6330f51d54ffbdd3d2a93a79))

### [1.0.3](https://github.com/vidavidorra/.github/compare/v1.0.2...v1.0.3) (2020-11-17)

### Continuous Integration

- use `env` to replace deprecated `set-env` ([69f4fe1](https://github.com/vidavidorra/.github/commit/69f4fe1bfd6e18810fcb6344455513544d31e6be))

### [1.0.2](https://github.com/vidavidorra/.github/compare/v1.0.1...v1.0.2) (2020-11-05)

### Documentation

- add contributing section on using the issue tracker ([68f551c](https://github.com/vidavidorra/.github/commit/68f551c6eb8a296097682feb51ddf70553465c2c))

### [1.0.1](https://github.com/vidavidorra/.github/compare/v1.0.0...v1.0.1) (2020-10-29)

### Documentation

- add contributing section on coding rules ([c29dec1](https://github.com/vidavidorra/.github/commit/c29dec16b7f89b1e2724c49babeecea4f635efc2))

## 1.0.0 (2020-10-19)

### Bug Fixes

- add if applicable note to bug enfironment information ([5a6c963](https://github.com/vidavidorra/.github/commit/5a6c963d548c62ff161efb82dfc7fa6636e540fd))

### Documentation

- add empty contributing file ([ba7fd64](https://github.com/vidavidorra/.github/commit/ba7fd648e2a66d5288f4d0b0cecbdadb81d8c6bd))
- add issue templates ([7a3b744](https://github.com/vidavidorra/.github/commit/7a3b7441f4b7ce0d5f7edfddc304a0613a520e17))
- add security policy ([85d8e13](https://github.com/vidavidorra/.github/commit/85d8e13187d7a088ed51a6a564ba226039d5c818))
- change wording in readme referencing projects ([bfc5c78](https://github.com/vidavidorra/.github/commit/bfc5c786622f2da897fd140769d577042686c674))
- **security:** add PGP information for secure emails ([7546732](https://github.com/vidavidorra/.github/commit/75467328da2c5fa50648ff4000ee18754290b6c8))
- create readme ([ee3b7d3](https://github.com/vidavidorra/.github/commit/ee3b7d36472dece85749ae305ecb1fa59ad0b691))

### Continuous Integration

- fix naming of main branch, `main` instead of `master` ([e86bb63](https://github.com/vidavidorra/.github/commit/e86bb630686f70e6159aa1e9b46392baa4f7d293))

### Styles

- format issue templates and security ([776a7ac](https://github.com/vidavidorra/.github/commit/776a7acb795f8a85841b85a91a4b7e2d36dc4240))
