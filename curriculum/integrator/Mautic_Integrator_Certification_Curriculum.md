# Certified Mautic Integrator Curriculum

## Course Overview

This comprehensive curriculum is designed to train technical implementers to become certified Mautic integrators, covering everything from server fundamentals and installation through configuration, operations, deployment, security, theming and third-party integration. Where the Developer track certifies writing code inside Mautic, the Integrator track certifies the engineering discipline that gets Mautic installed, configured, connected, secured, upgraded and kept running in production. An Integrator is not expected to write or read core Mautic PHP, but is expected to work confidently with configuration files and the command line, wire Mautic to external systems, and make safe operational decisions under production constraints.

## Prerequisites

- Linux shell experience (navigation, permissions, file transfer, redirection)
- Basic PHP literacy (reading configuration arrays, awareness of Symfony as a framework)
- Understanding of web development (HTML, CSS, JavaScript)
- Database administration basics (MySQL/MariaDB, dumps, users and privileges)
- Awareness of what a Mautic instance needs from DNS and TLS: a domain pointing at the server and a valid HTTPS certificate, so that the Site URL can be set to an https address
- Working knowledge of Mautic as an end user, at the level of the Mautic Marketer Certification

## Module 1: Open Source, the Mautic Project and the Release Cycle

### Learning Objectives
- State Mautic's licence and explain what GPL v3 permits and requires
- Describe the Mautic Community's governance structure and its teams
- Explain Mautic's time-based release strategy and its alignment to Symfony
- Identify which release in a series is the LTS and calculate a release's support window
- Choose an appropriate target version for a new client build given a support horizon

### Context
Choosing a Mautic version is a contractual decision as much as a technical one, because support windows determine how long a client keeps receiving security fixes. This module establishes the project context an integrator needs before recommending a version or a maintenance agreement.

### Key Topics
- Open source principles and what a copyleft licence means for client work
- Mautic's licence, project history and stated community purpose
- Governance: the five teams, elected leadership, the Community Council and the General Assembly
- Decision-making timeframes and lazy consensus as the default method
- Time-based release strategy and the major release interval aligned to Symfony
- LTS designation within a series, and active versus security support windows
- Extended Long Term Support as a paid, per-instance programme
- Reading the releases table to select a version for an engagement
- Mautic's role as a CVE Numbering Authority

