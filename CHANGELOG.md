# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Fixed
- Resolved `blog-post-workflow.yml` failures and Node.js 20 deprecation warnings.
  - Mitigated 403 Forbidden errors by adding retry logic (`retry_count: 5`, `retry_wait_time: 10`) to the `gautamkrishnar/blog-post-workflow` action.
  - Addressed Node.js 20 deprecation by moving the `FORCE_JAVASCRIPT_ACTIONS_TO_NODE24` environment variable to the job level for `actions/checkout@v4` and `gautamkrishnar/blog-post-workflow@v1`, ensuring they run with Node.js 24.
