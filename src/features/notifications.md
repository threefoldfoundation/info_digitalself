# Notification System

!()[https://eskadenia.com/Portals/Portal1/Upload/Block/Image/notification--sys.jpg]

Generic usable notification system.

The notifications (events) are shown in UI and also the ThreeFold connect will try to escalate to user if required.

- notification relay rules
  - who can escalate to our digital twin and we relay and manage the notification
- escalation rules
  - what needs to happen with the notification

## implementation

- stored as [dtml](dtml) or json files on [dtfs](dtfs)
- interface = [dtftp](dtftp) & rest
- index in [redis server](tdredis)
- notifications can be given to Digital Twin over rest (maybe redis interface)

Properties for each notification

- description (text)
- category (dot notation)
- severity (how serious is the event)
- priority (what is priority to deal with it)
- source_dtid (source digital twin id)
- source (text info)

Properties of escalation rules

- audience (list of groups or digital twin id's)
- target_emails
- target_sms (future)
- regex_description
- 1 or more categories (can be regex)
- min/max severity
- min/max priority
- acknowledgement_deadline (when does user have to acknowledge = optional)
- acknowledgement_policy (minimal amount of people who need to confirm)
  - e.g. 5 people recieve the notification, 3 of 5 need to confirm
  - if escalation done then the notification get's closed

> assign: lee/maxime/kristof

## Roadmap

- fall back to SMS (allow user to speficy e.g. API key of twilio)
- web based userinterface (time to be defined)
