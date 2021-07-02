---
layout: default
title: ApplicationDelegate
parent: SwiftWin32
---
# ApplicationDelegate

A set of methods used to manage shared behaviours for the application.

``` swift
public protocol ApplicationDelegate: AnyObject, _TriviallyConstructible 
```

## Inheritance

`AnyObject`, [`_TriviallyConstructible`](https://compnerd.github.io/swift-win32/SwiftWin32/_TriviallyConstructible)

## Default Implementations

### `application(_:willFinishLaunchingWithOptions:)`

``` swift
func application(_ application: Application,
                   willFinishLaunchingWithOptions options: [Application.LaunchOptionsKey:Any]?)
      -> Bool 
```

### `application(_:didFinishLaunchingWithOptions:)`

``` swift
func application(_ application: Application,
                   didFinishLaunchingWithOptions options: [Application.LaunchOptionsKey:Any]?)
      -> Bool 
```

### `applicationDidBecomeActive(_:)`

``` swift
public func applicationDidBecomeActive(_: Application) 
```

### `applicationWillResignActive(_:)`

``` swift
public func applicationWillResignActive(_: Application) 
```

### `applicationDidEnterBackground(_:)`

``` swift
public func applicationDidEnterBackground(_: Application) 
```

### `applicationWillEnterForeground(_:)`

``` swift
public func applicationWillEnterForeground(_: Application) 
```

### `applicationWillTerminate(_:)`

``` swift
public func applicationWillTerminate(_: Application) 
```

### `applicationProtectedDataDidBecomeAavailable(_:)`

``` swift
public func applicationProtectedDataDidBecomeAavailable(_ application: Application) 
```

### `applicationProtectedDataWillBecomeUnavailable(_:)`

``` swift
public func applicationProtectedDataWillBecomeUnavailable(_ application: Application) 
```

### `applicationDidRecieveMemoryWarning(_:)`

``` swift
public func applicationDidRecieveMemoryWarning(_ application: Application) 
```

### `applicationSignificantTimeChange(_:)`

``` swift
public func applicationSignificantTimeChange(_ application: Application) 
```

### `application(_:configurationForConnecting:options:)`

``` swift
public func application(_ application: Application,
                          configurationForConnecting connectingSceneSession: SceneSession,
                          options: Scene.ConnectionOptions) -> SceneConfiguration 
```

### `application(_:didDiscardSceneSessions:)`

``` swift
public func application(_ application: Application,
                          didDiscardSceneSessions sceneSessions: Set<SceneSession>) 
```

### `didFinishLaunchingNotification`

``` swift
public static var didFinishLaunchingNotification: NSNotification.Name 
```

### `didBecomeActiveNotification`

``` swift
public static var didBecomeActiveNotification: NSNotification.Name 
```

### `didEnterBackgroundNotification`

``` swift
public static var didEnterBackgroundNotification: NSNotification.Name 
```

### `willEnterForegroundNotification`

``` swift
public static var willEnterForegroundNotification: NSNotification.Name 
```

### `willResignActiveNotification`

``` swift
public static var willResignActiveNotification: NSNotification.Name 
```

### `willTerminateNotification`

``` swift
public static var willTerminateNotification: NSNotification.Name 
```

### `main()`

``` swift
public static func main() 
```

## Requirements

### application(\_:​willFinishLaunchingWithOptions:​)

Informs the delegate that the application launch process has begun.

``` swift
func application(_ application: Application,
                   willFinishLaunchingWithOptions options: [Application.LaunchOptionsKey:Any]?)
      -> Bool
```

### application(\_:​didFinishLaunchingWithOptions:​)

Informs the delegate that the application launch process has ended and
the application is almost ready to run.

``` swift
func application(_ application: Application,
                   didFinishLaunchingWithOptions options: [Application.LaunchOptionsKey:Any]?)
      -> Bool
```

### applicationDidBecomeActive(\_:​)

Informs the delegate that the application has become active.

``` swift
func applicationDidBecomeActive(_ application: Application)
```

### applicationWillResignActive(\_:​)

Informs the delgate that the application is about to become inactive.

``` swift
func applicationWillResignActive(_ application: Application)
```

### applicationDidEnterBackground(\_:​)

Informs the delegate that the application is now in the background.

``` swift
func applicationDidEnterBackground(_ application: Application)
```

### applicationWillEnterForeground(\_:​)

Informs the delegate that the application is about to enter the foreground.

``` swift
func applicationWillEnterForeground(_ application: Application)
```

### applicationWillTerminate(\_:​)

Informs the delegate that the application is about to terminate.

``` swift
func applicationWillTerminate(_ application: Application)
```

### applicationProtectedDataDidBecomeAavailable(\_:​)

Responding to Environment Changes

``` swift
func applicationProtectedDataDidBecomeAavailable(_ application: Application)
```

### applicationProtectedDataWillBecomeUnavailable(\_:​)

``` swift
func applicationProtectedDataWillBecomeUnavailable(_ application: Application)
```

### applicationDidRecieveMemoryWarning(\_:​)

``` swift
func applicationDidRecieveMemoryWarning(_ application: Application)
```

### applicationSignificantTimeChange(\_:​)

``` swift
func applicationSignificantTimeChange(_ application: Application)
```

### application(\_:​configurationForConnecting:​options:​)

Returns the configuration data to use when creating a new scene.

``` swift
func application(_ application: Application,
                   configurationForConnecting connectingSceneSession: SceneSession,
                   options: Scene.ConnectionOptions) -> SceneConfiguration
```

### application(\_:​didDiscardSceneSessions:​)

Informs the delegate that the user closed one or more of the application's
scenes.

``` swift
func application(_ application: Application,
                   didDiscardSceneSessions sceneSessions: Set<SceneSession>)
```
