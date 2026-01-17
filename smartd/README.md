# smartd

A very simple configuration that monitors temperatures and posts a
message if they get higher than 45°C. It's just to experiment and get a
fundamental understanding of monitoring and notifying. Hopefully, this
will help me set up a better solution in the future.

This configuration prints the notifications (if any) to /run/motd/motd.
We use this instead of the classic /etc/motd because we don't want the
notifications to persist indefinitely. The alternative would be to clean
it up on some timer, but it's probably not required for this sort of
notification. It's recommended to symlink /etc/motd to this instead of
using it directly, because that would be the standard location.

```sh
ln -sf /run/motd/motd /etc/motd
```

Make sure to check for its existence. If I see that programs are
confused by this then I'll consider creating an empty file at startup.
