# bug-autolayout
I have recently updated to `xcode8` release version and immediately encountered an issue with storyboard autolayout. 
Here is a screenshot of my constraints, which are explicitly determine positions of `UILabel` and `UISlider`

**STORYBOARD**

[![enter image description here][1]][1]

**iOS 9.3 DEVICE**



[![enter image description here][2]][2]

As you see, slider and label mispositioned and console prints following logs:

    "<NSLayoutConstraint:0x13e560cf0 UISlider:0x13e55e840.leading == UIView:0x13e55e490.leadingMargin + 9>",
    "<NSLayoutConstraint:0x13e539f40 H:[UISlider:0x13e55e840]-(10)-[UILabel:0x13e55ef00'Label']>",
    "<NSLayoutConstraint:0x13e539f90 UIView:0x13e55e490.trailingMargin == UILabel:0x13e55ef00'Label'.trailing + 9>"

  [1]: http://i.stack.imgur.com/epY59.png
  [2]: http://i.stack.imgur.com/sBSfT.jpg


The same set of constraints work **as expected** on previous version of `xcode7`. I uploaded the project to [github](https://github.com/gneil90/bug-autolayout) to reproduce the error. Is there any workaround?
