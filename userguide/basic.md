# Basic Usage

## Getting Started
Open Home Tab and press on `Create Project`.
A iOS app has to have a `Application Name` and a `Bundle Identifier`.
So chose a Name like `MyApp` and a BundleID like `com.myname.MyApp`.
The `Scheme` decides what Template will be used to create your app.


## Schemes
#### Swift App
Swift is a easy to understand programming language that is more beginner friendly and has a lot of beginner tutorials online and on youtube.
Your App will include only Swift files on creation.

#### ObjC App
Objectuve-C is object oriented C and is for more advanced users that know what they are doing as you can control everything in detail using Objective-C.
Its syntax is also harder to understand and compilers usually dont warn you when you do something silly(for example using a invalid UIColor).

#### Swift/ObjC App
This Scheme basically is meant for advanced developers that want to write their UI in Swift but some more compilcated symbols in Objective-C.

## Project Root
The root of your project has all files needed to compile your app. It includes code files,`entitlements.plist` and a resources folder.
> [!IMPORTANT]
> Do never delete the `Resources` folder or create a file called `DontTouchMe.plist` in the `Resources` folder as it will corrupt your project and will make the folder unlistable!

### Code Files
Code files are automatically parsed by FridaCodeManagers build system