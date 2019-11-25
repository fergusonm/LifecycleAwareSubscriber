# LifecycleAwareSubscriber
A wrapper around an rx subscriber that is lifecycle aware.

Usage:
```
observable.observe(lifecycleOwner) {
    // Do something
}
```

As the lifecycle move in and out of an active state the observer should be subscribed and disposed as needed.  If the lifecycle goes into a destoryed state then the observer will be removed and never re-attach.
