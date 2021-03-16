# Notification System

![](https://eskadenia.com/Portals/Portal1/Upload/Block/Image/notification--sys.jpg)

## A notification system at your service

It is a generic usable notification system. The notifications (events) are shown in User Interface and also the [Threefold Connect](TFConnect) will escalate them to user if required. Decide and manage which type of notification can escalate to your Digital Twin. You set the rules. 

## Properties for each notification

- Description (text)
- Category (dot notation)
- Severity (how serious is the event)
- Priority (what is priority to deal with it)
- Source_dtid (source digital twin id)
- Source (text info)

## Properties of escalation rules

- Audience (list of groups or digital twin id's)
- Target emails
- Target sms (not implemented yet)
- regex_description
- 1 or more categories (can be regex)
- min/max severity (define the min/max level)
- min/max priority (define the min/max level)
- Acknowledgement deadline (when does the users have to acknowledge the event= optional)
- Acknowledgement policy (minimum amount of people who need to confirm)

> More features coming soon

