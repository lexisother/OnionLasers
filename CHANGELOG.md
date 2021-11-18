# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.1](https://github.com/lexisother/OnionLasers/compare/v2.1.0...v2.1.1) - 2021-11-18

### Changed

- Fix an error that occurs when a message sent with `lib.paginate()` is deleted before the timeout triggers, causing the bot to attempt reaction deletion on a nonexistant message.

## [2.1.0](https://github.com/lexisother/OnionLasers/compare/v2.0.0...v2.1.0) - 2021-10-30

### Changed

- Changed package name to `onion-lasers-v13`
    - Note that whenever the original maintainer is ready to merge my version back into upstream, this package will enter maintainance mode.
- Updated dependencies
- (Temporarily) Fix an error related to the Node.js definition file not exporting a proper Error definition by using `any`
    - For info, see [this StackOverflow answer](https://stackoverflow.com/a/49562477)

## [2.0.0](https://github.com/lexisother/OnionLasers/compare/v1.0.0...v2.0.0) - 2021-10-29

### Added

- Support for Discord.JS v13!
- Implemented the loading phase of slash commands
    - This adds an option to the `LaunchSettings`, namely `slashCommandDevServers`, so you can test your slash commands without publishing them.
- Add type guarding to slash commands

# Pre-Keep-a-Changelog
<!-- For anyone reading the Markdown source, the reason I made this a separate
header is because I can't be bothered to figure out the date these releases
were made. I might do this in the future. -->

## 1.1.3
- Made `reactInOrder` public
- Moved last executed command rejection handler to just a callback for better user customization. **You'll need to implement `process.on("unhandledRejection", ...)` now.**

## 1.1.2
- Fixed an issue where a bot would end up deleting all reactions regardless of whether or not the message had a reaction event listener to begin with (i.e. for `paginate`).

## 1.1.1
- Fixed an issue where a bot would send the "no permissions to send in channel" message even if the message wasn't a command.

## 1.1.0
- Added `getUserByNickname` utility function

## 1.0.0
First major release
