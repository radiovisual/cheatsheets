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

Using `NSDictionaryOfVariableBindings` gives you the same result as above, where the result is a dictionary where the keys are generated automatically from the object variable names (self.foo => @"foo"). This allows for a cleaner and easier-to-update syntax.
```obj-c
    self.viewsDictionary = NSDictionaryOfVariableBindings(
        self.friendsButton,
        self.friendsSub,
        self.friendsUnderline,
        self.notificationsButton,
        self.notificationsSub,
        self.notificationsUnderline
    );
```


### UITableViewCell

Use a color other than the supplied defaults to style the UITableViewCell's 'selected' style:

```obj-c
// In -tableView:cellForRowAtIndexPath:object:
UIView *selectionView = [[UIView alloc] initWithFrame:CGRectMake(0, 0, cell.frame.size.width, cell.frame.size.height - 1)];
selectionView.backgroundColor = [UIColor redColor];
cell.selectedBackgroundView = selectionView;
return cell;

// Or in your subclass of UITableViewCell:
UIView *selectionView = [[UIView alloc] initWithFrame:CGRectMake(0, 0, self.frame.size.width, self.frame.size.height - 1)];
selectionView.backgroundColor = [UIColor redColor];
self.selectedBackgroundView = selectionView;
```