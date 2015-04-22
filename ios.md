#iOS Development

###Building Universal Apps

- [Building a Universal App](http://themainthread.com/blog/2014/02/building-a-universal-app.html)

###Auto Layout & Constraints

- [Learn to Love Auto Layout Programmatically](http://www.thinkandbuild.it/learn-to-love-auto-layout-programmatically/)
- [Advanced Auto Layout Toolbox](http://www.objc.io/issue-3/advanced-auto-layout-toolbox.html)

###viewDictionary Helpful Hints

These two lines of code will give you the same output:

Explicit Version:
```obj-c
    self.viewsDictionary = @{
                              @"friendsButton":self.friendsButton,
                              @"friendsSub":self.friendsSub,
                              @"friendsUnderline":self.friendsUnderline,
                              @"notificationsButton":self.notificationsButton,
                              @"notificationsSub":self.notificationsSub,
                              @"notificationsUnderline":self.notificationsUnderline
                              };
```

Using `NSDictionaryOfVariableBindings` gives you the same result
```obj-c
     self.viewsDictionary = NSDictionaryOfVariableBindings(self.friendsButton,
                                                           self.friendsSub,
                                                           self.friendsUnderline,
                                                           self.notificationsButton,
                                                           self.notificationsSub,
                                                           self.notificationsUnderline);
```
