# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.1.1] - 2023-08-19

### Changed
- Updated `required_ruby_version` to restrict compatibility to Ruby 2.x. This version of the gem is now explicitly compatible only with Ruby 2. [@9f97d06](https://github.com/thecodecrate/city-state/commit/9f97d060c9774778497e624d05c45309fdaf5d68)

### Notes
- Users running Ruby 3 or newer should refer to version `1.1.0` or later for compatibility.

## [1.1.0] - 2023-08-14

### Added
- Ruby 3 support.
- Development dependencies: `rspec 3.10`.
- Unit tests with RSpec.

### Removed
- Ruby 2.5 support. Minimum Ruby version is now 2.6.0.
- `Gemfile.lock` from version control.

### Changed
- Update bundled MaxMind database.
- Upgrade runtime dependencies: minimum Rake is 11.0, minimum Rubyzip is 2.3.

## [0.1.0] - 2020-03-25

### Added
- Methods `set_license_key(license_key)` and `set_maxmind_zip_url(url)`.

### Removed
- Rails-specific code for broader Ruby compatibility.

### Changed
- Improve methods for renaming and adding missing cities.
- Update bundled MaxMind database.
- Upgrade dependencies for security and compatibility.

### Fixed
- Duplicated city entries. `CS.cities(:CA, :US)` multiple `Burbank` entries.
- Calling `CS.cities(nil)` returns random values.