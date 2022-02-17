# Edrys Video Chat Module

This module adds video chat rooms to Edrys. It is based on [Jitsi](https://meet.jit.si). By default it uses the free official Jitsi instance, but you can [specify any other one](https://jitsi.github.io/handbook/docs/community/community-instances) or [self-host your own](https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-start).
 
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

```
{
  instance: 'https://meet.jit.si'
}
```
