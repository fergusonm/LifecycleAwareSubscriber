# LifecycleAwareSubscriber
A wrapper around an rx subscriber that is lifecycle aware.

Usage:
```
observable.observe(lifecycleOwner) {
    // Do something
}

// No dispose needed.  It's handled by the lifecycle owner
```

As the lifecycle move in and out of an active state the observer should be subscribed and disposed as needed.  If the lifecycle goes into a destroyed state then the observer will be removed and never re-attach.

The observer doesn't need to be disposed and will behave somewhat like livedata.  Emissions call the observer's function, errorrs cause an exception.
