## Verision 1.44.6

PLATFORM
- Log Levels: We've shifted some logs from "warning" to "debug" to avoid user confusion. This change ensures logs aren't seen as issues.
- Performance Upgrade: Syncs that don't meet filters won't create reports, saving database memory. It's now on by default for Jira Cloud / Getint Cloud
- Getint Archiver - Bugfix for establishing connection
- Resolved an issue with post-create updates not correctly setting up the ID or URL
- Bugfix for picking up correct mapped option marked as DEFAULT when 1:n options were mapped
- Bugfix for counting failed integration runs

APPS:
- Jira / Jira - bugfix for syncing only attachments included in the public comments
- Salesforce - bugfix for establishing connection and fetching items for synchronization
- GitLab - due date won’t be read only field anymore. It can be mapped if any other date field and synced both-ways
- Zendesk - URL field available, support for Brand and Group (agent group) fields, support for Advanced Scripting
