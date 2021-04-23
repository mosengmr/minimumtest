# Minimal Solution to Reproduce

This builds and runs fine in Visual Studio for Mac, but when I open the SDK command prompt and attempt to build, the build errors.

Output:
```
$USERNAME@Elantris MinimumTest % msbuild -target:Build MinimumTest.Android/MinimumTest.Android.csproj /property:Configuration=Debug
Microsoft (R) Build Engine version 16.6.0 for Mono
Copyright (C) Microsoft Corporation. All rights reserved.

Build started 4/23/2021 11:09:56 AM.
Project "/Users/$USERNAME/code/MinimumTest/MinimumTest.Android/MinimumTest.Android.csproj" on node 1 (Build target(s)).
_ResolveAndroidTooling:
  Found Java SDK version 1.8.0.
  Found Java SDK version 1.8.0.
_ResolveXamarinAndroidTools:
   Found Xamarin.Android 11.2.2.1
_ValidateAndroidPackageProperties:
    PackageName: com.moseng.test.minimumtest
_CheckInstantRunCondition:
  Dex Fast Deployment Enabled: False
_ResolveMonoAndroidSdks:
  MonoAndroid Tools: /Library/Frameworks/Xamarin.Android.framework/Libraries/xbuild/Xamarin/Android/
  Android Platform API level: 30
  TargetFrameworkVersion: v11.0
  Android NDK: 
  Android SDK: /Users/$USERNAME/Library/Developer/Xamarin/android-sdk-macosx/
  Android SDK Build Tools: /Users/$USERNAME/Library/Developer/Xamarin/android-sdk-macosx/build-tools/30.0.2/
  Java SDK: /Users/$USERNAME/Library/Developer/Xamarin/jdk/microsoft_dist_openjdk_1.8.0.25/
  Application Java class: android.app.Application
_CleanIntermediateIfNeeded:
Skipping target "_CleanIntermediateIfNeeded" because all output files are up-to-date with respect to the input files.
Project "/Users/$USERNAME/code/MinimumTest/MinimumTest.Android/MinimumTest.Android.csproj" (1) is building "/Users/$USERNAME/code/MinimumTest/MinimumTest/MinimumTest.csproj" (2:2) on node 1 (default targets).
Project "/Users/$USERNAME/code/MinimumTest/MinimumTest/MinimumTest.csproj" (2:2) is building "/Users/$USERNAME/code/MinimumTest/MinimumTest.SharedResources/MinimumTest.SharedResources.csproj" (3:2) on node 1 (default targets).
GenerateTargetFrameworkMonikerAttribute:
Skipping target "GenerateTargetFrameworkMonikerAttribute" because all output files are up-to-date with respect to the input files.
CoreGenerateAssemblyInfo:
Skipping target "CoreGenerateAssemblyInfo" because all output files are up-to-date with respect to the input files.
CoreCompile:
Skipping target "CoreCompile" because all output files are up-to-date with respect to the input files.
CopyFilesToOutputDirectory:
  MinimumTest.SharedResources -> /Users/$USERNAME/code/MinimumTest/MinimumTest.SharedResources/bin/Debug/netstandard2.0/MinimumTest.SharedResources.dll
Done Building Project "/Users/$USERNAME/code/MinimumTest/MinimumTest.SharedResources/MinimumTest.SharedResources.csproj" (default targets).
Project "/Users/$USERNAME/code/MinimumTest/MinimumTest/MinimumTest.csproj" (2:2) is building "/Users/$USERNAME/code/MinimumTest/MinimumTest.Data/MinimumTest.Data.csproj" (4:2) on node 1 (default targets).
/Library/Frameworks/Mono.framework/Versions/6.12.0/lib/mono/msbuild/Current/bin/Sdks/Microsoft.NET.Sdk/targets/Microsoft.NET.Sdk.FrameworkReferenceResolution.targets(283,5): error NETSDK1073: The FrameworkReference 'NETStandard.Library' was not recognized [/Users/$USERNAME/code/MinimumTest/MinimumTest.Data/MinimumTest.Data.csproj]
Done Building Project "/Users/$USERNAME/code/MinimumTest/MinimumTest.Data/MinimumTest.Data.csproj" (default targets) -- FAILED.
Done Building Project "/Users/$USERNAME/code/MinimumTest/MinimumTest/MinimumTest.csproj" (default targets) -- FAILED.
Done Building Project "/Users/$USERNAME/code/MinimumTest/MinimumTest.Android/MinimumTest.Android.csproj" (Build target(s)) -- FAILED.

Build FAILED.

"/Users/$USERNAME/code/MinimumTest/MinimumTest.Android/MinimumTest.Android.csproj" (Build target) (1) ->
"/Users/$USERNAME/code/MinimumTest/MinimumTest/MinimumTest.csproj" (default target) (2:2) ->
"/Users/$USERNAME/code/MinimumTest/MinimumTest.Data/MinimumTest.Data.csproj" (default target) (4:2) ->
(ResolveTargetingPackAssets target) -> 
  /Library/Frameworks/Mono.framework/Versions/6.12.0/lib/mono/msbuild/Current/bin/Sdks/Microsoft.NET.Sdk/targets/Microsoft.NET.Sdk.FrameworkReferenceResolution.targets(283,5): error NETSDK1073: The FrameworkReference 'NETStandard.Library' was not recognized [/Users/$USERNAME/code/MinimumTest/MinimumTest.Data/MinimumTest.Data.csproj]

    0 Warning(s)
    1 Error(s)
```

