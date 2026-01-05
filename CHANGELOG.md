# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-12-28

### Added
- Initial release of DevTrackr SDK
- `createDevTrackr()` factory function
- `getProfile()` method for fetching user profiles
- `getRepositories()` method with sorting and pagination options
- `getRecentCommits()` method with date filtering
- `getLanguageStats()` method with percentage calculations and color mapping
- `getContributionStats()` method with streak calculations
- `getActivityTimeline()` method for daily commit visualization
- Full TypeScript type definitions
- Comprehensive error handling with typed errors:
  - `DevTrackrAuthError` for authentication failures
  - `DevTrackrRateLimitError` with rate limit details
  - `DevTrackrNetworkError` for network issues
- ESM and CommonJS dual format support
- Tree-shakeable build configuration
- Comprehensive test suite (unit and integration tests)
- Complete documentation (README, VERIFICATION, COMPLIANCE)
- GitHub Actions CI/CD workflow
- Issue and PR templates

### Security
- Token handling: Tokens only exist in memory, never logged or persisted
- No environment variable reading in SDK (consumer responsibility)
- Secure error messages (no token exposure)

[1.0.0]: https://github.com/Raghaverma/Devtrackrnpm/releases/tag/v1.0.0
