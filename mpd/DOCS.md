# Configuration

```yaml
volume_normalization: false
```

### `volume_normalization`

Enabled the build-in volume normalization feature.

### `verbose` (optional)

Make `mpd` verbose.

```yaml
verbose: true
```


### `custom_config` (optional)

This option let you specify an custom configuration file for MPD.
To keep all MPD files in one place I restricted the path prefix to `/share/mpd`
Please use the default [mpd.conf of the addon](https://github.com/Poeschl/Hassio-Addons/blob/master/mpd/root/etc/mpd.conf) as starting point.
In case you have issues with your configuration, the [MPD docs](https://www.musicpd.org/doc/html/user.html#configuration) might help you out.

Working example: 
```yaml
...
custom_config: /share/mpd/mpd.conf
```

# Troubleshooting

### `RTIOThread could not get realtime scheduling, continuing anyway: sched_setscheduler`

This error is shown on any none-glibc system like alpine linux is. MPD should work without it.
More see here: [MPD Issue](https://github.com/MusicPlayerDaemon/MPD/issues/218)

### `Failed to open '/data/database/mpd.db': No such file or directory`

This error is shown on the first start, when no database exists. It will be there on the second run.