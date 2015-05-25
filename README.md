<p align="center">
<img src="https://raw.githubusercontent.com/tfrank64/TiltingLoader/master/TiltingLoader/Images.xcassets/tiltingLogo.imageset/tiltingLogo.png"  alt="Drawing" /></p>


TiltingLoader is a loading view you can tilt while you wait. The loader is meant to be an easy drop-in reusable UI component built in Swift that will work on iOS 7 and 8. The loader uses `UIMotionEffect` to create the tilting movement.

## Demo

Check out the DemoViewController for specific examples on how to use TiltingLoader</br>
<p align="center">
<img src="https://raw.githubusercontent.com/tfrank64/TiltingLoader/master/repo_images/tiltingloadermotion.gif"  alt="Drawing" /></p>

## Usage
** Run on a physical device for motion effects **

Create and being animating
```swift
var tlView = TiltingLoader(frame: CGRectMake(50, 50, 100, 100), color: UIColor.purpleColor(), cornerRad: 0.0)
tiltLoadingView.enableOverlayOnView(self.view)
tlView.animateColors(false)
```
Convenience create and begin animating
```swift
TiltingLoader.showTiltingLoader(self.view, color: UIColor.orangeColor(), cornerRad: 0.0)
```
Hide loader
```swift
tlView.hide()
// or to hide convenience instance
TiltingLoader.hideTiltingLoader(self.view, dynamic: true)
```

## Customization

<table>
  <caption>Init Params</caption>
  <tr>
    <td><tt> frame: CGRect</tt></td>
    <td>Simply the size of the loader within superview</td>
  </tr>
    <tr>
    <td><tt> color: UIColor</tt></td>
    <td>The color of the loader, darker colors work best.</td>
  </tr>
    <tr>
    <td><tt> cornerRad: CGFloat</tt></td>
    <td>is used to determine how rounded the corners of the loader should be.</td>
  </tr>
 </table>
</br>

Before calling animateColors() on a TiltingLoader instance, you can change the following properties:</br>

<table>
	<caption>Required Methods</caption>
	<tr>
	<td><tt>enableOverlayOnView: UIView?</tt></td>
    <td>Enable overlay behind tilting loader if superview has been passed in through this method</td>
	</tr>
	<tr>
		<td><tt>animateColors: Bool</tt></td>
    	<td>Begins color animation process by determining which color iteration method to call. When passing in false, colors animate in reverse. </td>
	</tr>
</table>

<table>
  <caption>Configureable Properties</caption>
  <tr>
    <td><tt>isAnimating: Bool</tt></td>
    <td>Getting this value determines if a loader is currently animating. Setting this value makes it so the loader will animate when animateColors() is called. Default: true</td>
  </tr>
  <tr>
    <td><tt>animationFrequency: NSTimeInterval</tt></td>
    <td>The interval for how often to swap colors in the loader, causing the animation effect. Default: 0.7</td>
  </tr>
  <tr>
    <td><tt>dynamicDismissal: Bool</tt></td>
    <td>Determines how loader will be removed from superview. If true, loader will drop out and if false, loader will fade out. Default: false</td>
  </tr>
</table>

## Screenshots

<img src="https://raw.githubusercontent.com/tfrank64/TiltingLoader/master/repo_images/rectangular.png" alt="rectangle" height="568"/>__
<img src="https://raw.githubusercontent.com/tfrank64/TiltingLoader/master/repo_images/largeRounded.png" alt="rectangle" height="568"/>


## Installation
##### To install, simple drag the TiltingLoader.swift file to your project and use it.
* Use a [briding header](https://developer.apple.com/library/prerelease/ios/documentation/Swift/Conceptual/BuildingCocoaApps/MixandMatch.html) to run in an Objective-C project.
* Coming soon: CocoaPods (Adding Swift projects to CocoaPods does not currently work) Check out this CocoaPods [issue](https://github.com/CocoaPods/CocoaPods/issues/2272) for more info and progress.

TiltingLoader requires iOS 7 or later.

## Contributing

This project is very open to contributions using the standard process below:

* Fork this repo
* Make your changes
* Submit a pull request

## Created By
[Taylor Franklin](https://github.com/tfrank64)

## License
TiltingLoader is distributed under the [MIT license](https://github.com/tfrank64/TiltingLoader/blob/master/LICENSE).
