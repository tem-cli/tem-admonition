Detects changes in certain files in your project. Based on rules defined by you,
it notifies you to verify that you have satisfied all admonitions and caveats
defined in those files.

## Example

```
file1.py
# NOTE: When editing this, make sure that file2.py is modified accordingly
var = [1, 2, 3]
```

```
file2.py
...
```

You can specify a rule that will notify the user:
```
file1.py has changed. Make sure you have followed all admonitions in this file:

# NOTE: When editing this, make sure that file2.py is modified accordingly

Please confirm [y/n]:
```

Perhaps you can set this check to be performed each time you commit your
changes, and notify the user only when `file1.py` has changed. If the user
doesn't confirm, the commit operation is aborted.

Some rules could be fully automatic, without requiring user confirmation.
