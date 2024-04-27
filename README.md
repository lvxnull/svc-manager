# svc-manager

A simple python stdlib-only service manager.

## Service
A service is a directory located in the same directory as this script that
implements two mandatory actions, `start` and `stop`. To implement an action,
create an executable of the same name as the action and place it in the
service's directory. Currently services must be registered in the `SVCS`
variable in source code.

## Action
The following actions are currently recognized:
- `start` - Start the service
- `stop` - Stop the service
- `restart` - Restart the service. If not explicitly implemented, runs `stop`
  and then `start`.
