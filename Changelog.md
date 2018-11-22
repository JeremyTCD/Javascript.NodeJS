# Changelog
This project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html). Refer to 
[The Semantic Versioning Lifecycle](https://www.jeremytcd.com/articles/the-semantic-versioning-lifecycle)
for an overview of semantic versioning.

## [Unreleased](https://github.com/JeringTech/Javascript.NodeJS/compare/4.0.0...HEAD)

## [4.0.0](https://github.com/JeringTech/Javascript.NodeJS/compare/3.4.0...4.0.0) - Nov 22, 2018
### Additions
- Added `INodeJSProcess` interface. A wrapper for NodeJS `Process` instances.

### Changes
- **Breaking**: `INodeJSProcessFactory.Create` now returns an `INodeJSProcess` instead of a `Process`.
- Increased default `OutOfProcessNodeJSServiceOptions.TimeoutMS` from 10000ms to 60000ms.
- Overhauled logic for multi-threadeding. Added in depth tests for most multi-threaded use cases.

## [3.4.0](https://github.com/JeringTech/Javascript.NodeJS/compare/3.3.0...3.4.0) - Nov 17, 2018
### Additions
- Added automatic retries. Retries are configurable using the property `NumRetries` of `OutOfProcessNodeJSServiceOptions`. Its default
value is 1, so by default, every javascript invocation that fails is retried once.

### Fixes
- Fixed some thread safety issues in `OutOfProcessNodeJSServiceOptions`.

## [3.3.0](https://github.com/JeringTech/Javascript.NodeJS/compare/3.2.1...3.3.0) - Nov 16, 2018
### Changes
- `InvocationException` is now serializable.

### Additions
- Added `StaticNodeJSService` which exposes a static API alternative to the existing dependency injection based API.

### Fixes
- Added the SourceLink Github package required for source-linked symbols.

## [3.2.1](https://github.com/JeringTech/Javascript.NodeJS/compare/3.2.0...3.2.1) - Nov 14, 2018
### Changes
- Source-linked symbols now included in Nuget package.
- Now targets Netstandard2.0 and Net461. Removed Netstandard1.3 target.

## [3.2.0](https://github.com/JeringTech/Javascript.NodeJS/compare/3.1.0...3.2.0) - Oct 10, 2018
### Changes
- Added Nuget package title and improved description.

## [3.1.0](https://github.com/JeringTech/Javascript.NodeJS/compare/3.0.0...3.1.0) - Aug 9, 2018
### Changes
- Reduced memory consumption.

## [3.0.0](https://github.com/JeringTech/Javascript.NodeJS/compare/2.0.0...3.0.0) - Aug 6, 2018
### Changes
- Renamed project to `Jering.Javascript.NodeJS` for consistency with other `Jering` packages. Using statements must be updated to reference types from the
namespace `Jering.Javascript.NodeJS` instead of `Jering.JavascriptUtils.NodeJS`.

## [2.0.0](https://github.com/JeringTech/Javascript.NodeJS/compare/1.0.1...2.0.0) - Aug 4, 2018
### Changes
- Logging is now optional (previously, console logging was enabled by default). To make logging optional, 
the default `INodeJSService` implementation, `HttpNodeJSService`, now takes an 
`Microsoft.Extensions.Logging.ILoggerFactory` instead of an `Microsoft.Extensions.Logging.ILogger` 
as a constructor argument.
- Added .NET Standard 1.3 as a target framework.

## [1.0.1](https://github.com/JeringTech/Javascript.NodeJS/compare/1.0.0...1.0.1) - Aug 1, 2018
### Fixes
- Added some minor null checks in `InvocationContent`.

## [1.0.0](https://github.com/JeringTech/Javascript.NodeJS/compare/0.1.0...1.0.0) - Jul 28, 2018
### Changes
- Reduced default invocation/NodeJS initialization timeout.
- Improved comments for intellisense.

## [0.1.0](https://github.com/JeringTech/Javascript.NodeJS/compare/0.1.0...0.1.0) - Jul 24, 2018
Initial release.