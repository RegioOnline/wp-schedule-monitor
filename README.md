# WP Schedule Monitor

WP Schedule Monitor is a lightweight WordPress plugin that monitors scheduled posts and automatically recovers publications that WordPress has missed.

WordPress normally publishes scheduled posts through WP-Cron. In some situations, a scheduled post may remain unpublished after its scheduled time. WP Schedule Monitor provides an additional safety net by periodically checking for missed scheduled posts and publishing them when necessary.

## Beta status

**Current version: 0.4.1-beta.2**

WP Schedule Monitor is currently in beta testing.

The plugin has been running in a live WordPress production environment. During the current practical test:

- 5 missed scheduled publications were detected and successfully recovered
- 0 recovery attempts failed
- All recovered posts were published correctly
- The original scheduled publication time was preserved
- Recovery occurred approximately five minutes after the missed publication time

More installations and different WordPress environments are now needed to broaden testing.

## Features

- Automatically monitors scheduled WordPress posts
- Detects missed scheduled publications
- Automatically publishes eligible missed posts
- Preserves the original scheduled publication time
- Configurable safety margin
- Configurable maximum number of recoveries per check
- Manual check and recovery option
- Recovery log with successful and failed attempts
- CSV export of the recovery log
- Diagnostic information for troubleshooting
- Automatic cleanup of old log entries
- Compatible with normal WP-Cron operation
- Can also be used on installations where cron is triggered externally

## Languages

English is the default plugin language.

A complete Dutch (`nl_NL`) translation is included. WordPress automatically uses the appropriate translation based on the site's active locale.

## Installation

1. Download the latest beta ZIP from the **Releases** section of this repository.
2. In WordPress, go to **Plugins → Add New Plugin → Upload Plugin**.
3. Select the ZIP file and install it.
4. Activate **WP Schedule Monitor**.
5. Open **Schedule Monitor** in the WordPress admin menu.
6. Verify that the status is shown as active and that a next check is scheduled.

No modification of WordPress core files is required.

## Default configuration

The plugin is designed to work with sensible defaults. Testers can review and change the available settings from the Schedule Monitor administration page.

The plugin only records actual recovery attempts in its recovery log. Normal checks update the current status without filling the log with unnecessary entries.

## Beta testing

This is beta software. Backups and normal WordPress testing precautions are recommended.

Testers are especially welcome to report:

- Successful automatic recoveries
- Failed recovery attempts
- Unexpected behaviour
- Compatibility problems
- Cron-related issues
- Problems with the administration interface or logging

When reporting a problem, please include the WordPress version, PHP version and relevant diagnostic information shown by WP Schedule Monitor whenever possible.

## Reporting issues

Please use the **Issues** section of this GitHub repository to report bugs, compatibility problems or other technical feedback.

Before opening a new issue, please check whether the same problem has already been reported.

## Scope

WP Schedule Monitor is intentionally focused on one task: providing an additional safety net for missed scheduled WordPress posts.

It is not intended to replace WordPress cron, external cron services, Action Scheduler or general-purpose job queues.

## License

WP Schedule Monitor is licensed under the GNU General Public License v2.0 (GPL-2.0).

## Project status

The plugin is being expanded from successful testing on its original production environment to a broader external beta test.

Feedback from different WordPress installations, hosting environments and cron configurations is welcome.

