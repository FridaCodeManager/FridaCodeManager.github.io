# Basic Usage

## Getting Started
Open Home Tab and press on `Create Project`.
A iOS app has to have a `Application Name` and a `Bundle Identifier`.
So chose a Name like `MyApp` and a BundleID like `com.myname.MyApp`.
The Scheme decides what Template will be used to create your project.


## Schemes
#### Swift App
Swift is a easy to understand programming language that is more beginner friendly and has a lot of beginner tutorials online and on youtube.
Your Project will only include Swift files after creation.

#### ObjC App
Objective-C is object oriented C and is for more advanced developers that know what they are doing as you can control everything in detail using Objective-C.
Its syntax is also harder to understand and compilers usually dont warn you when you do something silly(for example using a invalid UIColor).

#### Swift/ObjC App
This Scheme basically is meant for advanced developers that want to write their UI in Swift but some more compilcated symbols in Objective-C.

## Project Files
The root of your project has all files needed to compile your app. It includes code files,`entitlements.plist` and a resources folder.
> Do never delete the `Resources` folder or create a file called `DontTouchMe.plist` in the `Resources` folder as it will corrupt your project and will make the entire project unlistable!

### Code Files
As you create new code files they will automatically be found by FridaCodeManagers build system.

### Entitlements
`entitlements.plist` is a file that basically gives your app magic abilities. It elevates its permissions to what ever you write into the file. You can use almost all entitlements on TrollStore and jailbroken devices. You can find more documentation online about iOS App Entitlements.

### Resources Folder
The resources folder in your projects root has all files that gonna be in the apps root directory(for example Info.plist).