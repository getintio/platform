## Verision 1.44.6 (2023-09-26)

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

## Version 1.44.5 (2023-09-14)

PLATFORM
- You can distinguish/discover right now dropdown options with the same name by comparing their IDs when you mouseover the option
- DEBUG REQUESTS responses will be loaded in a textarea for easier copying and performance improvement
- Bugfix - Enter pressed on forms won’t lead to page reload
Jira DC Apps:
- Premium feature - Migration - available. Run tasks migration directly from Jira Server/DataCenter app
- IMPORTANT !! Bugfix for number of items synced in one integration run
APPS:
- Wrike - Support for START DATE field and empty dates handling
- Freshdesk/Freshservice - support for DEPARTMENT field

## Version 1.44.4 (2023-09-10)
PLATFORM
- Important bugfix for filtering new items

## Version 1.44.3 (2023-09-08)

PLATFORM
- Fixed a usability bug related to mapping 1:n options.
- Improved dropdown functionality: You can now navigate through dropdown options using keyboard up and down arrows and select an option with the ENTER key.
- On dedicated or migration instances, the license warning will no longer be present. Additionally, the Jira license warning will only be displayed when the license from Jira is fetched.

Jira DC Apps:
- For Jira DC apps, switch to our new Intercom chat.

APPS:
- Jira / Azure - Fixed a bug in syncing Labels with Tags
- Asana - tasks without titles will be skipped from synchronization and won't generate failures anymore.
- Jira - fetching all service desk organizations with pagination.

## Version 1.44.2 (2023-08-29)
PLATFORM
- Bugfix for copy/paste feature doesn’t work
- Import feature fix, replaced uploading a file to a textarea where you can just type or paste list of items to import
- Security bugfix

Jira DC Apps:
- fix for options not loading due to a json parsing issue

APPS:
- Wrike - display fields with a space ID to distinguish them correctly

## Version 1.44.1 (2023-08-24)
PLATFORM
- Dropdown field can not be updated after the item is created (e.g. Priority - Jira Priority)
- A way to link item with some already existing item by setting up a value in the custom field
- Dropdowns bugfix - options filtering should work without problems
- Filtering items bugfix - display field only once instead of multiple times in filters
- Cloud security improvements

## Version 1.44.0 (2023-08-09)
PLATFORM
- Status custom field - no need to add them to fields mappings to successfully synchronize status.
- Update on Create - New option in field mapping configuration that let you to update a field with a value from selected field belonging to a newly created item, e.g. once new item is created you can store its url or id in custom field of source item that triggered the sync.
- Fix for casting Integer and Double fields
- Notion Connection alpha version released !!
- Airtable Connection alpha version released !!
- Trello Connection alpha version released!!

APPS:
- Azure - Fetching iterations paths from all team that belong to the synchronized project
- Wrike - support for EU located accounts - so far there was error when setting up connection

## Version 1.43.1
PLATFORM
- OnPremise - warning bar on dashboard page when using default H2 database which is designed only for a test purposes

APPS:
- Azure DevOps Server - possibility to provide collection name - for now only Default Collection was provided
- Azure DevOps - fetching iteration paths also from a team settings - missing so far iterations should be available for pick up
- Asana - fetching subtasks of the task in a paginated way. Till now if there was to much subtasks integration was just failing
- Wrike - added support for Milestone task types

## Version 1.43.0
Platform:
- Improved mappings !! copy & paste already mapped options. Use auto-mapping feature to automatically map options for you.
- Syncs warnings !! Directly on the syncs report you can will see warnings related to particular sync. Warnings for now will relate to number of warn logs that were printed during the sync and to number of missing options that were not found by Getint which could end up in potential field value being not correctly synchronized.
- Notifications for warnings !! stay notified via email or slack about warnings that were encountered during your items syncs

APPS:
- Bugfix - for Wrike and Servicenow if both counterparts were changed, Getint faild to propagate changes
- Salesforce - fixed automatic token refreshing
- Wrike - status mappings - statuses will be available to map - fetched via api/c4/workflows endpoint
- GitLab - fixed creating connection with self hosted GitLab
## Version 1.42.6
Platform:
- Fix in syncing items with the same IDs
- Transition fields - fixed styling for a new window with transition fields which was till now malformed and hard to use

APPS:
- Asana - fix for custom text fields value extraction
- Jira - support for user fields
