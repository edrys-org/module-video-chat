# Edrys Video Chat Module

This module adds video chat rooms to Edrys. It is based on [Jitsi](https://meet.jit.si). By default it uses the free official Jitsi instance, but you can [specify any other one](https://jitsi.github.io/handbook/docs/community/community-instances) or [self-host your own](https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-start).
 
## Usage

Simply add this URL to your class modules:

```
https://edrys-org.github.io/module-video-chat/
```

Please note this module will only work when your Edrys server is running behind HTTPS. Otherwise you will get errors about missing navigator objects.

### Configuration

Optionally, you may specify the following config:

```
{
  instance: 'https://meet.jit.si'
}
```
