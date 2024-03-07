# simple-unity-server
Simple golang web server to locally run gzipped Unity WebGL builds

## Requirements
Build in Unity for WebGL, with the Publisher Settings in the Player Settings set to the following:
* Compression Format: Gzip
* Decompression Fallback: Enabled

## Build
Linux (on Linux)
```bash
go build -o server main.go
```

Windows (on Linux)
```bash
GOOS=windows GOARCH=amd64 go build -o server.exe main.go
```

## Run
Either run the `server` or `server.exe` binary (depending on your OS) in the directory of the Unity build folder (with the `Build` and `TemplateData` folders). This will spin up a webserver on port 8080, so go to http://localhost:8080 to load the game.