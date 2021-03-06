# Go Buildpack Changelog

## Unreleased

Deprecate .godir, Godeps file (not Godeps/Godeps.json) and older Go versions.
Specifying a major version of go (e.g. go1.5) in Godeps/Godeps.json will cause the buildpack to select the current minor rev of Go (for bugfix goodness).

## V22 (2015-12-03)

Default back to `./...` when not using Godeps/Godeps.json at all (.godir & old Godeps file).

## V21 (2015-12-03)

Always detect packages from Godeps.json file. Previously this was only done for projects using GO15VENDOREXPERIMENT.

## V20 (2015-11-10)

Default to Package "." when using GO15VENDOREXPERIMENT

## V19 (2015-10-06)

Use new linker -X option format for go1.5

## V18 (2015-08-26)

Fix a typo (wanr -> warn)

## V17 (2015-08-26)

Support GO15VENDOREXPERIMENT flag (experimentally) & jq updated from 1.3 to 1.5

## V16 (2015-08-19)

Default to Go 1.5 if no version is specified

## V15 (2015-08-06)

Update godeps (bug fixes and version command)

## V14 (2015-07-10)

Basic validation of Godeps/Godeps.json file.

* https://github.com/heroku/heroku-buildpack-go/commit/c01751fdfcd5476421a6229ac4168a9c76823d4b

## v13 (2015-06-30)

Set GOMAXPROCS based on dyno size.

## v12 (2015-06-29)

GOPATH naming changed & update godep

* https://github.com/heroku/heroku-buildpack-go/pull/82
