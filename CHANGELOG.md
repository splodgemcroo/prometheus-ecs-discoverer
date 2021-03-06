# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

* Nothing.

## [3.2.0] 2020-08-19

### Added

* Alerting dashboard.

### Changed

* Improved dashboards.

## [3.1.1] [3.1.0] 2020-08-17

### Added

* Gauge with interval seconds as value.

## [3.0.0] 2020-08-16

### Added

* Makefile for development.

### Changed

* Rename Dynaconf env var prefix to `PROMED`.
* Make prometheus target marker changable. Change default to `PROMETHEUS_TARGET`.
* Marker must be `true` not just set.

## [2.3.1] 2020-08-13

### Changed

* Bugfix: If no proper network binding is found the task should be popped from 
    the cache. Currently this is only done for the current cache. It is still 
    in the next cache.

## [2.3.0] 2020-08-12

### Added 

* Two more metrics.
    * targets_marked
    * targets_marked_rejected

## [2.2.3] [2.2.2] [2.2.1] 2020-08-12

### Changed

* Bugfix: Moved not-working metric task_definitions to correct location. The 
    method it was set previously is not used in many cases.
* Improved release workflow: Sometimes after package is built and published to
    PyPI repository the following docker build cannot find the new package. So 
    I have added a loop that runs and sleeps until package is found.

## [2.2.0] 2020-08-12

### Added

* Debug logging.
* More metrics.
    * clusters
    * container_instances
    * task_definitions
    * tasks
    * task_infos
    * targets

### Changed

* Updated dependencies.

## [2.1.3] [2.1.2] [2.1.1] 2020-08-08

* Fix workflow not fetching latest package version from PyPI.
* Hotfix missing import that breaks PromED on startup.

## [2.1.0] 2020-08-07

### Added

* Grafana Dashboards.
* Add info gauge that exposes infos (currently only interval).

### Changed

* Misc around the documentation of the project.
* Improved config handling.

## [2.0.3] 2020-08-03

### Changed

* Misc around the documentation of the project.
* Change default Prometheus namespace from `PrometheusEcsDiscoverer_` to
    `discoverer_` and rename metric.

## [2.0.2] 2020-08-02

* 2.0.1 failed

### Added

* Provide Docker image for deployment of PromED.
* Improved INFO logging.

### Changed

* Misc around the documentation of the project.

## [2.0.0] 2020-08-01

### Changed

* Initial re-release. Previous project - same name but different - removed.

## [Unreleased]

* Nothing.
