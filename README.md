# maplibre-pod

[![CI Status](https://img.shields.io/travis/hactar/maplibre-pod.svg?style=flat)](https://travis-ci.org/hactar/maplibre-pod)
[![Version](https://img.shields.io/cocoapods/v/maplibre-pod.svg?style=flat)](https://cocoapods.org/pods/maplibre-pod)
[![License](https://img.shields.io/cocoapods/l/maplibre-pod.svg?style=flat)](https://cocoapods.org/pods/maplibre-pod)
[![Platform](https://img.shields.io/cocoapods/p/maplibre-pod.svg?style=flat)](https://cocoapods.org/pods/maplibre-pod)

## Description

This package turns the MapLibre Metal edition into a pod, allowing it to depended on by other pods, like Mapvox navigation.

### Updating MetalAngle
- download the .framework zips for iOS and Simulator
- extract to -simulator and -iOS
- use lipo to remove all archs except the ones we really need: iOS its arm64, simulator its arm64 and x86_64 *lipo -remove i386 MetalANGLE -output MetalAngle*
- create the framework *xcodebuild -create-xcframework -framework simulator/MetalANGLE.framework -framework MetalANGLE.framework -output "MetalANGLE.xcframework"*

## Requirements

## Installation

maplibre-pod is available through [CocoaPods](https://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'maplibre-pod', git => "https://github.com/hactar/maplibre-pod"
```

## Author

hactar, patrick@subzero.eu

## License

maplibre-pod is available under the MIT license. See the LICENSE file for more info.
