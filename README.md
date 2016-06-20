# Winston Logger for deepstream.io

Configuration is done in your deepstream config file.

###### Example

```yaml
logLevel: INFO
logger:
  name: winston
  options:
    # specify a list of transports (console, file, time)
    -
      type: console
      options:
        level: verbose # logLevel (INFO) will overwrite this value
        colorize: true
```

If you don't pass any options for the winston logger it defaults to the console logger with info level and colors.

###### Define multiple transports

```yaml
logger:
  name: winston
  options:
    # specify a list of transports (console, file, time)
    -
      type: console
      options:
        level: verbose
        colorize: true
    -
      type: file
      level: debug
      options:
        filename: 'logs.json'
    -
      type: time
      level: warn
      options:
        filename: time-roated-logfile
        datePattern: .yyyy-MM-dd-HH-mm
```
