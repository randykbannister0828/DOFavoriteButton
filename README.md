# DOFavoriteButton

Cute Animated Button written in Swift.
It could be just right for favorite buttons!

## Requirements
* iOS 7.0+
* Swift 1.2

## Installation

#### Manual
Just drag DOFavoriteButton.swift to your project.

## How to use
#### 1. Add a flat icon image
![Flat Icon Image](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/flatIconImage.png)

#### 2. Create a button
##### ・By coding
```swift
let button = DOFavoriteButton(frame: CGRectMake(0, 0, 44, 44), image: UIImage(named: "star.png"))
self.view.addSubview(button)
```

##### ・By using Storyboard or XIB
1. Add Button object and set Custom Class `DOFavoriteButton`  
![via Storyboard](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/storyboard.png)

2. Connect Outlet  
![connect outlet](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/connect.png)

#### 3. Add tapped function
```swift
button.addTarget(self, action: Selector("tapped:"), forControlEvents: .TouchUpInside)
```
```swift
func tapped(sender: DOFavoriteButton) {
    if sender.selected {
        // deselect
        sender.deselect()
    } else {
        // select with animation
        sender.select()
    }
}
```

## Customize
You can change button color & animation duration:
```swift
button.imageColorOff = UIColor.brownColor()
button.imageColorOn = UIColor.redColor()
button.circleColor = UIColor.greenColor()
button.lineColor = UIColor.blueColor()
button.duration = 3.0 // default: 1.0
```
Result:  
![Customize](https://raw.githubusercontent.com/okmr-d/okmr-d.github.io/master/img/DOFavoriteButton/changeColor.gif)

## DEMO
There is a demo project added to this repository, so you can see how it works.