Visual Studio About Info:
```
=== Visual Studio Enterprise 2019 for Mac ===

Version 8.9.7 (build 8)
Installation UUID: 78422082-92e2-4321-81d3-b1f2897166ed
	GTK+ 2.24.23 (Raleigh theme)
	Xamarin.Mac 6.18.0.23 (d16-6 / 088c73638)

	Package version: 612000125

=== Mono Framework MDK ===

Runtime:
	Mono 6.12.0.125 (2020-02/8c552e98bd6) (64-bit)
	Package version: 612000125

=== Roslyn (Language Service) ===

3.9.0-6.21152.10+c10f884b30737542ddd84ca889a4aad9281ce210

=== NuGet ===

Version: 5.8.0.6860

=== .NET Core SDK ===

SDK: /usr/local/share/dotnet/sdk/5.0.202/Sdks
SDK Versions:
	5.0.202
	3.1.408
MSBuild SDKs: /Applications/Visual Studio.app/Contents/Resources/lib/monodevelop/bin/MSBuild/Current/bin/Sdks

=== .NET Core Runtime ===

Runtime: /usr/local/share/dotnet/dotnet
Runtime Versions:
	5.0.5
	3.1.14

=== .NET Core 3.1 SDK ===

SDK: 3.1.408

=== Xamarin.Profiler ===

Version: 1.6.15.68
Location: /Applications/Xamarin Profiler.app/Contents/MacOS/Xamarin Profiler

=== Updater ===

Version: 11

=== Xamarin Designer ===

Version: 16.9.0.324
Hash: b1e216c75
Branch: remotes/origin/d16-9
Build date: 2021-04-16 00:02:50 UTC

=== Apple Developer Tools ===

Xcode 12.4 (17801)
Build 12D4e

=== Xamarin.Mac ===

Xamarin.Mac not installed. Can't find /Library/Frameworks/Xamarin.Mac.framework/Versions/Current/Version.

=== Xamarin.iOS ===

Version: 14.14.2.5 (Visual Studio Enterprise)
Hash: 3836759d4
Branch: d16-9
Build date: 2021-02-10 17:56:44-0500

=== Xamarin.Android ===

Version: 11.2.2.1 (Visual Studio Enterprise)
Commit: xamarin-android/d16-9/877f572
Android SDK: /Users/mrmoseng_mac/Library/Developer/Xamarin/android-sdk-macosx
	Supported Android versions:
		None installed

SDK Tools Version: 26.1.1
SDK Platform Tools Version: 30.0.4
SDK Build Tools Version: 30.0.2

Build Information: 
Mono: 5e9cb6d
Java.Interop: xamarin/java.interop/d16-9@54f8c24
ProGuard: Guardsquare/proguard/v7.0.1@912d149
SQLite: xamarin/sqlite/3.34.1@daff8f4
Xamarin.Android Tools: xamarin/xamarin-android-tools/d16-9@d210f11

=== Microsoft OpenJDK for Mobile ===

Java SDK: /Users/mrmoseng_mac/Library/Developer/Xamarin/jdk/microsoft_dist_openjdk_1.8.0.25
1.8.0-25
Android Designer EPL code available here:
https://github.com/xamarin/AndroidDesigner.EPL

=== Android SDK Manager ===

Version: 16.9.0.22
Hash: a391de2
Branch: remotes/origin/d16-9~2
Build date: 2021-03-24 08:30:26 UTC

=== Android Device Manager ===

Version: 16.9.0.17
Hash: fc2b3db
Branch: remotes/origin/dev/jmt/d16-9bump~1
Build date: 2021-03-24 08:30:44 UTC

=== Build Information ===

Release ID: 809070008
Git revision: 8b7ac2442978ec88d09703fafa4e43eb774f0a26
Build date: 2021-04-16 07:38:03-04
Build branch: release-8.9
Xamarin extensions: 8b7ac2442978ec88d09703fafa4e43eb774f0a26

=== Operating System ===

Mac OS X 10.16.0
Darwin 20.3.0 Darwin Kernel Version 20.3.0
    Thu Jan 21 00:07:06 PST 2021
    root:xnu-7195.81.3~1/RELEASE_X86_64 x86_64
```
