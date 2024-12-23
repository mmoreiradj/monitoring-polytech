# Syslog

Syslog is a standard for message logging. It allows separation of the software that generates messages, the system that stores them, and the software that reports and analyzes them.

## Syslog Message Format

### Original BSD Syslog Message Format

The original BSD syslog protocol is a simple ASCII-based protocol. Each message is a single line of text, with the following format:

```
<priority>timestamp hostname: message
```

- **priority**: This is a combination of the facility and the severity level of the message. The facility is used to specify the type of program that is logging the message, while the severity level is used to specify the importance of the message.

## vrac

- automatic log rotate
- pas besoin de logrotate, configurable à un pourcentage de taille du volume sur le quel il est host
- binary format
- system.journal pour le système: process root, boot, etc.
- user-<UID>.journal for user: gui events, non root apps, services for user (pipewire), only user activities

