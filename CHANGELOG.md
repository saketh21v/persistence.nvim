# Changelog

## [3.1.0](https://github.com/folke/persistence.nvim/compare/v3.0.1...v3.1.0) (2024-07-07)


### Features

* **load:** fallback to regular session when branch session does not exist (yet) ([a93748a](https://github.com/folke/persistence.nvim/commit/a93748acdb2e7bc4389b3738b4c787b764c3b2a6))

## [3.0.1](https://github.com/folke/persistence.nvim/compare/v3.0.0...v3.0.1) (2024-07-07)


### Bug Fixes

* branch detection. Closes [#62](https://github.com/folke/persistence.nvim/issues/62) ([a1d37fa](https://github.com/folke/persistence.nvim/commit/a1d37fa32ef9431f6a57c217ba5c456d20834679))
* **branch:** escape branch name. Fixes [#65](https://github.com/folke/persistence.nvim/issues/65) ([1565ca0](https://github.com/folke/persistence.nvim/commit/1565ca0af2d93ee94335c2950d92bc133c90aa82))
* windows ([2d83b1a](https://github.com/folke/persistence.nvim/commit/2d83b1a5c3fe5b2251866f5263fb9607db8d64c0))

## [3.0.0](https://github.com/folke/persistence.nvim/compare/v2.0.0...v3.0.0) (2024-07-06)


### ⚠ BREAKING CHANGES

* opts.need specifieds how many buffers should be open for saving. Replaces save_empty. Closes #19
* removed load_pre/load_post/save_pre/save_post in favor of events. Check the readme
* removed `opts.options`. Use `vim.o.sessionoptions` instead.

### Features

* added `require("persistence").select()` to select a session to load ([5346b53](https://github.com/folke/persistence.nvim/commit/5346b5346a2dd1732ae84f05251ecb704f35df87))
* opts.need specifieds how many buffers should be open for saving. Replaces save_empty. Closes [#19](https://github.com/folke/persistence.nvim/issues/19) ([7bb5755](https://github.com/folke/persistence.nvim/commit/7bb575517cebbc2b172caa04581dc5d91be90136))
* persistence.active. Check if a session saving is active ([f0ac0e9](https://github.com/folke/persistence.nvim/commit/f0ac0e981e4c864df11e613636a23c5bad09376d))
* **persistence:** add `pre-` and `post-` load hooks ([#24](https://github.com/folke/persistence.nvim/issues/24)) ([3d443bd](https://github.com/folke/persistence.nvim/commit/3d443bd0a7e1d9eebfa37321fc8118d8d538af13))
* removed `opts.options`. Use `vim.o.sessionoptions` instead. ([eb5622e](https://github.com/folke/persistence.nvim/commit/eb5622edae69ec65f6f83fcdd0eb5a70ce48ece7))
* removed load_pre/load_post/save_pre/save_post in favor of events. Check the readme ([f58a838](https://github.com/folke/persistence.nvim/commit/f58a838282dac1ed33165a5fd03829b036584df2))
* sessions per branch. Closes [#9](https://github.com/folke/persistence.nvim/issues/9) ([cd0054e](https://github.com/folke/persistence.nvim/commit/cd0054e6a4c17e4068a3e69a030013d268e569f9))


### Bug Fixes

* don't save `gitrebase` session ([#44](https://github.com/folke/persistence.nvim/issues/44)) ([9dbe264](https://github.com/folke/persistence.nvim/commit/9dbe2648c67b678bf7fe688f03b57a2514e03e6f))
* opts.need ([9c0e522](https://github.com/folke/persistence.nvim/commit/9c0e5227fa7b36208a2db0d812008965c1aac889))
* remove expand() as stdpath() expands itself ([#50](https://github.com/folke/persistence.nvim/issues/50)) ([a2fd3d9](https://github.com/folke/persistence.nvim/commit/a2fd3d99656ac496e56233aa4a40dd045a16fdc4))

## [2.0.0](https://github.com/folke/persistence.nvim/compare/v1.2.1...v2.0.0) (2023-10-15)


### ⚠ BREAKING CHANGES

* **start:** session name is now based on the cwd when the session starts and not when the session ends. Fixes #1688

### Bug Fixes

* **start:** session name is now based on the cwd when the session starts and not when the session ends. Fixes [#1688](https://github.com/folke/persistence.nvim/issues/1688) ([0361df7](https://github.com/folke/persistence.nvim/commit/0361df7775f5b4ed51a6d7fe159438573b7f07a6))

## [1.2.1](https://github.com/folke/persistence.nvim/compare/v1.2.0...v1.2.1) (2023-10-13)


### Bug Fixes

* dont save the session when only `gitcommit` buffers are present. Fixes [#14](https://github.com/folke/persistence.nvim/issues/14) ([8f7cbcc](https://github.com/folke/persistence.nvim/commit/8f7cbccfb506fe6cb35db9ad966137c363b049c5))

## [1.2.0](https://github.com/folke/persistence.nvim/compare/v1.1.0...v1.2.0) (2023-10-13)


### Features

* don't save the session when no files are open (save_empty = false) ([e9afeaf](https://github.com/folke/persistence.nvim/commit/e9afeaf3a7bb645ca73980cd13048c48c292500c))

## [1.1.0](https://github.com/folke/persistence.nvim/compare/v1.0.1...v1.1.0) (2023-02-28)


### Features

* **persistence:** `pre_save` option to call before saving ([#22](https://github.com/folke/persistence.nvim/issues/22)) ([f4bb0c5](https://github.com/folke/persistence.nvim/commit/f4bb0c5641a0e6c9ac3675ddd794ca78099d8510))

## [1.0.1](https://github.com/folke/persistence.nvim/compare/v1.0.0...v1.0.1) (2023-01-06)


### Bug Fixes

* dont throw error when session was already stopped ([70c281e](https://github.com/folke/persistence.nvim/commit/70c281e54e34630d8bef9b1cf9f7a0ac3edd6a1c))

## 1.0.0 (2023-01-04)


### ⚠ BREAKING CHANGES

* save sessions in state instead of config

### Features

* added config options ([a39f3f1](https://github.com/folke/persistence.nvim/commit/a39f3f10c836709f9b6e009b20a1f028851c50e0))
* inital version ([8b32094](https://github.com/folke/persistence.nvim/commit/8b32094309ee986066c219d2b4d88a4045fbcb8c))
* save sessions in state instead of config ([c304745](https://github.com/folke/persistence.nvim/commit/c30474509666187181add6122e775f9978478c81))


### Bug Fixes

* dont show errors when loading a session ([ad7fcd4](https://github.com/folke/persistence.nvim/commit/ad7fcd4fed0cecb9ae3c6cbc4a61801ef4e2466d))
* properly escape session file names on Windows ([#7](https://github.com/folke/persistence.nvim/issues/7)) ([83af96b](https://github.com/folke/persistence.nvim/commit/83af96b1f205dddab066c96b029ceeee192b48d4))
* renamed session to persistence in autocmds ([38203a1](https://github.com/folke/persistence.nvim/commit/38203a17a97d49bfcc938f171ecfa44f52dda08e))
* vim.fn.has('win32') returns 0 or 1, not a boolean ([#8](https://github.com/folke/persistence.nvim/issues/8)) ([77cf5a6](https://github.com/folke/persistence.nvim/commit/77cf5a6ee162013b97237ff25450080401849f85))
