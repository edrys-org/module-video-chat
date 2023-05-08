# Edrys Video Chat Module

This module adds video chat rooms to Edrys. It is based on [Jitsi](https://meet.jit.si). By default it uses the free official Jitsi instance, but you can [specify any other one](https://jitsi.github.io/handbook/docs/community/community-instances) or [self-host your own](https://jitsi.github.io/handbook/docs/devops-guide/).
 
## Usage

Simply add this URL to your class modules:

```
https://edrys-org.github.io/module-video-chat/
```

## Development

Please note **this module will only work when your Edrys server is running behind HTTPS**. Otherwise you will get errors about missing navigator objects and CORS violations. You can use [Caddy](https://caddyserver.com/download) to easily acheive that, for example:

```
caddy reverse-proxy --from localhost:8001 --to localhost:8000
```

This will run a new HTTPS server on https://localhost:8001 (assuming your Edrys is running at http://localhost:8000).

### Configuration

Optionally, you may specify the following config:
General settings: `instance`, `config`
General, Teacher, Student and Station settings: `config`
`instance`:  selects a specific Jitsi Meet instance.
The optionally `config` options are attached the URL.
General settings `config` are attached first, then depending on the role `studentConfig` `teacherConfig` or `stationConfig`

For config options see: [Jitsi Meet User Guide (advanced)](https://jitsi.github.io/handbook/docs/user-guide/user-guide-advanced/)
e.g.:

```
      "config": {
        "instance": "https://meet.jit.si",
        "config": "&config.startWithAudioMuted=true"
      },
      "studentConfig": {
        "config": "&config.startWithVideoMuted=true&stud"
      },
      "teacherConfig": {
        "config": "&config.startWithVideoMuted=true&teach"
      },
      "stationConfig": {
        "config": "&config.startWithVideoMuted=false&station"
      },
```
