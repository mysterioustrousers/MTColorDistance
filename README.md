MTColorDistance
===============

A category on UIColor. Pass in an array of colors and it will return the closest color to the receiver.

### Installation

In your Podfile, add this line:

    pod "MTColorDistance"

pod? => https://github.com/CocoaPods/CocoaPods/

NOTE: You may need to add `-all_load` to "Other Linker Flags" in your targets build settings if the pods library only contains categories.

### Example Usage

    UIColor *red    = [UIColor redColor];
    UIColor *redish = [UIColor colorWithRed:0.9 green:0 blue:0 alpha:1];
    NSArray *palette = @[redish, [UIColor blueColor], [UIColor whiteColor], [UIColor greenColor]];
    
    UIColor *closestToRed = [red closestColorInPalette:palette];
  
You guessed it, `redish` will be returned.  
