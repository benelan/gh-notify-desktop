# Changelog

## [0.3.0](https://github.com/benelan/gh-notify-desktop/compare/v0.2.0...v0.3.0) (2025-05-30)


### Features

* **dunst:** Improve terminal detection for cli action ([a0b347c](https://github.com/benelan/gh-notify-desktop/commit/a0b347c2a8d0083cf9e6bf9b2073e1e6828f63b5))

## [0.2.0](https://github.com/benelan/gh-notify-desktop/compare/v0.1.0...v0.2.0) (2025-05-13)


### Features

* Add `-c` and `-C` flags that get the total count of unread notifications ([467bdcd](https://github.com/benelan/gh-notify-desktop/commit/467bdcdf7d57ad9fcdf09d64c803ea7519921bcb))
* Add `-h` flag that displays help message ([#12](https://github.com/benelan/gh-notify-desktop/issues/12)) ([a805187](https://github.com/benelan/gh-notify-desktop/commit/a8051876116ed47897c65a6ae825a32e31ddf24d))
* Add `GH_ND_MAX` environment variable to specify the max notifications to display at once ([0b1027c](https://github.com/benelan/gh-notify-desktop/commit/0b1027c5a3bbee26376348b4967778fcec1dd889))
* Add dunst actions to mark the notification as `read`, `done`, or `unsubscribed` ([447c38a](https://github.com/benelan/gh-notify-desktop/commit/447c38aa8ac36c496cb15b11fc18ef04cd95fefb))
* Add support for `osascript` and `notify-send` ([#11](https://github.com/benelan/gh-notify-desktop/issues/11)) ([02aa67c](https://github.com/benelan/gh-notify-desktop/commit/02aa67c8e635b544da5cc55bc1840b1585b03047))
* Auto-determine terminal application to use for the "cli" dunst action ([19355ba](https://github.com/benelan/gh-notify-desktop/commit/19355bab989a37c3383aa2c110e74ae467063f1e))
* Prioritize the `GH_BROWSER` environment variable when determining how to open links ([5139e4b](https://github.com/benelan/gh-notify-desktop/commit/5139e4ba21b574512dd5318413bfb507d5b718e6))


### Bug Fixes

* Ensure debug info is logged to stderr instead of stdout ([c599fea](https://github.com/benelan/gh-notify-desktop/commit/c599fea6bd87cfeaff1c32eeec5f24ebe6655645))
* Resolve issue that caused duplicate notifications to be displayed ([09576c1](https://github.com/benelan/gh-notify-desktop/commit/09576c13e902277580386e2a01c1355d4fc773e4))

## 0.1.0 (2024-12-16)


### Features

* Add flags to filter notifications by `participating` and `all` ([eba9c3a](https://github.com/benelan/gh-notify-desktop/commit/eba9c3a4ed35c287a519f2417efc70be11cda63a))
* Display `repo`, `type`, `reason`, and `title` values in notifications ([#2](https://github.com/benelan/gh-notify-desktop/issues/2)) ([6a6c7e5](https://github.com/benelan/gh-notify-desktop/commit/6a6c7e514db3eac80387f5dd3ae6cad76f96755f))
* Support `GH_BROWSER` environment variable for dunst's 'web' action ([a4c9953](https://github.com/benelan/gh-notify-desktop/commit/a4c9953bc34da64d582b9dc02d331f15e9cef4d4))
* Use the GitHub logo as the default icon for notifications ([820687b](https://github.com/benelan/gh-notify-desktop/commit/820687b8df2e3fb9a7a63d002cffb24b7dac223f))
