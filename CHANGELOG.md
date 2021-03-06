# Bolts CHANGELOG

## 1.5.0
**New**
- Bolts Tasks now have nullability annotations. #161
**Improved**
- Improved return types for continuation methods of a `BFTask` when used with generics. #198
- Improved performance of constructing a `BFTask` with result/error/exception. #181, #187
- Improved performance and dispatch policy of `BFExecutor.defaultExecutor()`. #197
- Improved performance and removed a stack frame when completing a `BFTask`. #184
**Fixed**
- Fixed rare issue when compilation would fail if Bolts is used as a subproject reference. #188
- Fixed potential data inconsistency when getting description of a `BFTask`. #182
- Fixed a warning in `BFWebViewAppLinkResolver`. #183

## 1.4.0
**New**
- Bolts now fully supports tvOS and Xcode 7.1.
**Changes**
- Bolts for iOS requires at least iOS 6.0.
- Bolts for OS X requires at least OS X 10.8.

## 1.3.0
**New**
- Bolts now fully supports watchOS 2.
- Bolts for iOS is now compilied with Bitcode slice.
**Fixed**
- Potential undefined behavior caused by casting block types.

## 1.2.2
- New: Added bitcode support when built from source for iOS 9.
- New: `BFTask` and `BFTaskCompletionSource` now supports Obj-C Generics for types of the result.
- Fixed: Resolved a crash when creating a BFURL when `target_url` is not a string (null or a number).
- Fixed: `BFIncludeStatusBarInSizeAlways` is properly handled now.

## 1.2.1
- Improved: Removed the need to check canOpenURL: and just use openURL: directly which improves App Links behavior on iOS 9.
- Fixed: Potentially never completed task if continuation returns a task and cancellation was requested.
- Fixed: iOS 9 deprecations that cause warnings when building from source and targeting iOS 9+.

## 1.2.0
- Added: `BFCancellationToken`, `BFCancellationTokenSource`, `BFCancellationTokenRegistration`
- Updated: `BFTask` APIs to have methods that accept `BFCancellationToken` as an argument.
- Documentation updates and small bug fixes.

## 1.1.5
- Better subclassing support for `BFTask`, `BFTaskCompletionSource`, `BFExecutor`.
- Improved `taskForCompletionOfAllTasks:` to check for `error`/`exception` before cancelling a task.
- Fixed and improved layout of `BFAppLinkReturnToRefererController`.
- Improve optional importing for AppLinks code in umbrella header.
- Split Tasks and AppLinks in subspecs.

## 1.1.4
- New: Bolts for iOS is easily importable from Swift code (via `import Bolts`).
- New: Added `BFTask +taskForCompletionOfAllTaskResults`.
- New: Added `faulted` property on `BFTask`.
- New: Made `BFTaskErrorDomain` and `BFTaskMultipleExceptionsException` constants publicly available.
- New: `BFTask -description` now shows completed/cancelled/faulted status of a task.

## 1.1.3
- Made Bolts work if added as a subproject
- Support for iOS 8
- Support for OS X 10.10
- Updated headers to support llvm header maps

## 1.1.2

- [App Links Analytics](https://github.com/BoltsFramework/Bolts-iOS#analytics)

## 1.1.1

- Bolts for Mac is now a dynamic framework
- Bug fixes

## 1.1.0

- Adds App Links.

## 1.0.0

- Initial release.
