# Maintenance guide

## Releasing a new version

> See also the [internal development notes](https://github.com/qensus-labs/venafi-dev-notes/blob/master/VENAFI-CLIENT-TOOLS.md) to learn how to check for and obtain new Venafi client tools versions.

 1. Bump the version number in `src/venafi_csp/__init__.py` and for compatibility purposes here `src/venafi_csp/support/version.txt`.

 2. Bump the versions of existing dependencies in `requirements-dev.txt`.

 3. Ensure [the CI](https://github.com/qensus-labs/venafi-csp-lib-python/actions) is successful.

 4. [Trigger the "CI/CD" workflow](https://github.com/qensus-labs/venafi-csp-lib-python/actions/workflows/ci-cd.yml). Ensure you have pushed the newest release with a tag which matches the version number. Wait until it finishes. This creates a signed release.

 6. Edit [the release](https://github.com/qensus-labs/venafi-csp-lib-python/releases)'s notes and finalize the release.
