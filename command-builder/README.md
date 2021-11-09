# command-builder

## Link it

```
npm link
```

## Use it in another angular project

### Link to it

```
npm link @example/command-runner
```

### Define the command in angular.json

```
      .
      .
      .
      "architect": {
        "explore": {
          "builder": "@example/command-runner:command",
          "options": {
            "command": "explorer",
            "args": [
              "/e",
              ",",
              "."
            ]
          }
        },
        "dir": {
          "builder": "@example/command-runner:command",
          "options": {
            "command": "cmd",
            "args": [
              "/C",
              "dir",
              "."
            ]
          }
        },
        "cnn": {
          "builder": "@example/command-runner:command",
          "options": {
            "command": "cmd",
            "args": [
              "/C",
              "C:\\Program Files (x86)\\Google\\Chrome\\Application\\chrome.exe",
              "--url",
              "https://cnn.com"
            ]
          }
        },
        .
        .
        .
```

### Run various targets for ```@example/command-runner```

```
ng run command-builder-test:explore
```

or

```
ng run command-builder-test:dir
```

or

```
ng run command-builder-test:cnn
```