### Official Reference Links
- [About Mautic](https://contribute.mautic.org/en/latest/about/about.html)
- [Governance Model](https://contribute.mautic.org/en/latest/governance/governance_model_v2.html)
- [Mautic Releases](https://mautic.org/releases/)
- [Mautic Release Strategy and LTS](https://mautic.org/blog/introducing-mautics-new-release-strategy-long-term-support-elts/)
- [Extended Long Term Support](https://mautic.org/extended-long-term-support-elts/)
- [Mautic Security](https://mautic.org/security)
- [Mautic authorized as a CVE Numbering Authority (CNA)](https://mautic.org/blog/mautic-authorized-cve-numbering-authority-cna/)
- [mautic/mautic](https://github.com/mautic/mautic)
- [The Open Source Definition](https://opensource.org/osd)

## Module 2: Mautic Repositories, Releases and Translation

### Learning Objectives
- Find the Mautic repository, release or file you need on GitHub
- Read shipped configuration defaults straight from the Mautic source files
- Track releases and security advisories for the version a client runs
- Report a problem with the detail Mautic asks for
- Manage and contribute Mautic translations

### Context
Mautic publishes no reference page for the settings held in the local configuration file, so the shipped configuration files in the Mautic repository are often the only authoritative source for a parameter name or its default. The same repository carries the releases and security advisories that tell an integrator when a client's instance needs attention. This module covers finding and reading that material, reporting problems and managing translations - none of which requires writing code or working with version control.

### Key Topics
- The Mautic organisation on GitHub and which repository holds what
- Releases and tags, and identifying the release a client's instance is running
- Reading shipped configuration defaults from the bundle configuration files
- Watching releases and security advisories for a supported version
- Reporting a problem: reproduction steps, the Mautic and PHP versions, and the errors found in the log files
- Translation platform workflow, the daily language pack generation cycle, and forcing a pack refresh
- System default language, per-user language, and string override files

### Official Reference Links
- [Contributing as a Translator](https://contribute.mautic.org/en/latest/contributing/translator.html)
- [Translations](https://docs.mautic.org/en/6.0/translations/translations.html)
- [Mautic Releases](https://mautic.org/releases/)
- [mautic/mautic](https://github.com/mautic/mautic)
- [mautic/recommended-project](https://github.com/mautic/recommended-project)
- [mautic/api-library](https://github.com/mautic/api-library)
- [GitHub Repositories Documentation](https://docs.github.com/en/repositories)
- [Transifex Help Center](https://help.transifex.com/en/)

## Module 3: Web Server, PHP/Symfony and Shell Fundamentals

### Learning Objectives
- State Mautic 6's supported web servers, PHP versions and required PHP extensions
- Diagnose and correct PHP resource limit failures
- Set correct file ownership and permissions for a Mautic install
- Work safely in a shell on a production server and recognise destructive commands
- Explain Symfony's role in Mautic and locate the conventions Mautic inherits

### Context
Almost every Integrator task ultimately happens over SSH against a web server the integrator configured. Mautic publishes very little server configuration of its own, so this module builds that competence from the web servers' and PHP's own documentation and layers Mautic's specific rules on top.

### Key Topics
- Supported PHP versions, required extensions, and npm as a requirement from Mautic 5.0
- Supported web servers, and mod_rewrite or equivalent rewrite configuration for SEO URLs
- Document root rules: the project root for a package install, the docroot directory for a Composer install
- Shared hosting exclusion and the VPS or dedicated server alternative
- PHP resource settings, the documented minimum execution time, and the master versus local value distinction
- Configuration testing and reload for Apache; equivalent Nginx handling
- `.htaccess` as a Composer scaffold file and as a last-resort PHP override
- File ownership and permission reset, identifying the web server user, and common root causes of permission failure
- Shell fundamentals: navigation, search, ownership, permissions, remote copy, redirection and log capture
- Shell scripting for maintenance tasks, and running console commands non-interactively
- Destructive-command awareness: recursive removal, data cleanup, and fixture loading which purges the database
- Symfony's contribution: HTTP kernel, service container, environments, Console, Mailer, Messenger; Doctrine as the ORM
- Bundle organisation, and reading a bundle's configuration file to discover parameters and defaults

### Official Reference Links
- [Mautic Requirements](https://mautic.org/mautic-requirements/)
- [Working with Resource Limits](https://docs.mautic.org/en/6.0/troubleshooting/working_with_resource_limits.html)
- [File Ownership and Permissions](https://docs.mautic.org/en/6.0/troubleshooting/file_ownership_permissions.html)
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Plugin Structure](https://devdocs.mautic.org/en/6.0/plugins/structure.html)
- [PHP Manual](https://www.php.net/manual/en/index.php)
- [PHP Supported Versions](https://www.php.net/supported-versions.php)
- [Apache HTTP Server 2.4 Documentation](https://httpd.apache.org/docs/2.4/)
- [nginx documentation](https://nginx.org/en/docs/)
- [Configuring Symfony](https://symfony.com/doc/current/configuration.html)
- [POSIX Shell Command Language](https://pubs.opengroup.org/onlinepubs/9799919799/utilities/V3_chap02.html)
- [chown(1) Linux manual page](https://man7.org/linux/man-pages/man1/chown.1.html)
- [scp(1) OpenBSD manual page](https://man.openbsd.org/scp)

## Module 4: Database Server Basics and the Mautic Data Model

### Learning Objectives
- State the supported database engines and minimum versions for Mautic 6
- Configure Mautic's database connection parameters, including a table prefix
- Run Doctrine schema and migration commands safely
- Perform routine optimization and maintenance on Mautic's tables
- Explain why the configured table prefix must be allowed for when querying the database

### Context
Mautic is a write-heavy application whose tables grow continuously through tracking, campaign logs and email statistics. Integrators are regularly asked to answer questions the interface cannot, or to migrate data in and out, and doing so safely requires understanding how the schema is generated and which conventions constrain it.

### Key Topics
- Supported engines and minimum versions, and the InnoDB requirement
- Connection parameters, table prefix, and the read-only replica host parameter
- Mautic's documented MySQL global settings
- That Mautic generates and owns its schema, so tables are not altered by hand
- Configurable table prefixes, and allowing for them when querying the database directly
- The reporting and statistics tables exposed through the stats endpoint
- Contact, campaign, email, form, page and point log tables; audit log, IP address and webhook log tables
- The Messenger queue table
- Schema and migration commands, including the dry-run form that prints SQL without executing it
- The in-app schema check endpoint
- Table optimization and housekeeping for growth-prone tables
- Reading the live schema on a client instance rather than assuming it

### Official Reference Links
- [Mautic Requirements](https://mautic.org/mautic-requirements/)
- [Stats API](https://devdocs.mautic.org/en/6.0/rest_api/stats.html)
- [Troubleshooting](https://docs.mautic.org/en/6.0/troubleshooting/troubleshooting.html)
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Command Line Interface](https://docs.mautic.org/en/6.0/configuration/command_line_interface.html)
- [MySQL OPTIMIZE TABLE](https://dev.mysql.com/doc/refman/8.0/en/optimize-table.html)
- [MariaDB Documentation](https://mariadb.com/kb/en/documentation/)

## Module 5: Installing Mautic without Composer

### Learning Objectives
- Run the pre-flight environment checks and interpret their colour coding
- Complete a package and web-installer installation end to end
- Complete a fully non-interactive command line installation
- Pre-seed installation parameters through a configuration file
- Decide between SMTP and API-based sending at install time

### Context
The package installation remains common for smaller instances and for environments where Composer is unavailable. Understanding it also explains what the Composer install is doing differently, which matters when converting an existing instance later.

### Key Topics
- Downloading, uploading and unzipping the package, and permissions for the web server user
- Environment checks and the error, warning and success result semantics
- Installer stage order: environment checks, database, administrator account, email settings, log in
- Database setup fields, table prefix, and the backup existing tables option and its default
- Command line installation and its documented database, admin and mailer options
- The backup table prefix default and the encryption and authentication mode values
- Installer stage output and how to read a failure
- Pre-seeding a configuration file, and the two parameters that must be omitted
- The complex administrator password requirement from Mautic 5.1
- API-based sending versus SMTP, and the option to queue rather than send immediately
- Securing the installation with HTTPS

### Official Reference Links
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Mautic Requirements](https://mautic.org/mautic-requirements/)
- [Mautic Download](https://mautic.org/download)
- [Command Line Interface](https://docs.mautic.org/en/6.0/configuration/command_line_interface.html)

## Module 6: Composer, Packagist and the Mautic Marketplace

### Learning Objectives
- Explain Composer, Packagist, and the roles of the manifest and lock file
- Create a new Mautic project from the Recommended Project template
- Explain the Recommended Project's directory contract and configure a web server for it
- Change the web root for a new and an existing project
- Convert an existing package install to a Composer-managed install
- Manage plugins through the Mautic Marketplace and understand its Packagist requirements

### Context
From Mautic 6, Composer is the default way to install, update and manage Mautic. The Recommended Project imposes a directory contract that changes web server configuration, file locations and the entire update procedure, so this module is foundational for everything operational that follows.

### Key Topics
- Composer fundamentals: the manifest, the lock file, version constraints, require and update
- Packagist as the package index Composer resolves against
- Creating a project from the Recommended Project template
- The directory contract: the docroot directory, autoloader location, and plugin and theme install paths
- Scaffolding, the files it writes, and automating it through Composer script hooks
- Applying patches to packages with the patches plugin
- Pinning the platform PHP version
- Migrating a package install to Composer: minimum version, files to copy, directory swap, web server repoint
- That the database is untouched by the switch and existing data is retained
- Enabling full Composer management, which also enables the Marketplace
- Marketplace history, its Composer and Packagist foundation, and the version-compatibility caveat
- Listing a plugin: the required package type, install directory name, core library constraint and allow-list approval

### Official Reference Links
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Switching to Composer](https://docs.mautic.org/en/6.0/getting_started/switching_composer.html)
- [Mautic Marketplace](https://docs.mautic.org/en/6.0/marketplace/marketplace.html)
- [Marketplace Getting Started](https://devdocs.mautic.org/en/6.0/marketplace/getting_started.html)
- [Listing a Plugin on the Marketplace](https://devdocs.mautic.org/en/6.0/marketplace/listing.html)
- [mautic/recommended-project](https://github.com/mautic/recommended-project)
- [Composer Documentation](https://getcomposer.org/doc/)
- [Packagist](https://packagist.org/about)

## Module 7: Local Development with DDEV

### Learning Objectives
- Explain what DDEV provides and why Mautic standardises on it
- Start a Mautic instance with DDEV from a clone of the repository
- Identify the services DDEV provisions and how to reach them
- Run Mautic console commands inside DDEV
- Read the shipped DDEV configuration and explain what it pins

### Context
DDEV is Mautic's officially recommended local environment and its configuration ships inside the repository. For an integrator it is the safest place to rehearse upgrades, test plugins and reproduce client issues before touching production.

### Key Topics
- DDEV and Docker or Colima prerequisites
- Starting Mautic with a clone and a single start command
- Services provisioned: MailHog, PHPMyAdmin and Redis Commander
- The default host name and default credentials
- Reading the shipped configuration: PHP version, web server type, database version, Composer version, upload directories, extra packages
- The bootstrap script sequence and where it writes the local configuration file
- Running Mautic console commands inside the container
- Common DDEV verbs for starting, stopping and running commands inside the environment
- Using DDEV to rehearse an update or reproduce a client bug

### Official Reference Links
- [How to Install Mautic with DDEV](https://devdocs.mautic.org/en/6.0/development-environment/how_to_install_with_ddev.html)
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Mautic DDEV configuration](https://github.com/mautic/mautic/blob/6.x/.ddev/config.yaml)
- [Local Mautic development with DDEV](https://mautic.org/blog/local-mautic-development-with-ddev/)
- [DDEV Documentation](https://docs.ddev.com/en/stable/)

## Module 8: Mautic Configuration — UI and local.php

### Learning Objectives
- Navigate every tab of Settings and Configuration and state what it controls
- Locate the local configuration file for Mautic 6 and explain the path change from earlier versions
- Set core parameters: URLs, paths, trusted hosts and proxies, CORS, cookies, locale and date formats
- Configure Mautic behind a reverse proxy or SSL-terminating load balancer
- Override any parameter through an environment variable
- Explain the environment file precedence rules and production compilation

### Context
Mautic exposes the same settings through three surfaces — the user interface, the local configuration file, and environment variables — and an integrator must know which surface wins. Because Mautic publishes no parameter reference page, the shipped bundle configuration files are frequently the only authoritative source for parameter names and defaults.

### Key Topics
- The Configuration tabs and what each one controls
- Where the local configuration file lives, and how its values relate to the settings shown in the UI
- Path overrides for themes, media, plugins, translations and assets
- Core parameters and defaults: site URL, cache and log paths, image and temp paths, theme, locale, timezone, date formats, page limit, cached data timeout
- Site URL as the value cron jobs need to build absolute links
- Trusted hosts and trusted proxies for reverse-proxy and SSL-terminating deployments
- CORS restriction, its default, and the valid domain formatting rules
- Cookie, remember-me and security header parameters and their defaults
- API settings and the default token lifetimes
- Asset directory placement outside the public web root
- IP lookup service configuration and the licence key format
- The tokens reference — contact fields, unsubscribe and web view links — which is separate from the configuration parameters
- Environment file precedence, real environment variables winning, and the secrets prohibition
- The uppercase prefixed environment variable mapping for any parameter, and production compilation

### Official Reference Links
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Tokens and Variables](https://docs.mautic.org/en/6.0/configuration/variables.html)
- [MaxMind Licence](https://docs.mautic.org/en/6.0/configuration/maxmind_license.html)
- [URL Shortener](https://docs.mautic.org/en/6.0/configuration/shortener.html)
- [Tracking Script](https://docs.mautic.org/en/6.0/configuration/tracking_script.html)
- [Development Environments](https://devdocs.mautic.org/en/6.0/development-environment/environments.html)
- [Mautic paths configuration](https://github.com/mautic/mautic/blob/6.x/app/config/paths.php)
- [Mautic core configuration defaults](https://github.com/mautic/mautic/blob/6.x/app/bundles/CoreBundle/Config/config.php)
- [Configuring Symfony](https://symfony.com/doc/current/configuration.html)

## Module 9: Customizing Mautic and Configuration Best Practices

### Learning Objectives
- Create and manage custom fields, including background column creation and field width optimization
- Design a role and permission model and read Mautic's permission notation
- Configure categories, tags, stages, points and dynamic content correctly
- Apply the documented performance-oriented configuration settings
- Configure Symfony Messenger queueing and choose a transport

### Context
Most client-specific Mautic behaviour is configuration rather than code, and a default configuration is tuned for a small instance. Scaling to high contact counts and send volumes is largely a configuration exercise, and the relevant settings are scattered across several tabs.

### Key Topics
- Custom field types, identifier fields, and the listing icon semantics
- Background column creation, the command that materialises the column, and when to schedule it
- Analysing and optimising field storage when approaching the leads table limit
- Custom countries and regions files
- Roles, the full system access switch, and the view, edit, create, delete, activate and full permission model
- Own versus others scoping, and the export permission
- User management, password rules, and the fact that Mautic sends no credential emails
- Categories and the elements they apply to; tags and their segment filter operators and search syntax
- Stages, stage weight, and single-stage membership
- Points, point actions, point triggers and point groups, including the webhook that group points do not fire
- Dynamic web content, campaign-based versus filter-based, and its template slot name
- Documented performance settings: campaign summary statistics, background import threshold, segment rebuild warning, webhook queue mode
- Queueing off by default; the Messenger transports and their prerequisites
- Consuming the queue, supervising workers, retry strategy and failure transports

### Official Reference Links
- [Custom Fields](https://docs.mautic.org/en/6.0/contacts/custom_fields.html)
- [Managing Roles](https://docs.mautic.org/en/6.0/users_roles/managing_roles.html)
- [Managing Users](https://docs.mautic.org/en/6.0/users_roles/managing_users.html)
- [Categories Overview](https://docs.mautic.org/en/6.0/categories/categories-overview.html)
- [Tags](https://docs.mautic.org/en/6.0/contacts/tags.html)
- [Stages](https://docs.mautic.org/en/6.0/stages/stages.html)
- [Points](https://docs.mautic.org/en/6.0/points/points.html)
- [Point Groups](https://docs.mautic.org/en/6.0/points/point_groups.html)
- [Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html)
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Message Queue](https://docs.mautic.org/en/6.0/queue/message_queue.html)
- [Mautic Messenger configuration defaults](https://github.com/mautic/mautic/blob/6.x/app/bundles/MessengerBundle/Config/config.php)
- [Symfony Messenger](https://symfony.com/doc/current/messenger.html)

## Module 10: Cron Jobs and Console Commands (Integrator Level)

### Learning Objectives
- Install the required cron jobs in the correct order with correct staggering
- Choose and tune batch limits for segment and campaign processing
- Select the correct optional cron jobs for a given feature set
- Use the console safely and non-interactively, and capture output
- Diagnose cron failures caused by the PHP binary, argument handling or interactivity
- Distinguish commands that look similar but do different things

### Context
Mautic does almost nothing on a schedule unless an integrator makes it, which makes cron configuration the single most common cause of "Mautic isn't working" tickets. Several commands have near-identical names and materially different effects.

### Key Topics
- Crontab syntax and scheduling; running Mautic commands from bin/console
- The documented staggering example and the resulting processing order
- Required jobs: segment update, campaign update, campaign trigger, marketing message queue send, custom field column creation
- Batch size defaults and the flags that override them
- How a per-run contact cap differs from a per-batch size, and which of the segment, campaign rebuild and campaign trigger commands accept each
- Campaign trigger ordering from newest to oldest since Mautic 5.1
- Optional jobs: email queue consumption, monitored email fetch, social monitoring, imports, scheduled exports, webhooks, IP lookup, cleanup, do-not-sell, broadcasts, scheduled reports, integration sync, plugin reload
- Why the queue consumer requires a memory, message or time limit under cron
- Webhook range mode for large backlogs
- Data cleanup flags including the dry run and the GDPR retention flag
- Broadcast throttling flags and safe parallelisation by contact ID range
- The exclude option and the three commands that support it
- Commands easily confused: Symfony cache clear versus Mautic cache clear, campaign update versus trigger, marketing message queue versus Messenger mail queue, asset generation
- Command aliases, non-interactive execution, output redirection, and the PHP binary and argument workarounds

### Official Reference Links
- [Cron Jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [Command Line Interface](https://docs.mautic.org/en/6.0/configuration/command_line_interface.html)
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Custom Fields](https://docs.mautic.org/en/6.0/contacts/custom_fields.html)
- [Symfony Console Commands](https://symfony.com/doc/current/console.html)
- [crontab(5) Linux manual page](https://man7.org/linux/man-pages/man5/crontab.5.html)

## Module 11: Updating Mautic, Backup and Restore

### Learning Objectives
- Define what Mautic considers an acceptable backup
- Update a package install and a Composer-managed install
- Roll back a failed Composer update
- Set an appropriate update stability level
- Diagnose and recover from a failed update
- Build a staging environment to rehearse an update

### Context
Mautic makes a tested backup a hard precondition for every update but publishes no procedure for taking one, so the integrator must supply it. The update procedure itself differs completely between installation methods, and the browser-based updater no longer exists.

### Key Topics
- Mautic's definition of a tested backup: files and database, re-created in a separate environment and verified working
- Database dumps with vendor tooling, and consistency considerations for a live instance
- Filesystem backup scope: configuration, media, plugins, themes, translations
- The Composer manifest and lock file as the codebase rollback mechanism
- Installer-level table backup behaviour and the backup table prefix
- Package update at the command line: find, apply, then finish
- Composer update: version bumps, dependency update, scaffolding review, then the database command block
- Update stability levels and why early-access releases never belong in production
- Browser update deprecation and complete removal
- Failed-update recovery: cache clear, manual trigger, migration status, manual file replacement and which files to restore
- The schema check endpoint, and the common memory and archive-extension failures
- Restore ordering and validating a restore: version, error log, cron execution, test send
- Rehearsing an update on a staging clone, including cron suspension and the site URL change
- Backup scheduling, retention and offsite storage as engagement policy

### Official Reference Links
- [How to Update Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_update_mautic.html)
- [Troubleshooting](https://docs.mautic.org/en/6.0/troubleshooting/troubleshooting.html)
- [Installing Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_install_mautic.html)
- [Switching to Composer](https://docs.mautic.org/en/6.0/getting_started/switching_composer.html)
- [Cron Jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [How to set up a staging server to test new Mautic releases](https://kb.mautic.org/article/how-to-set-up-a-staging-server-to-test-new-mautic-releases.html)
- [mysqldump](https://dev.mysql.com/doc/refman/8.0/en/mysqldump.html)

## Module 12: Deployment and Preparing Mautic for Production

### Learning Objectives
- Design a repeatable deployment for a Composer-managed Mautic instance
- Apply the correct post-deployment command sequence
- Configure environments and secrets for production
- Apply the documented production readiness settings
- Recognise which production concerns Mautic does not document and plan for them explicitly

### Context
Deployment is where installation and configuration meet, and Mautic publishes no deployment guide, so the integrator assembles one from the Composer contract, the update procedure and general Symfony deployment practice. An instance that works in a demo will not necessarily survive a segment of half a million contacts.

### Key Topics
- Hosting posture: dedicated or virtual private server, resource sizing, and why shared hosting fails
- The web root contract as the one explicit web server instruction Mautic publishes
- Deployment models: package upload, Composer build, and build-and-release pipelines
- Which files carry environment-specific settings, and why secrets never belong in shared files
- Environment separation, environment file precedence, and production compilation of environment files
- Configuration that changes per environment, starting with site URL
- Handling media, uploads and generated assets across releases
- Scaffolded files and preserving local customisation of them
- Pausing cron and queue workers during a release, and resuming them after
- The post-deployment command block: cache clear, update finish, migrations, cache clear
- Generating production assets and re-applying ownership and permissions
- Verification: dashboard version, schema check endpoint, error log, test email, a campaign event firing
- Rollback: restoring the manifest and lock file, restoring the database, reverting the web root
- Documented scale mechanisms: queueing, webhook queue mode, campaign summary statistics, background imports, parallel broadcast ranges, segment pruning
- Housekeeping commands for production, log locations and log file retention settings

### Official Reference Links
- [How to Update Mautic](https://docs.mautic.org/en/6.0/getting_started/how_to_update_mautic.html)
- [Switching to Composer](https://docs.mautic.org/en/6.0/getting_started/switching_composer.html)
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Command Line Interface](https://docs.mautic.org/en/6.0/configuration/command_line_interface.html)
- [Cron Jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [File Ownership and Permissions](https://docs.mautic.org/en/6.0/troubleshooting/file_ownership_permissions.html)
- [Working with Resource Limits](https://docs.mautic.org/en/6.0/troubleshooting/working_with_resource_limits.html)
- [Development Environments](https://devdocs.mautic.org/en/6.0/development-environment/environments.html)
- [Mautic Requirements](https://mautic.org/mautic-requirements/)
- [How to Deploy a Symfony Application](https://symfony.com/doc/current/deployment.html)
- [Symfony Performance](https://symfony.com/doc/current/performance.html)

## Module 13: Secure Setup and Maintenance

### Learning Objectives
- Apply correct file ownership and permissions as a security control
- Harden the documented configuration surface, including CORS, trusted hosts, cookies, security headers, API exposure and upload restrictions
- Configure SAML single sign-on correctly, including the default role for provisioned users
- Follow Mautic's vulnerability disclosure policy
- Determine whether a given instance is still receiving security advisories
- Apply GDPR and CCPA data lifecycle controls

### Context
Mautic stores personal data and sends mail on a client's behalf, which makes it an attractive target. This module covers the security controls Mautic actually exposes, and is explicit about the substantial hardening guidance Mautic does not publish.

### Key Topics
- Security-relevant shipped defaults: cookie flags, security headers off by default, CORS restriction, API disabled, form upload extension blacklist, empty trusted hosts
- Cookie security derived from whether the site URL uses HTTPS
- File ownership and permissions framed as a security control
- Asset storage outside the public web root
- Complex password requirements and role design following least privilege
- SAML single sign-on: metadata upload, entity ID, service provider metadata and assertion consumer service URLs
- The recommendation to use a non-admin default role, and the consequence of leaving it empty
- Direct login availability when single sign-on is enabled
- Vulnerability disclosure: private reporting only, coordinated disclosure, and what is in and out of scope
- The security advisory window and why version currency is itself a security control
- Out-of-sequence release notice period
- Data lifecycle: GDPR retention purge, CCPA do-not-sell pair, IP anonymisation and do-not-track lists
- Install-time hardening: complex password, disabling table backup on a new install, restricting CORS domains, and confirming the instance is served over HTTPS
- Ongoing maintenance: patch cadence, credential rotation, access review

### Official Reference Links
- [File Ownership and Permissions](https://docs.mautic.org/en/6.0/troubleshooting/file_ownership_permissions.html)
- [Authentication](https://docs.mautic.org/en/6.0/authentication/authentication.html)
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Cron Jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [Mautic Security Policy](https://github.com/mautic/mautic/blob/6.x/SECURITY.md)
- [Mautic Security](https://mautic.org/security)
- [Mautic Releases](https://mautic.org/releases/)

## Module 14: Themes, Email Templating, MJML, CSS and JavaScript

### Learning Objectives
- Build, package and install a Mautic theme that passes validation
- Read and write a theme configuration file, declaring builders and features correctly
- Author an MJML email theme and know which MJML components Mautic processes
- Use Mautic's token syntax accurately, including fallbacks and date formatting
- Style and embed forms, and choose the correct embed method for progressive profiling
- Use the tracking script and the documented JavaScript callbacks

### Context
Themes and templates are how a client's brand reaches emails, landing pages and embedded forms, and email is the most constrained frontend environment in common use. Mautic's theme documentation is split between the user documentation and older developer documentation, and several pages are empty, so knowing where each fact lives is part of the competency.

### Key Topics
- Theme package structure: assets, template directory, configuration file, thumbnail
- The theme configuration file: name, author, builder declaration and feature declaration
- Declaring one or multiple builders, valid builder values, and valid feature values
- Packaging rules: thumbnail dimensions, zipping contents rather than the folder, configuration file at the zip root
- Installing, previewing, hiding, downloading and deleting themes; default theme selection for pages and emails
- Risks of changing a theme after content has been built
- MJML: what it solves, document structure, core body components, head components, and the documented processing limits
- Where MJML lives in a theme and the compiled HTML counterpart that must accompany it
- Bundled MJML themes and the builder they require
- Builder options: visual builder, legacy builder and code mode, and code mode's preview limitation
- Enabling and disabling builders and clearing cache afterwards
- Token syntax: contact fields with fallbacks, URL encoding and date formats; system and component tokens
- Tracking pixel placement and explicit repositioning; custom builder fonts
- CSS fundamentals and Mautic's styling controls: theme style toggle, theme form support, per-field attribute inputs, render style
- Overriding form templates and styles from within a theme
- The three form embed methods, their trade-offs, and why progressive profiling requires an embedded method
- The submission lookback limit for auto-fill and progressive profiling
- The tracking script: global object, loader file and pageview call
- Form callbacks registered against a form's API name, the callback list, and generated field element naming
- CMS shortcodes for embedding forms

### Official Reference Links
- [Creating Themes](https://docs.mautic.org/en/6.0/builders/creating_themes.html)
- [Email and Landing Page Builders](https://docs.mautic.org/en/6.0/builders/email_landing_page.html)
- [Managing Themes](https://docs.mautic.org/en/6.0/themes/manage_themes.html)
- [Code Mode](https://docs.mautic.org/en/6.0/themes/code_mode.html)
- [Emails](https://docs.mautic.org/en/6.0/channels/emails.html)
- [Forms](https://docs.mautic.org/en/6.0/components/forms.html)
- [Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html)
- [Tracking Script](https://docs.mautic.org/en/6.0/configuration/tracking_script.html)
- [Tokens and Variables](https://docs.mautic.org/en/6.0/configuration/variables.html)
- [Theme Directory Structure](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)
- [GrapesJS Builder](https://devdocs.mautic.org/en/5.x/themes/grapesjs.html)
- [Theme Forms](https://devdocs.mautic.org/en/5.x/themes/forms.html)
- [MauticJS API](https://devdocs.mautic.org/en/5.x/mauticjs_api/tracking_script.html)
- [Form Hooks](https://devdocs.mautic.org/en/5.x/form_hooks/getting_started.html)
- [MJML Documentation](https://documentation.mjml.io/)
- [Twig Documentation](https://twig.symfony.com/doc/3.x/)
- [MDN CSS Documentation](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [MDN: Dynamic scripting with JavaScript](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting)

## Module 15: Email Infrastructure, Service Providers and Deliverability

### Learning Objectives
- Configure an email transport using a Symfony Mailer connection string
- Install and configure an API-based transport and understand its trade-offs
- Choose between immediate and queued delivery and configure the queue
- Configure bounce and unsubscribe handling
- Apply domain authentication and bulk sender requirements
- Diagnose email that is queued, pending or not sending

### Context
Mautic ships with SMTP only, so every other transport is a dependency the integrator adds, and the choice determines send throughput and whether bounce handling is even possible. Deliverability is where a Mautic implementation is ultimately judged, and authentication and unsubscribe compliance are now enforced requirements rather than best practice.

### Key Topics
- Symfony Mailer as the transport layer since Mautic 5, configured through a connection string
- Connection string anatomy, the documented ports for SSL and TLS, and the port to avoid
- Encoding rules when writing a connection string directly into configuration, and the environment variable override
- Installing an API transport as a Composer dependency
- The two documented limitations of generic transports: no batch sending, and no transport callback handling for bounces
- Send settings: from name and address, reply-to, custom return path, address length limit, mailer is owner
- Immediate versus queued delivery, and the default queue state
- Bounce and unsubscribe handling: monitored inbox folders and their defaults, and the fetch command
- Plus-addressing requirements on the return path, and the list-unsubscribe header
- Which providers support webhook callbacks for bounce management, and the consequence of using a stock transport instead
- Provider selection criteria: volume, cost, reputation, regional presence
- Domain authentication: SPF policy records, DKIM key publication and signing, DMARC policy progression and reporting
- Bulk sender requirements and one-click unsubscribe compliance, and the Mautic versions that introduced it
- Complaint rate thresholds, list hygiene and bounce suppression
- Monitoring reputation with provider postmaster tooling; warming a new domain or IP
- Diagnosis: test send behaviour, pending versus sent, frequency-rule queueing, single send per email per contact, and bot filtering parameters

### Official Reference Links
- [Configuration Settings](https://docs.mautic.org/en/6.0/configuration/settings.html)
- [Emails](https://docs.mautic.org/en/6.0/channels/emails.html)
- [Cron Jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [Command Line Interface](https://docs.mautic.org/en/6.0/configuration/command_line_interface.html)
- [Mautic email configuration defaults](https://github.com/mautic/mautic/blob/6.x/app/bundles/EmailBundle/Config/config.php)
- [Navigating Gmail and Yahoo's spam policies](https://mautic.org/blog/navigating-gmail-and-yahoos-new-spam-policies-what-mautic-users-need-know/)
- [Email sending doesn't work — 10 things to check](https://kb.mautic.org/article/email-sending-doesn-039%3Bt-work-here-are-10-things-to-check.html)
- [Symfony Mailer](https://symfony.com/doc/current/mailer.html)
- [Amazon SES Developer Guide](https://docs.aws.amazon.com/ses/latest/dg/Welcome.html)
- [Email sender guidelines](https://support.google.com/a/answer/81126)
- [Google Postmaster Tools](https://support.google.com/mail/answer/9981691)
- [RFC 7208 — Sender Policy Framework](https://www.rfc-editor.org/rfc/rfc7208.html)
- [RFC 6376 — DomainKeys Identified Mail](https://www.rfc-editor.org/rfc/rfc6376.html)
- [RFC 7489 — DMARC](https://www.rfc-editor.org/rfc/rfc7489.html)
- [RFC 8058 — One-Click Unsubscribe](https://www.rfc-editor.org/rfc/rfc8058.html)

## Module 16: Integrations — Plugins, Webhooks and the REST API

### Learning Objectives
- Enable and manage plugins, and test an integration three different ways
- Configure the major documented CRM and service integrations
- Design and secure a webhook consumer, including signature verification
- Enable the REST API and authenticate with Basic Auth or OAuth2
- Use the core REST endpoints for contacts, segments, campaigns, emails and forms
- Choose the right integration mechanism for a given requirement

### Context
Mautic is rarely the only system in a client's stack, and an integrator's core value is knowing which of Mautic's integration surfaces fits a requirement and what each costs to operate. Mautic's plugin documentation is uneven, so knowing which integrations are documented and which are not is itself part of the judgement.

### Key Topics
- Comparing the mechanisms: plugin, webhook push, API pull or push, and an automation platform on top
- Where plugins live in the interface, enabling defaults, and reloading plugins from the command line
- Plugins as Symfony bundles, their install path and namespace convention, and the install and update lifecycle events
- The three documented ways to test an integration: campaign action, form action, points trigger
- Contact field mapping principles and mapping only what is synced
- Documented integrations: S3 asset storage, contact enrichment, HubSpot, MailChimp, Zoho CRM, Salesforce via the Knowledgebase, Twilio, social login, WordPress
- Integration authentication patterns: API key, OAuth2 authorization code, data centre selection
- Push, pull and bidirectional synchronisation; scheduling integration commands and naming the integration explicitly
- Identity handling: unique identifiers, deduplication, and placeholder values for missing required fields
- Activity synchronisation and its volume implications
- Webhook configuration, queue mode, event ordering, and processing queued webhooks on a schedule
- Webhook payload structure keyed by event type, and event grouping under batching
- Signature verification over the raw request body, and the test payload button
- Available webhook events, retrieving the list at runtime, and the webhook limit, timeout and log retention settings
- REST API disabled by default, enabling it, the base endpoint and the version response header
- Basic Auth versus OAuth2, credential creation, the authorization code and client credentials flows, bearer tokens and token lifetimes
- Core endpoints for contacts including batch operations, do-not-contact, points and activity
- Partial update versus update-or-create semantics; list parameters, pagination, ordering and minimal responses
- Batch limits, rate limiter configuration and documented error response shapes
- The official API client library and its dependencies
- Evaluating a Marketplace plugin before installing it for a client

### Official Reference Links
- [Plugin Resources](https://docs.mautic.org/en/6.0/plugins/plugin_resources.html)
- [Amazon S3 Plugin](https://docs.mautic.org/en/6.0/plugins/amazon.html)
- [Clearbit Plugin](https://docs.mautic.org/en/6.0/plugins/clearbit.html)
- [HubSpot Plugin](https://docs.mautic.org/en/6.0/plugins/hubspot.html)
- [MailChimp Plugin](https://docs.mautic.org/en/6.0/plugins/mailchimp.html)
- [Zoho CRM Plugin](https://docs.mautic.org/en/6.0/plugins/zoho_crm.html)
- [Twilio Plugin](https://docs.mautic.org/en/6.0/plugins/twilio.html)
- [Social Login Plugin](https://docs.mautic.org/en/6.0/plugins/social_login.html)
- [WordPress Plugin](https://docs.mautic.org/en/6.0/plugins/wordpress.html)
- [How to integrate Mautic with Salesforce](https://kb.mautic.org/article/how-to-integrate-mautic-with-salesforce.html)
- [Integrations Framework](https://devdocs.mautic.org/en/6.0/plugin_integrations/integrations.html)
- [Plugin Installation and Lifecycle](https://devdocs.mautic.org/en/6.0/plugins/installation.html)
- [Webhooks Getting Started](https://devdocs.mautic.org/en/6.0/webhooks/getting_started.html)
- [Webhook Example Scripts](https://devdocs.mautic.org/en/6.0/webhooks/example_scripts.html)
- [Webhook Events](https://devdocs.mautic.org/en/6.0/webhooks/events/index.html)
- [Webhooks API](https://devdocs.mautic.org/en/6.0/rest_api/webhooks.html)
- [REST API Getting Started](https://devdocs.mautic.org/en/6.0/rest_api/getting_started.html)
- [API Authentication](https://devdocs.mautic.org/en/6.0/rest_api/authentication.html)
- [Contacts API](https://devdocs.mautic.org/en/6.0/rest_api/contacts.html)
- [Segments API](https://devdocs.mautic.org/en/6.0/rest_api/segments.html)
- [Campaigns API](https://devdocs.mautic.org/en/6.0/rest_api/campaigns.html)
- [Emails API](https://devdocs.mautic.org/en/6.0/rest_api/emails.html)
- [Forms API](https://devdocs.mautic.org/en/6.0/rest_api/forms.html)
- [Mautic API Library](https://github.com/mautic/api-library)
- [Integrations and API](https://mautic.org/features/integrations-and-api/)
- [Postman Documentation](https://learning.postman.com/docs/introduction/overview/)
- [n8n Mautic Node](https://docs.n8n.io/integrations/builtin/app-nodes/n8n-nodes-base.mautic/)

---

## Certification Requirements

To earn the Certified Mautic Integrator certification, candidates must:

1. Complete all 16 modules
2. Pass the certification exam with a score of 80% or higher
3. Pay the examination entry fee
4. Verify identity via the online examination platform

## Exam Details

- **Total Questions**: 75
- **Duration**: 90 minutes
- **Passing Score**: 80%
- **Question Format**: four options each, with a small proportion of multiple-response questions

## Continuing Education

Certified integrators are encouraged to:
- Stay active in the Mautic community
- Contribute to the Mautic project
- Maintain knowledge of new versions, release cycles and security advisories
