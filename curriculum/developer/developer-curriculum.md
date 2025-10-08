# Certified Mautic Developer Curriculum

## Course Overview

This comprehensive curriculum is designed to train developers to become certified Mautic experts, covering everything from basic setup to advanced plugin development and API integration.

## Prerequisites

- Basic PHP knowledge (OOP concepts, Symfony framework familiarity preferred)
- Understanding of web development (HTML, CSS, JavaScript)
- Database concepts (MySQL/MariaDB)
- Command line interface experience
- Git version control basics
- Familiarity with Codeception unit testing framework

## Module 1: Prerequisites for Mautic

### Learning Objectives
- Understand system requirements for Mautic
- Identify necessary server configurations
- Learn about PHP, database, and web server requirements

### Context
Before diving into Mautic development, it's crucial to understand the technical prerequisites and system requirements. This module covers the foundation needed to run Mautic effectively in development and production environments.

### Key Topics
- PHP version requirements (8.1+)
- Database requirements (MySQL 5.7+/MariaDB 10.2+)
- Web server configuration (Apache/Nginx)
- PHP extensions and configurations
- Memory and performance requirements
- Security considerations

### Official Reference Links
- [Installation Requirements](https://devdocs.mautic.org/en/5.x/development-environment/getting_started.html)
- [Mautic Official Website](https://mautic.org)

## Module 2: Setup and Installation using DDEV

### Learning Objectives
- Set up a local development environment using DDEV
- Configure Mautic for development
- Understand the benefits of containerized development

### Context
DDEV provides a standardized, containerized development environment that ensures consistency across different development setups. This module teaches how to leverage DDEV for efficient Mautic development.

### Key Topics
- DDEV installation and configuration
- Creating a Mautic project with DDEV
- Database setup and management
- Environment configuration
- Debugging setup with DDEV
- Profiling code performance with Xhprof, Blackfire or Xdebug
- Performance optimization in development
- Unit testing setup in Mautic

### Official Reference Links
- [DDEV Installation Guide](https://ddev.readthedocs.io)
- [Local Development Setup](https://devdocs.mautic.org/en/5.x/development-environment/environments.html)

## Module 3: Mautic Platform Walkthrough

### Learning Objectives
- Navigate the Mautic user interface
- Understand core Mautic concepts and terminology
- Identify key features and functionalities

### Context
Understanding the Mautic platform from a user perspective is essential for developers. This module provides a comprehensive overview of the platform's capabilities and structure.

### Key Topics
- Dashboard and navigation
- Contacts and segments
- Campaigns and email marketing
- Landing pages and forms
- Reports and analytics
- Configuration and settings
- User management and permissions

### Official Reference Links
- [Getting Started](https://docs.mautic.org/en/5.x/getting_started/index.html)
- [User Interface Guide](https://docs.mautic.org/en/5.x/contacts/index.html)
- [Managing Contacts](https://docs.mautic.org/en/5.x/contacts/manage_contacts.html)

## Module 4: Configuring and Extending Mautic

### Learning Objectives
- Configure Mautic for different environments
- Understand configuration management
- Learn about extending Mautic's functionality

### Context
Proper configuration is crucial for Mautic's performance and functionality. This module covers how to configure Mautic for various use cases and how to extend its capabilities.

### Key Topics
- Configuration file structure
- Environment-specific configurations
- Email configuration and sending
- Integration configurations
- Performance and caching settings
- Security configurations
- Multi-tenancy considerations
- Familiarity with production environment configuration

### Official Reference Links
- [Configuration Settings](https://docs.mautic.org/en/5.x/configuration/settings.html)
- [Email Configuration](https://docs.mautic.org/en/5.x/configuration/settings.html#email-settings)
- [System Configuration](https://docs.mautic.org/en/5.x/configuration/index.html)

## Module 5: Developing with Mautic

### Learning Objectives
- Understand Mautic's architecture and coding standards
- Learn about the Symfony framework integration
- Develop custom functionality within Mautic

### Context
Mautic is built on the Symfony framework, which provides a robust foundation for development. This module introduces developers to Mautic's specific development patterns and best practices.

### Key Topics
- Mautic architecture overview
- Symfony framework integration
- Bundle structure and organization
- Service container and dependency injection
- Event system and hooks
- Form handling and validation
- Security and authentication
- Translations
- Integration with Third-Party authentication systems for fetching data from other services
- Configurations for Bundle
- Familiarity with IntegrationsBundle to add new integrations

### Official Reference Links
- [Developer Documentation Overview](https://devdocs.mautic.org/en/5.x/)
- [Plugin Development Guide](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [Mautic vs Symfony](https://devdocs.mautic.org/en/5.x/plugins/mautic_vs_symfony.html)
- [Integrations](https://devdocs.mautic.org/en/5.x/components/integrations.html)

## Module 6: Setting Up a Debugging Environment

### Learning Objectives
- Configure development debugging tools
- Implement logging and monitoring
- Set up performance profiling

### Context
A proper debugging environment is essential for efficient development and troubleshooting. This module should be completed early in the learning path to ensure developers have the right tools before tackling coding tasks.

### Key Topics
- IDE debugging configuration (PHPStorm, VS Code)
- Xdebug setup and configuration
- Logging setup and management
- Performance profiling tools (Xhprof, Blackfire)
- Error tracking and monitoring
- Database query debugging
- Frontend debugging (browser dev tools)
- Remote debugging techniques

### Official Reference Links
- [Development Environment](https://devdocs.mautic.org/en/5.x/development-environment/environments.html)
- [Troubleshooting](https://docs.mautic.org/en/5.x/troubleshooting/index.html)
- [Log Management](https://docs.mautic.org/en/5.x/troubleshooting/monitoring.html)

## Module 7: Mautic Security Best Practices

### Learning Objectives
- Implement security best practices in Mautic development
- Understand common security vulnerabilities and prevention
- Secure API endpoints and data handling

### Context
Security is paramount in any application handling customer data. This module covers essential security practices that developers must understand and implement when working with Mautic.

### Key Topics
- Data sanitization and validation
- Preventing XSS (Cross-Site Scripting) attacks
- CSRF (Cross-Site Request Forgery) protection
- SQL injection prevention
- Permissions and role management
- Secure API practices and authentication
- Protecting sensitive configuration data
- Password hashing and storage
- Secure file uploads and handling
- HTTPS and SSL/TLS configuration
- Security headers and configurations

### Official Reference Links
- [Security Best Practices](https://docs.mautic.org/en/5.x/security/index.html)
- [Configuration Security](https://docs.mautic.org/en/5.x/configuration/settings.html)
- [API Security](https://docs.mautic.org/en/5.x/rest_api/authentication.html)

## Module 8: Mautic's API Overview

### Learning Objectives
- Understand Mautic's API architecture
- Learn about authentication methods
- Explore available API endpoints

### Context
Mautic's API is a powerful tool for integrating with external systems and automating tasks. This module provides an overview of the API's capabilities and structure.

### Key Topics
- REST API fundamentals
- Authentication methods (OAuth, Basic Auth)
- API rate limiting and best practices
- Available endpoints overview
- Response formats and error handling
- API versioning and compatibility

### Official Reference Links
- [API Configuration](https://docs.mautic.org/en/5.x/configuration/settings.html#api-settings)
- [API Documentation](https://devdocs.mautic.org/en/5.x/components/api.html)
- [REST API Reference](https://docs.mautic.org/en/5.x/rest_api/index.html)

## Module 9: Working with Mautic's REST API

### Learning Objectives
- Implement API authentication
- Perform CRUD operations via API
- Handle API responses and errors

### Context
Practical implementation of Mautic's REST API is essential for integrations and custom applications. This module provides hands-on experience with API operations.

### Key Topics
- Setting up API credentials
- Making authenticated requests
- Contact management via API
- Campaign and email operations
- Asset and form management
- Batch operations and bulk updates
- Error handling and debugging

### Official Reference Links
- [REST API Documentation](https://docs.mautic.org/en/5.x/rest_api/index.html)
- [Authentication Guide](https://docs.mautic.org/en/5.x/rest_api/authentication.html)
- [GitHub Examples](https://github.com/mautic/api-library)

## Module 10: Building Custom API Endpoints

### Learning Objectives
- Create custom API endpoints
- Implement proper authentication and authorization
- Design RESTful API interfaces

### Context
Sometimes the standard API endpoints aren't sufficient for specific use cases. This module teaches how to create custom API endpoints that integrate seamlessly with Mautic's existing API structure.

### Key Topics
- Controller development for APIs
- Route configuration
- Request validation and serialization
- Response formatting
- Authentication integration
- API documentation and testing
- Performance considerations

### Official Reference Links
- [API Development](https://devdocs.mautic.org/en/5.x/components/api.html)
- [Plugin Development](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [GitHub Repository](https://github.com/mautic/mautic)

## Module 11: Introduction to Mautic Plugins

### Learning Objectives
- Explore existing plugins and their functionality
- Understand plugin installation and management
- Learn about plugin marketplace and distribution

### Context
Before creating plugins, it's important to understand the existing plugin ecosystem and how plugins integrate with Mautic's core functionality. This foundational knowledge is essential before diving into plugin development.

### Key Topics
- Plugin marketplace overview
- Installation and activation
- Plugin configuration
- Common plugin patterns
- Plugin dependencies
- Version compatibility
- Community plugins vs. commercial plugins

### Official Reference Links
- [Plugin Documentation](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [Mautic Marketplace](https://docs.mautic.org/en/5.x/marketplace/marketplace.html)
- [Plugin Resources](https://docs.mautic.org/en/5.x/plugins/plugin_resources.html)

## Module 12: Plugin Development

### Learning Objectives
- Understand Mautic's plugin architecture
- Create and structure plugins
- Implement plugin lifecycle management

### Context
Plugins are the primary way to extend Mautic's functionality. This module covers the fundamentals of plugin development and architecture.

### Key Topics
- Plugin architecture and structure
- Plugin lifecycle and events
- Configuration and settings
- Database integration
- User interface integration
- Security considerations
- Distribution and packaging
- Authentication with third party systems

### Official Reference Links
- [Plugin Development](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [Plugin Marketplace](https://docs.mautic.org/en/5.x/marketplace/marketplace.html)
- [Plugin Structure](https://devdocs.mautic.org/en/5.x/plugins/structure.html)

## Module 13: Setting Up a Plugin Development Environment

### Learning Objectives
- Configure development environment for plugin development
- Set up debugging and testing tools
- Implement version control for plugins

### Context
A proper development environment is crucial for efficient plugin development. This module covers the tools and configurations needed for professional plugin development.

### Key Topics
- Development environment setup
- IDE configuration and debugging
- Version control best practices
- Testing framework setup
- Continuous integration
- Documentation tools
- Package management

### Official Reference Links
- [Development Environment](https://devdocs.mautic.org/en/5.x/development-environment/environments.html)
- [Plugin Dependencies](https://devdocs.mautic.org/en/5.x/plugins/dependencies.html)
- [Continuous Integration](https://devdocs.mautic.org/en/5.x/plugins/continuous-integration.html)

## Module 14: Creating Your First Mautic Plugin

### Learning Objectives
- Create a basic plugin from scratch
- Implement core plugin functionality
- Test and debug plugin functionality

### Context
This hands-on module walks through creating a complete plugin, from initial structure to working functionality, providing practical experience with the development process.

### Key Topics
- Plugin scaffolding and structure
- Configuration files and metadata
- Basic functionality implementation
- Event handling and hooks
- User interface integration
- Testing and validation
- Installation and activation
- Console commands for the plugin
- Familiarity with DTO (Data Transfer Objects) pattern

### Official Reference Links
- [Plugin Getting Started](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [Plugin Structure](https://devdocs.mautic.org/en/5.x/plugins/structure.html)
- [Plugin Config](https://devdocs.mautic.org/en/5.x/plugins/config.html)

## Module 15: Handling Plugin Updates and Maintenance

### Learning Objectives
- Implement plugin versioning and updates
- Handle database migrations
- Manage plugin lifecycle events

### Context
Long-term plugin maintenance requires proper update mechanisms and lifecycle management. This module covers strategies for maintaining plugins over time.

### Key Topics
- Version management and semantic versioning
- Database schema updates
- Configuration migrations
- Backward compatibility
- Update notifications and processes
- Error handling during updates
- Rollback strategies

### Official Reference Links
- [Plugin Migration 4 to 5](https://devdocs.mautic.org/en/5.x/plugins/from-4-to-5.html)
- [Marketplace Best Practices](https://devdocs.mautic.org/en/5.x/marketplace/best_practices.html)
- [Plugin Installation](https://devdocs.mautic.org/en/5.x/plugins/installation.html)

## Module 16: Mautic Continuous Integration and Code Quality

### Learning Objectives
- Understand Mautic's CI/CD pipeline
- Implement code quality tools
- Ensure code standards compliance

### Context
Maintaining code quality is essential for contributing to Mautic or developing professional plugins. This module covers the tools and practices used in Mautic's development workflow.

### Key Topics
- PHPStan for static analysis
- PHP CS Fixer for code style
- Rector for automated refactoring
- PHPUnit for testing
- GitHub Actions and CI pipelines
- Code coverage analysis
- Pre-commit hooks
- Automated code reviews
- Quality gates and standards

### Official Reference Links
- [Continuous Integration](https://devdocs.mautic.org/en/5.x/plugins/continuous-integration.html)
- [Code Standards](https://devdocs.mautic.org/en/5.x/plugins/code_standards.html)
- [Testing Guide](https://devdocs.mautic.org/en/5.x/plugins/testing.html)

## Module 17: Mautic Contribution Guide

### Learning Objectives
- Understand the contribution process
- Learn best practices for contributing
- Navigate the Mautic community

### Context
Contributing to Mautic benefits the entire community and helps developers grow their skills. This module covers how to effectively contribute to the Mautic project.

### Key Topics
- Contribution workflow and guidelines
- Fork, branch, and pull request process
- Issue tracking and bug reporting
- Feature proposal process
- Documentation contributions
- Code review process
- Community communication channels
- Contributor License Agreement (CLA)
- Recognition and credits

### Official Reference Links
- [Contributing to Mautic](https://github.com/mautic/mautic/blob/5.x/.github/CONTRIBUTING.md)
- [Mautic Community](https://www.mautic.org/community)
- [GitHub Repository](https://github.com/mautic/mautic)

## Module 18: Customizing the User Interface

### Learning Objectives
- Modify Mautic's user interface
- Implement custom UI components
- Integrate with Mautic's design system

### Context
User interface customization allows developers to create tailored experiences within Mautic. This module covers techniques for modifying and extending the UI.

### Key Topics
- UI architecture and components
- Theme customization
- Custom form elements
- Dashboard widgets
- Menu and navigation customization
- Responsive design considerations
- Accessibility requirements

### Official Reference Links
- [Themes Getting Started](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)
- [Theme Forms](https://devdocs.mautic.org/en/5.x/themes/forms.html)
- [Design Permissions](https://devdocs.mautic.org/en/5.x/design/displaying_elements_based_on_user_permissions.html)

## Module 19: Mautic's Twig Templating Engine

### Learning Objectives
- Master Twig templating in Mautic
- Create custom templates and layouts
- Implement template inheritance and blocks

### Context
Twig is the templating engine used throughout Mautic for rendering views and emails. Understanding Twig is essential for customizing the user interface and email templates.

### Key Topics
- Twig syntax and fundamentals
- Template inheritance and blocks
- Custom Twig functions and filters
- Template debugging
- Performance optimization
- Security considerations
- Integration with Mautic's data
- Translations and pluralization

### Official Reference Links
- [Themes Getting Started](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)
- [Twig Documentation](https://twig.symfony.com)
- [Theme System](https://devdocs.mautic.org/en/5.x/themes/system.html)

## Module 20: Customizing Landing Page Templates

### Learning Objectives
- Develop responsive landing page templates
- Implement template variables and personalization
- Optimize landing pages for conversion

### Context
Landing pages are critical for lead generation and conversion. This module focuses specifically on creating effective landing page templates.

### Key Topics
- Landing page template structure
- Responsive design for landing pages
- Form integration in templates
- Template variables and tokens
- Personalization techniques
- A/B testing setup
- Performance optimization
- SEO considerations

### Official Reference Links
- [Themes Getting Started](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)
- [Landing Pages](https://docs.mautic.org/en/5.x/channels/landing_pages.html)
- [Theme System](https://devdocs.mautic.org/en/5.x/themes/system.html)

## Module 21: Email Template Development with MJML

### Learning Objectives
- Master MJML for email development
- Create responsive email templates
- Implement dynamic content and personalization

### Context
MJML is a powerful framework for creating responsive emails. This dedicated module covers email template development in depth, including MJML usage.

### Key Topics
- Introduction to MJML framework
- MJML syntax and components
- Converting MJML to HTML
- Responsive email design principles
- Email client compatibility
- Dynamic content integration
- Personalization tokens and variables
- Email deliverability optimization
- Testing across email clients
- Inline CSS and styling
- Dark mode support

### Official Reference Links
- [Email Templates](https://docs.mautic.org/en/5.x/channels/emails.html)
- [GrapesJS Builder](https://devdocs.mautic.org/en/5.x/themes/grapesjs.html)
- [MJML Documentation](https://mjml.io/documentation/)
- [Themes Getting Started](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)

## Module 22: Adding Custom JavaScript and CSS

### Learning Objectives
- Integrate custom JavaScript and CSS
- Implement frontend build processes
- Optimize performance and loading

### Context
Custom JavaScript and CSS allow for enhanced user experiences and specialized functionality. This module covers best practices for frontend development in Mautic.

### Key Topics
- Asset management and organization
- JavaScript event handling
- CSS preprocessing and optimization
- Build tools and workflows
- Performance considerations
- Security and XSS prevention
- Third-party library integration

### Official Reference Links
- [Themes Getting Started](https://devdocs.mautic.org/en/5.x/themes/getting_started.html)
- [Theme System](https://devdocs.mautic.org/en/5.x/themes/system.html)
- [Frontend Assets](https://docs.mautic.org/en/5.x/configuration/settings.html)

## Module 23: Database and Entities

### Learning Objectives
- Understand Mautic's database architecture
- Work with entity relationships
- Implement database best practices

### Context
Database knowledge is fundamental for Mautic development. This module covers the database structure and how to work with it effectively.

### Key Topics
- Database schema overview
- Entity relationships and associations
- Query optimization
- Indexing strategies
- Data integrity and constraints
- Performance monitoring
- Backup and recovery considerations

### Official Reference Links
- [Plugin Data](https://devdocs.mautic.org/en/5.x/plugins/data.html)
- [Components Database](https://devdocs.mautic.org/en/5.x/components/database.html)
- [Installation Database](https://docs.mautic.org/en/5.x/getting_started/requirements.html)

## Module 24: Understanding Mautic's Database Schema

### Learning Objectives
- Navigate Mautic's database structure
- Understand key tables and relationships
- Implement proper database queries

### Context
A deep understanding of Mautic's database schema is essential for effective development and troubleshooting. This module provides a comprehensive overview of the database structure.

### Key Topics
- Core entity tables
- Relationship mappings
- Audit and tracking tables
- Configuration and settings storage
- Queue and job tables
- Cache and session management
- Data archiving and cleanup

### Official Reference Links
- [Contact Management](https://docs.mautic.org/en/5.x/contacts/manage_contacts.html)
- [Plugin Data](https://devdocs.mautic.org/en/5.x/plugins/data.html)
- [Components Database](https://devdocs.mautic.org/en/5.x/components/database.html)

## Module 25: Working with Doctrine ORM in Mautic

### Learning Objectives
- Master Doctrine ORM concepts
- Implement entity mapping and relationships
- Optimize database queries

### Context
Doctrine ORM is the database abstraction layer used in Mautic. Understanding Doctrine is crucial for effective database operations and entity management.

### Key Topics
- Entity mapping and annotations
- Repository patterns
- Query builder and DQL
- Relationship management
- Lazy loading and performance
- Caching strategies
- Transaction management

### Official Reference Links
- [Plugin Data](https://devdocs.mautic.org/en/5.x/plugins/data.html)
- [Components Database](https://devdocs.mautic.org/en/5.x/components/database.html)
- [Doctrine Documentation](https://www.doctrine-project.org/projects/orm.html)

## Module 26: Creating Custom Entities

### Learning Objectives
- Design and implement custom entities
- Set up entity relationships
- Implement entity validation and constraints
- Extending Mautic's core entities

### Context
Custom entities allow developers to extend Mautic's data model for specific use cases. This module covers the complete process of creating and managing custom entities.

### Key Topics
- Entity design and planning
- Annotation and mapping configuration
- Repository implementation
- Form integration
- API integration
- Validation and constraints
- Performance considerations

### Official Reference Links
- [Plugin Data](https://devdocs.mautic.org/en/5.x/plugins/data.html)
- [Components Database](https://devdocs.mautic.org/en/5.x/components/database.html)
- [Plugin Structure](https://devdocs.mautic.org/en/5.x/plugins/structure.html)

## Module 27: Database Migrations and Schema Updates

### Learning Objectives
- Create and manage database migrations
- Handle schema updates safely
- Implement rollback strategies

### Context
Database migrations are essential for maintaining database schema consistency across environments. This module covers migration strategies and best practices.

### Key Topics
- Migration file structure and naming
- Schema modification techniques
- Data migration strategies
- Version control integration
- Rollback and recovery
- Testing migrations
- Production deployment considerations

### Official Reference Links
- [Plugin Data](https://devdocs.mautic.org/en/5.x/plugins/data.html)
- [Plugin Installation](https://devdocs.mautic.org/en/5.x/plugins/installation.html)
- [Components Database](https://devdocs.mautic.org/en/5.x/components/database.html)

## Module 28: Command Line Interface and Automation

### Learning Objectives
- Understand Mautic's CLI architecture
- Execute built-in commands
- Configure cron jobs and automation
- Create custom CLI commands

### Context
Mautic's CLI provides powerful tools for administration, maintenance, and automation. This consolidated module covers both using existing commands and creating custom ones.

### Key Topics
- CLI architecture and structure
- Built-in command overview
- Command structure and syntax
- Cron job configuration and scheduling
- Queue processing automation
- Email sending automation
- Cache management
- Database operations
- Creating custom CLI commands
- Command class structure
- Argument and option handling
- Input validation and output formatting
- Progress indicators
- Command registration and testing
- Debugging and logging

### Official Reference Links
- [Cron Jobs](https://docs.mautic.org/en/5.x/setup/cron_jobs.html)
- [Command Line](https://docs.mautic.org/en/5.x/configuration/command_line_interface.html)
- [Queue Processing](https://docs.mautic.org/en/5.x/queue/index.html)
- [Components Commands](https://devdocs.mautic.org/en/5.x/components/commands.html)

## Module 29: Event Listeners and Subscribers

### Learning Objectives
- Understand Mautic's event system
- Distinguish between listeners and subscribers
- Implement event-driven architecture

### Context
Mautic's event system provides a powerful way to extend functionality without modifying core code. This module covers the fundamentals of event-driven development.

### Key Topics
- Event system architecture
- Event listener vs. subscriber patterns
- Event priority and ordering
- Custom event creation
- Performance considerations
- Debugging events
- Best practices

### Official Reference Links
- [Event Listeners](https://devdocs.mautic.org/en/5.x/plugins/event_listeners.html)
- [Components Events](https://devdocs.mautic.org/en/5.x/components/events.html)
- [Plugin Structure](https://devdocs.mautic.org/en/5.x/plugins/structure.html)

## Module 30: Understanding Mautic Events

### Learning Objectives
- Identify available events in Mautic
- Understand event data and context
- Implement event handling strategies

### Context
Mautic dispatches numerous events throughout its operation. Understanding these events is crucial for creating responsive and integrated extensions.

### Key Topics
- Core event types and categories
- Event lifecycle and timing
- Event data and context
- Event documentation
- Event debugging tools
- Performance impact
- Security considerations

### Official Reference Links
- [Components Events](https://devdocs.mautic.org/en/5.x/components/events.html)
- [Webhook Events](https://devdocs.mautic.org/en/5.x/webhooks/events/index.html)
- [Event Listeners](https://devdocs.mautic.org/en/5.x/plugins/event_listeners.html)

## Module 31: Creating Event Listeners

### Learning Objectives
- Implement event listeners
- Handle event data and responses
- Manage listener lifecycle

### Context
Event listeners provide a simple way to respond to specific events in Mautic. This module covers the creation and management of event listeners.

### Key Topics
- Listener class structure
- Event subscription
- Event handling methods
- Response modification
- Error handling
- Listener registration
- Testing listeners

### Official Reference Links
- [Event Listeners](https://devdocs.mautic.org/en/5.x/plugins/event_listeners.html)
- [Components Events](https://devdocs.mautic.org/en/5.x/components/events.html)
- [Plugin Structure](https://devdocs.mautic.org/en/5.x/plugins/structure.html)

## Module 32: Using Event Subscribers

### Learning Objectives
- Implement event subscribers
- Handle multiple events in a single class
- Optimize subscriber performance

### Context
Event subscribers provide a more organized way to handle multiple related events. This module covers subscriber patterns and best practices.

### Key Topics
- Subscriber class structure
- Multiple event handling
- Event priority management
- Conditional event handling
- Subscriber registration
- Performance optimization
- Testing strategies

### Official Reference Links
- [Event Listeners](https://devdocs.mautic.org/en/5.x/plugins/event_listeners.html)
- [Components Events](https://devdocs.mautic.org/en/5.x/components/events.html)
- [Plugin Getting Started](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)

## Module 33: Email and Campaign Development

### Learning Objectives
- Develop custom email functionality
- Create advanced campaign logic
- Implement email tracking and analytics

### Context
Email and campaigns are core features of Mautic. This module covers advanced development techniques for creating sophisticated email and campaign functionality.

### Key Topics
- Email service architecture
- Campaign workflow development
- Email template engines
- Personalization and segmentation
- Delivery optimization
- Analytics and tracking
- A/B testing implementation

### Official Reference Links
- [Campaigns](https://docs.mautic.org/en/5.x/campaigns/index.html)
- [Email Channels](https://docs.mautic.org/en/5.x/channels/emails.html)
- [Components Campaigns](https://devdocs.mautic.org/en/5.x/components/campaigns.html)

## Module 34: Developing Campaign Logic

### Learning Objectives
- Create complex campaign workflows
- Implement conditional logic
- Optimize campaign performance

### Context
Advanced campaign development requires understanding of workflow logic and decision trees. This module covers creating sophisticated automated campaigns.

### Key Topics
- Campaign workflow architecture
- Decision node implementation
- Conditional logic and branching
- Timing and scheduling
- Performance optimization
- Testing and debugging
- Analytics integration

### Official Reference Links
- [Creating Campaigns](https://docs.mautic.org/en/5.x/campaigns/campaign_builder.html)
- [Campaign Events](https://docs.mautic.org/en/5.x/campaigns/campaign_events.html)
- [Components Campaigns](https://devdocs.mautic.org/en/5.x/components/campaigns.html)

## Module 35: Advanced Email and Campaign Customization

### Learning Objectives
- Implement advanced customization techniques
- Create custom campaign actions
- Develop sophisticated email features

### Context
This module covers advanced techniques for customizing email and campaign functionality beyond standard configuration options.

### Key Topics
- Custom campaign actions
- Advanced email features
- Integration with external services
- Custom tracking and analytics
- Advanced personalization
- Performance optimization
- Security considerations

### Official Reference Links
- [Components Campaigns](https://devdocs.mautic.org/en/5.x/components/campaigns.html)
- [Event Listeners](https://devdocs.mautic.org/en/5.x/plugins/event_listeners.html)
- [Email Configuration](https://docs.mautic.org/en/5.x/configuration/settings.html#email-settings)

## Module 36: Using and Extending Reports

### Learning Objectives
- Understand Mautic's reporting system
- Create custom reports
- Extend existing report functionality

### Context
Reports provide valuable insights into marketing performance. This module covers how to work with Mautic's reporting system and create custom reports for specific needs.

### Key Topics
- Report architecture and structure
- Built-in reports overview
- Creating custom report types
- Query building for reports
- Data aggregation and calculation
- Custom report widgets
- Exporting and scheduling reports
- Performance optimization for large datasets
- Report permissions and access control
- Integrating custom data sources

### Official Reference Links
- [Reports](https://docs.mautic.org/en/5.x/reports/index.html)
- [Components Reports](https://devdocs.mautic.org/en/5.x/components/reports.html)
- [Plugin Development](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)

## Module 37: Testing and Debugging

### Learning Objectives
- Set up comprehensive testing environments
- Implement debugging strategies
- Create automated test suites
- Distinguish between unit and functional tests

### Context
Testing and debugging are crucial for maintaining high-quality Mautic installations and custom development. This module covers tools and techniques for effective testing, including both unit and functional testing approaches.

### Key Topics
- Testing environment setup
- Debugging tools and techniques
- **Unit vs Functional testing concepts**
- **Unit testing with PHPUnit**
  - Testing individual classes and methods
  - Mocking dependencies
  - Isolated test cases
  - Fast execution
- **Functional testing with Symfony**
  - Testing complete workflows
  - Database interactions
  - API endpoint testing
  - Browser automation testing
- Integration testing
- Test data fixtures and factories
- Performance testing
- Security testing
- Continuous integration
- Code coverage analysis

### Official Reference Links
- [Development Environment](https://devdocs.mautic.org/en/5.x/development-environment/environments.html)
- [Continuous Integration](https://devdocs.mautic.org/en/5.x/plugins/continuous-integration.html)
- [Troubleshooting](https://docs.mautic.org/en/5.x/troubleshooting/index.html)

## Module 38: Testing Plugins

### Learning Objectives
- Implement comprehensive plugin testing strategies
- Create unit and functional tests for plugins
- Set up automated testing pipelines

### Context
Plugin testing requires specialized approaches to ensure functionality works correctly within the Mautic ecosystem. This module focuses specifically on testing plugin code.

### Key Topics
- Plugin testing environment setup
- Unit testing plugin components
  - Testing plugin services
  - Testing event listeners/subscribers
  - Testing custom entities
  - Mocking Mautic dependencies
- Functional testing plugin features
  - Testing complete plugin workflows
  - Testing UI components
  - Testing database operations
- Integration testing with Mautic core
- Test fixtures for plugin data
- Automated testing pipelines
- Test coverage for plugins
- Testing plugin updates and migrations
- Performance testing for plugins

### Official Reference Links
- [Continuous Integration](https://devdocs.mautic.org/en/5.x/plugins/continuous-integration.html)
- [Plugin Development](https://devdocs.mautic.org/en/5.x/plugins/getting_started.html)
- [Testing Best Practices](https://devdocs.mautic.org/en/5.x/plugins/testing.html)

---

## Certification Requirements

To earn the Certified Mautic Developer certification, candidates must:

1. Complete all 38 modules
2. Pass the certification exam with a score of 80% or higher
3. Submit a capstone project demonstrating proficiency
4. Show evidence of code contributions or plugin development

## Exam Details

- **Total Questions**: 100
- **Duration**: 120 minutes
- **Passing Score**: 80%
- **Question Distribution**:
  - Easy (Basic Configuration): 10%
  - Advanced Coding (Custom Modules): 30%
  - Advanced Configuration (Performance): 30%
  - Situation-Based Questions: 30%

## Continuing Education

Certified developers are encouraged to:
- Stay active in the Mautic community
- Contribute to the Mautic project
- Maintain knowledge of new versions and features
- Recertify every 2 years