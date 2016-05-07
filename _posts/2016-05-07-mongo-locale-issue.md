---
title: MongoDB Locale Settings Issue Exit Code 1
updated: 2016-05-07 16:56
---

### Description

I was trying to bootstrap a Meteor 1.3 app, but running the command `meteor` failed due to MongoDB exiting with code 1. Turns out that MongoDB was unable to recognize my system locale settings.

### The Fix

After referring to [this comment](https://github.com/meteor/meteor/issues/4019#issuecomment-142520772) on a related Github issue, turns out that executing the following command in the terminal:

```
dpkg-reconfigure locales
```

and setting the default to `en_US.UTF-8` did the trick.
