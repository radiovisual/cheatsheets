#iOS Development


###Crash Reports

- [Understanding and Analyzing iOS Application Crash Reports](https://developer.apple.com/library/ios/technotes/tn2151/_index.html)
- [My App Crashed, Now What? – Part 1](http://www.raywenderlich.com/10209/my-app-crashed-now-what-part-1)
- [My App Crashed, Now What? – Part 2](http://www.raywenderlich.com/10505/my-app-crashed-now-what-part-2)

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

    self.viewsDictionary[@"friendsButton"] => self.friendsButton
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

    self.viewsDictionary[@"friendsButton"] => self.friendsButton
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

### UITableView

Create an offset on the bottom of the tableView so that the bottom-most item rests higher than the default. Creating
a fixed amount of space below the table view.
```obj-c
// will raise the tableview up by 50 pixels
// [self.tableView setContentInset:UIEdgeInsetsMake(0,0,50,0)];
```

### Bundle Info

Get the bundle version number:

```obj-c
[[[NSBundle mainBundle] infoDictionary] objectForKey:@"CFBundleShortVersionString"]
// or
[[NSBundle mainBundle] objectForInfoDictionaryKey:@"CFBundleShortVersionString"];
```

Auto-increment your build number before each release (warning: currently not tested)
```
#!/bin/bash
buildNumber=$(/usr/libexec/PlistBuddy -c "Print CFBundleVersion" "${PROJECT_DIR}/${INFOPLIST_FILE}")
buildNumber=$(($buildNumber + 1))
/usr/libexec/PlistBuddy -c "Set :CFBundleVersion $buildNumber" "${PROJECT_DIR}/${INFOPLIST_FILE}"
```

### Find a specific UIView

```obj-c
// Locate a specific UIView by querying for its tag
UIView *groupBtn = [self.groupsScrollContainerView viewWithTag:index];
```

### Sort an NSArray

```obj-c
// This will sort an NSArray of Strings
sortedArray = [anArray sortedArrayUsingSelector:@selector(localizedCaseInsensitiveCompare:)];

// This will sort an NSArray of objects (using the "name" property in this example)
NSSortDescriptor *sort = [NSSortDescriptor sortDescriptorWithKey:@"name" ascending:YES];
sortedArray = [anArray sortedArrayUsingDescriptors:@[sort]];

// Or for a case-insensitive compare:
NSSortDescriptor *sort = [NSSortDescriptor sortDescriptorWithKey:@"name" ascending:YES selector:@selector(caseInsensitiveCompare:)];
sortedArray = [anArray sortedArrayUsingDescriptors:@[sort]];
```

### Call any method in your App Delegate

```obj-c
// this will let you call the `someMethod` method from your
// App Delegate anywhere in any View Controller
PA_AppDelegate *appDelegate = [[UIApplication sharedApplication] delegate];
[appDelegate someMethod];
```

### Convert a JSON String into an NSDictionary

```obj-c
NSError *jsonError;
        NSData *objectData = [@"{\"2\":\"3\"}" dataUsingEncoding:NSUTF8StringEncoding];
        NSDictionary *json = [NSJSONSerialization JSONObjectWithData:objectData
                                                             options:NSJSONReadingMutableContainers
                                                               error:&jsonError];
```

### Find the location where your app icon masks are saved

```
 $ find /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneSimulator.platform/Developer/SDKs -name 'MobileIcons.framework'
```