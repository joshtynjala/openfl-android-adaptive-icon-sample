# OpenFL Android adaptive icon

The [OpenFL](https://openfl.org) library for Haxe contains a number of template files that are used when building a project. You can find them in the [_assets/templates_](https://github.com/openfl/openfl/tree/develop/assets/templates) directory. Using the `<template>` element in _project.xml_, it's possible to provide additional template files to copy to the output directory, on a per-project basis, and without forking OpenFL.

This sample project contains a directory named [_custom-templates_](https://github.com/joshtynjala/openfl-android-adaptive-icon-sample/tree/main/custom-templates). It is configured in [_project.xml_](https://github.com/joshtynjala/openfl-android-adaptive-icon-sample/tree/main/project.xml) like this:

```xml
<template path="custom-templates"/>
```

Inside [_custom-templates_](https://github.com/joshtynjala/openfl-android-adaptive-icon-sample/tree/main/custom-templates), there's a file at [_android/template/app/src/main/res/mipmap-anydpi-v26/ic\_launcher.xml_](https://github.com/joshtynjala/openfl-android-adaptive-icon-sample/tree/main/custom-templates/android/template/app/src/main/res/mipmap-anydpi-v26/ic_launcher.xml). This is an Android resource that defines how the icon looks.

To add an adaptive icon to the generated _AndroidManifest.xml_ file, configure it in [_project.xml_](https://github.com/joshtynjala/openfl-android-adaptive-icon-sample/tree/main/project.xml) like this:

```xml
<config:android>
	<application android:icon="@mipmap/ic_launcher"/>
</config:android>
```

To build and launch the project, run the following command:

```sh
openfl test android
```

Sample created by [Josh Tynjala](https://github.com/sponsors/joshtynjala), the author of [Feathers UI](https://feathersui.com/) and a member of the [OpenFL](https://openfl.org/) leadership team.