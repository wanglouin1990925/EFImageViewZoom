# EFImageViewZoom
A very simple IBDesignable ImageView with zoom

## Installation
Just drag `EFImageViewZoom.swift` to your project.

## How to use
Just set an UIView in your Storyboard to `EFImageViewZoom` type.
![intructions](https://media.giphy.com/media/vEBdiijlgK8BW/giphy.gif)

```swift
import UIKit

class ViewController: UIViewController, EFImageViewZoomDelegate {

    @IBOutlet weak var imageViewZoom: EFImageViewZoom!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        self.imageViewZoom._delegate = self
        self.imageViewZoom.image = UIImage(named: "14bis.png")
        self.imageViewZoom.contentMode = .left
    }

    override func didReceiveMemoryWarning() {
        super.didReceiveMemoryWarning()
        // Dispose of any resources that can be recreated.
    }
}
```

## Setup
Optionally, you can set up some properties of UIImageView

```swift
@IBInspectable public var image: UIImage! 
@IBInspectable public var _minimumZoomScale: CGFloat = 1.0 
@IBInspectable public var _maximumZoomScale: CGFloat = 6.0

public var highlightedImage: UIImage? = nil
public var isHighlighted: Bool = false 
public var animationImages: [UIImage]? = nil
public var highlightedAnimationImages: [UIImage]? = nil 
public var animationDuration: TimeInterval = TimeInterval()
public var animationRepeatCount: Int = 0 
override public var tintColor: UIColor! 

public func startAnimating()
public func stopAnimating()
public var isAnimating: Bool
```

## Screenshots
![Demo](https://media.giphy.com/media/23yu4cpEF0Dzq/giphy.gif)

## License
**EFImageViewZoom** is released under the MIT license. See the LICENSE file for more info.
