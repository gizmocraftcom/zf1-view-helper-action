# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-view-helper-action`, published as `gizmocraft/zendframework1-view-helper-action`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-view-helper-action` to `gizmocraft/zendframework1-view-helper-action`. It now requires `gizmocraft/zendframework1-controller` and `gizmocraft/zendframework1-view` (each `^2.0.0`).

### Other changes

- No library code changes were needed and no public signatures changed.
- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes.
- Temporary: the dev dependency on `gizmocraft/zendframework1-view-helper-partial` is removed because that package is not tagged yet (restore after #59 is tagged). `Zend_View_Helper_ActionTest::testActionWithPartialsUseOfViewRendererReturnsToOriginatingViewState` skips while `Zend_View_Helper_Partial` is missing. It passes (18 of 18 tests) on PHP 8.5 and 8.6 when the upstream helper is loaded.
- CI runs PHP 8.5 and 8.6.
