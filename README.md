# Yet Another Build Visualizer Plug-in
A Jenkins plugin that allows visualization of the build flow of upstream and
downstream builds in Jenkins.

![Screenshot](https://raw.githubusercontent.com/jenkinsci/yet-another-build-visualizer-plugin/master/static/yabv.png)

This plugin provides a few features not found in any current build flow
visualizers:

* It displays not only downstream builds, but the *full* build flow. In the screenshot above, the
build currently visited is highlighted using a thick dashed border.

* Since the full chain is always shown, the plugin provides easy and fast navigation
between all executed builds in the pipeline.

* Sports nice and modern interface.

* It is compatible with all build types in Jenkins and all known mechanisms of triggering
downstream builds.

* Provides visualization without adding actions or tagging builds in Jenkins with
additional meta-data, hence it is totally non-destructive and safe for removal without
risking serialization issues.

## Usage

* No configuration is needed, just install the plugin and you are ready to go.

* The "Build Flow"-graph (as seen in the screenshot above) can be found on the Project page
(shows the graph for the latest build) or on the Build status page. The graph is only shown for
builds that has at least one upstream or downstream job.

* Click the build links to go to the status page of that build. Note that all links are decorated
with drop down menus, allowing quick access to common pages (console, parameters info, etc).

* This plugin currently only work for Classic UI. Blue Ocean support may follow in future
versions.

## Changelog
See [CHANGELOG.md](CHANGELOG.md) for release details.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

## Plug-in Dependencies
This plugin is dependent on the *Downstream Build Cache* plugin, which keeps
tracks of the upstream->downstream relationship of all builds in Jenkins.

