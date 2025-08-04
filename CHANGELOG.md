# Change Log

All notable changes to this project will be documented in this file

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html),
but may switch to [CalVer Versioning](https://calver.org/) in the future.

## Unreleased

## Known issues

- Highlighting of emojis as errors, especially in identifiers longer than 63 characters
- High CPU load when inspecting tokens which contain complex unicode graphemes
- Highlighting of unclosed multiline comments
- Adding/removing a line comment on a line that starts with a block comment removes the first `#` of
    the multiline comment (this might be impossible to fix, because block comments start with the
    same character as line comments)

## 0.1.5 -

### Added

- (kay 0.6.4) `0d` decimal numbers prefix
- (kay 0.6.4) Prefix short hand assignment operator `!=`, old boolean "not equals" `!=` is now `!==`
- (kay 0.6.4) More string and characters escape codes:
    - `\e` -> ASCII `ESC` (`0x1b`)
<!--  -->
- Classification of whitespace

### Changed

- (kay 0.6.4) `#* *#` block comments
- Better tokens classification and improved naming consistency

## 0.1.4 - 2025-06-21

### Added

- (kay 0.6.3) identifier strings: ``this is an identifier``
- Autoclosing `r""`
- Autoclosing `## ##`
- Highlighting of operators and symbols
- Highlighting of unrecognized characters

### Changed

- Improved auto closing pairs activation contexts
- Boolean are now considered literals instead of keywords

### Fixed

- Fixed unclosed strings and characters patterns

### Removed

- Removed highlighting of type annotation, made builtin types special identifiers

## 0.1.3 - 2025-02-27

### Changed

- Simplified patterns
- (kay 0.6.2) Empty binary/octal/hexadecimal numbers literals (`0b`, `0o`, `0x`) are no longer
    considered syntax errors and now mean `0`

### Removed

- Removed highlighting of identifiers over the limit of 63 characters as errors

## 0.1.2 - 2024-09-27

### Changed

- Multiline comments are now enclosed by `##` and `##`

## 0.1.1 - 2024-09-20

### Added

- Highlighting of identifiers over the limit of 63 characters as errors
- Highlighting of `_` integer literals separator
- Highlighting of alternative integer literal bases
- Highlighting of escaped double quotes `\"` in raw string literals
- Highlighting of multiline comments, enclosed by `#{` and `#}`

### Changed

- Pattern now have more descriptive names

### Fixed

- Highlighting of utf8 characters in variable names now does not split variables
- Highlighting of illegal string and character literals, numbers and indeitifiers mimicking compiler
    behaviour (i.e. multiple errors are correctly taken into account and reported all at once)
- Highlighting of array type annotations

## 0.1.0 - 2024-08-30

### Added

- Initial release
- Highlighting of comments
- Highlighting of keywords
- Highlighting of character literals
- Highlighting of string literals
- Highlighting of raw string literals
- Highlighting of integer literals
- Highlighting of variables
- Highlighting of type hints
