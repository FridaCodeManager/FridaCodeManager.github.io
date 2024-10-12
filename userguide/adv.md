# Advanced Usage

## Interpreted API (1.1)
Here is a brief introduction of how to use FridaCodeManagers inbuild interpreted API to take over control over your projects build process.

### Sytax
The Syntax is simular to XML. So you use tags like `<tag>content</tag>`. It also has placeholders like `<placeholder>` which gives your script access to information stored in the APP or information provided by `libfcm`.

### Classes
The parser parses classes. like..
```xml
# Main Class

<api>
    ... sub classes ...
</api>
```
As you can see api is the main class.

### Getting Started
Create a file called `api.api` in your FCM projects root directory, then you'll have to create the Main class(`<api>`) then create a class called `<version>` to tell the API interpreter of FridaCodeManager for what version it should parse, this is to avoid issues in the future when we changed the API a bit.
Do it like...
```xml
<api>
    <version>1.1</version>
    <!-- sub classes -->
</api>
```
After the `<version>` class you can add more subclasses the 1.1 version supports.

### Sub Classes
```xml
<api>
    <!-- lets you add flags to the build command -->
    <build>-Lexamplelibfolder -lexample -Iexample/include</build>

    <!-- lets you add flags to the object file build command -->
    <build-object>-Iexample/include</build-object> #

    <!-- lets you execute bash commands before build command has been executed, in this time the app folder already exists(i.e Payload/<app>.app/). This sub class is useful to compile roothelpers or libraries -->
    <exec-before>
        echo Hello
        echo Meow :3
    </exec-before>

    <!-- lets you execute bash commands after build command has been executed, in this time the app folder still exists(i.e Payload/<app>.app/). This subclass is useful for cleanup processes -->
    <exec-after>
        echo Cleaning up
    </exec-after>

    <!-- lets you ignore folders and files in case you want that these files arent compiled with the app (i.e files of a roothelper or library) -->
    <compiler-ignore-content>
        example/mylibrary
        example/myroothelper
        example/main.c
    </compiler-ignore-content>
</api>
```

### Placeholders
```xml
<random-subclass>
	<!-- will be replaced with your current API version -->
	<apiver>

	<!-- will be replaced with your current version of FridaCodeManager -->
	<fcmver>

	<!-- will be replaced with your projects apps bundle identifier -->
	<bundle>

	<!-- will be replaced with your projects apps name -->
	<app>

	<!-- will be replaced with your devices hostname -->
	<host>

	<!-- will be replaced with your devices cpu name -->
	<cpu>

	<!-- will be replaced with your devices architecture(arm64e, arm64, armv7...) -->
	<arch>

	<!-- will be replaced with your devices model identifier -->
	<model>

	<!-- will be replaced with your devices operating system name(mostlikely iOS XD) -->
	<osname>

	<!-- will be replaced with your projects path in FridaCodeManagers container -->
	<project-path>

	<!-- will be replaced with FridaCodeManagers inbuild theos include folder -->
	<theos-path>

	<!-- will be replaced with FridaCodeManagers container path -->
	<container-path>
</random-subclass>
```

### Notice
If you want to compile something and you are a beginner, you dont have to fear the arguments of the clang command, as FridaCodeManagers spawns commands with environment variables that preset these arguments(i.e SDK root), this is done to make FridaCodeManager feel intuitive