UIRefreshControl+UITableView
============================

When you use `UIRefereshControl` directly with a `UITableView`, instead of with a `UITableViewController`, you are in for a lovely surprise: It is buggy. It has a white background, and it is jumpy.

This little ObjC category tries to fix it with multiple methods, whichever are available at the time. Just call your `[UIRefreshControl addToTableView:_tableView]` to add it to your table view correctly.

What really happens is that when adding a `UIRefreshControl` directly to a `UITableView`, the `UITableView` does not know of it, and is not able to handle it's scroll-dragging correctly when the `UIRefreshControl` changes the scroll insets. This category tries to tell UITableView about it so the scrolling and background color bugs are avoided.

For those concerned with AppStore Review - there are already multiple apps out there with this extension - and they were accepted without a problem.

This was originally in my other repository https://github.com/danielgindi/drunken-danger-zone/


## Me
* Hi! I am Daniel Cohen Gindi. Or in short- Daniel.
* danielgindi@gmail.com is my email address.
* That's all you need to know.

## Help

If you like what you see here, and want to support the work being done in this repository, you could:
* Actually code, and issue pull requests
* Spread the word
* 
[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=CHRDHZE79YTMQ)

## License

All the code here is under MIT license. Which means you could do virtually anything with the code.
I will appreciate it very much if you keep an attribution where appropriate.

    The MIT License (MIT)
    
    Copyright (c) 2013 Daniel Cohen Gindi (danielgindi@gmail.com)
    
    Permission is hereby granted, free of charge, to any person obtaining a copy
    of this software and associated documentation files (the "Software"), to deal
    in the Software without restriction, including without limitation the rights
    to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
    copies of the Software, and to permit persons to whom the Software is
    furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all
    copies or substantial portions of the Software.