# Certified Mautic Developer Curriculum

## Course Overview

This comprehensive curriculum is designed to train developers to become certified Mautic experts, covering everything from basic setup to advanced plugin development and API integration.

## Prerequisites

- Basic PHP knowledge (OOP concepts, Symfony framework familiarity preferred)
- Understanding of web development (HTML, CSS, JavaScript)
- Database concepts (MySQL/MariaDB)
- Command line interface experience
- Git version control basics

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
- [Installation Requirements](https://docs.mautic.org)
- [System Requirements](https://docs.mautic.org)
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
- Performance optimization in development

### Official Reference Links
- [DDEV Installation Guide](https://ddev.readthedocs.io)
- [Local Development Setup](https://docs.mautic.org)
- [DDEV Troubleshooting](https://ddev.readthedocs.io)

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
- [Mautic Platform Overview](https://docs.mautic.org)
- [User Interface Guide](https://docs.mautic.org)
- [Managing Contacts](https://docs.mautic.org)

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

### Official Reference Links
- [Configuration Settings](https://docs.mautic.org)
- [Email Configuration](https://docs.mautic.org)
- [System Configuration](https://docs.mautic.org)

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

### Official Reference Links
- [Developer Documentation Overview](https://developer.mautic.org)
- [Plugin Development Guide](https://developer.mautic.org)
- [Customizing Themes](https://developer.mautic.org)

## Module 6: Mautic's API Overview

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
- [API Configuration](https://developer.mautic.org)
- [API Documentation](https://developer.mautic.org)
- [Authentication Setup](https://developer.mautic.org)

## Module 7: Working with Mautic's REST API

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
- [API Documentation](https://developer.mautic.org)
- [Authentication Guide](https://developer.mautic.org)
- [GitHub Examples](https://github.com/mautic/api-library)

## Module 8: Building Custom API Endpoints

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
- [Developer Documentation](https://developer.mautic.org)
- [API Development Guide](https://developer.mautic.org)
- [GitHub Repository](https://github.com/mautic/mautic)

## Module 9: Plugin Development

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

### Official Reference Links
- [Plugin Development](https://developer.mautic.org)
- [Plugin Marketplace](https://www.mautic.org)
- [Integration Testing](https://developer.mautic.org)

## Module 10: Introduction to Mautic Plugins

### Learning Objectives
- Explore existing plugins and their functionality
- Understand plugin installation and management
- Learn about plugin marketplace and distribution

### Context
Before creating plugins, it's important to understand the existing plugin ecosystem and how plugins integrate with Mautic's core functionality.

### Key Topics
- Plugin marketplace overview
- Installation and activation
- Plugin configuration
- Common plugin patterns
- Plugin dependencies
- Version compatibility
- Community plugins vs. commercial plugins

### Official Reference Links
- [Plugin Documentation](https://developer.mautic.org)
- [Mautic Marketplace](https://www.mautic.org)
- [Knowledge Base](https://kb.mautic.org)

## Module 11: Setting Up a Plugin Development Environment

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
- [Development Setup Guide](https://developer.mautic.org)
- [GitHub Documentation](https://github.com/mautic/mautic)
- [Developer Resources](https://developer.mautic.org)

## Module 12: Creating Your First Mautic Plugin

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

### Official Reference Links
- [Plugin Development Tutorial](https://developer.mautic.org)
- [Code Examples](https://github.com/mautic/mautic)
- [Community Resources](https://www.mautic.org)

## Module 13: Handling Plugin Updates and Maintenance

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
- [Plugin Maintenance Guide](https://developer.mautic.org)
- [Version Management](https://developer.mautic.org)
- [Best Practices](https://developer.mautic.org)

## Module 14: Customizing the User Interface

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
- [UI Customization Guide](https://developer.mautic.org)
- [Theme Development](https://developer.mautic.org)
- [Design Resources](https://developer.mautic.org)

## Module 15: Mautic's Twig Templating Engine

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

### Official Reference Links
- [Template Development](https://developer.mautic.org)
- [Twig Documentation](https://twig.symfony.com)
- [Customization Examples](https://developer.mautic.org)

## Module 16: Customizing Mautic's Email and Landing Page Templates

### Learning Objectives
- Create custom email templates
- Develop responsive landing page templates
- Implement template variables and personalization

### Context
Email and landing page templates are crucial for marketing campaigns. This module covers creating professional, responsive templates with proper personalization.

### Key Topics
- Email template structure and best practices
- Landing page template development
- Responsive design techniques
- Template variables and tokens
- Personalization and dynamic content
- A/B testing considerations
- Cross-client compatibility

### Official Reference Links
- [Email Templates](https://developer.mautic.org)
- [Email Configuration](https://docs.mautic.org)
- [GrapesJS Builder](https://developer.mautic.org)

## Module 17: Adding Custom JavaScript and CSS

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
- [Frontend Development](https://developer.mautic.org)
- [Asset Management](https://developer.mautic.org)
- [Performance Guide](https://developer.mautic.org)

## Module 18: Database and Entities

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
- [Database Documentation](https://developer.mautic.org)
- [Entity Reference](https://developer.mautic.org)
- [Performance Guide](https://developer.mautic.org)

## Module 19: Understanding Mautic's Database Schema

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
- [Segments Management](https://docs.mautic.org)
- [Database Schema](https://developer.mautic.org)
- [Contact Management](https://docs.mautic.org)

## Module 20: Working with Doctrine ORM in Mautic

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
- [Doctrine Integration](https://developer.mautic.org)
- [ORM Guide](https://developer.mautic.org)
- [Database Best Practices](https://developer.mautic.org)

## Module 21: Creating Custom Entities

### Learning Objectives
- Design and implement custom entities
- Set up entity relationships
- Implement entity validation and constraints

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
- [Entity Development](https://developer.mautic.org)
- [Custom Entity Guide](https://developer.mautic.org)
- [Development Examples](https://developer.mautic.org)

## Module 22: Database Migrations and Schema Updates

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
- [Migration Guide](https://developer.mautic.org)
- [Schema Management](https://developer.mautic.org)
- [Deployment Best Practices](https://developer.mautic.org)

## Module 23: Command Line Interface

### Learning Objectives
- Understand Mautic's CLI architecture
- Execute built-in commands
- Monitor and troubleshoot CLI operations

### Context
Mautic's CLI provides powerful tools for administration, maintenance, and automation. This module covers the available commands and their usage.

### Key Topics
- CLI architecture and structure
- Built-in command overview
- Cron job management
- Queue processing
- Cache management
- Database operations
- Debugging and logging

### Official Reference Links
- [CLI Commands](https://docs.mautic.org)
- [Cron Jobs Setup](https://docs.mautic.org)
- [Queue Management](https://docs.mautic.org)

## Module 24: Introduction to Mautic CLI

### Learning Objectives
- Set up and configure Mautic CLI
- Understand command structure and options
- Implement basic CLI operations

### Context
The command line interface is essential for many Mautic operations, especially in production environments. This module introduces the CLI and its capabilities.

### Key Topics
- CLI installation and setup
- Command structure and syntax
- Help and documentation
- Configuration options
- Environment considerations
- Error handling and logging
- Security considerations

### Official Reference Links
- [CLI Setup Guide](https://docs.mautic.org)
- [Command Line Reference](https://docs.mautic.org)
- [Administration Guide](https://docs.mautic.org)

## Module 25: Automating Tasks with Mautic CLI

### Learning Objectives
- Automate routine tasks using CLI
- Set up cron jobs and scheduled tasks
- Implement monitoring and alerting

### Context
Automation is crucial for maintaining a healthy Mautic installation. This module covers how to automate common tasks using the CLI.

### Key Topics
- Cron job configuration
- Queue processing automation
- Email sending automation
- Data cleanup and maintenance
- Monitoring and alerting
- Performance optimization
- Error handling and recovery

### Official Reference Links
- [Cron Jobs Configuration](https://docs.mautic.org)
- [Command Line Interface](https://docs.mautic.org)
- [Automation Tasks](https://docs.mautic.org)

## Module 26: Creating Custom CLI Commands

### Learning Objectives
- Develop custom CLI commands
- Implement proper command structure
- Handle command arguments and options

### Context
Custom CLI commands allow developers to create specialized automation tools tailored to specific needs. This module covers the development of custom commands.

### Key Topics
- Command class structure
- Argument and option handling
- Input validation
- Output formatting
- Progress indicators
- Error handling
- Command registration
- Testing custom commands

### Official Reference Links
- [Custom Command Development](https://developer.mautic.org)
- [CLI Architecture](https://developer.mautic.org)
- [Development Examples](https://developer.mautic.org)

## Module 27: Event Listeners and Subscribers

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
- [Event System Guide](https://developer.mautic.org)
- [Event Reference](https://developer.mautic.org)
- [Development Patterns](https://developer.mautic.org)

## Module 28: Understanding Mautic Events

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
- [Event Documentation](https://developer.mautic.org)
- [Event Catalog](https://developer.mautic.org)
- [Integration Guide](https://developer.mautic.org)

## Module 29: Creating Event Listeners

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
- [Event Listener Guide](https://developer.mautic.org)
- [Listener Development](https://developer.mautic.org)
- [Code Examples](https://developer.mautic.org)

## Module 30: Using Event Subscribers

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
- [Event Subscriber Guide](https://developer.mautic.org)
- [Subscriber Patterns](https://developer.mautic.org)
- [Advanced Examples](https://developer.mautic.org)

## Module 31: Email and Campaign Development

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
- [Email Development](https://developer.mautic.org)
- [Campaign Architecture](https://developer.mautic.org)
- [Marketing Automation](https://docs.mautic.org)

## Module 32: Customizing Email Templates

### Learning Objectives
- Create responsive email templates
- Implement dynamic content
- Optimize for deliverability

### Context
Email templates are crucial for effective marketing campaigns. This module covers advanced template development techniques and best practices.

### Key Topics
- Template architecture and structure
- Responsive design techniques
- Dynamic content integration
- Personalization tokens
- Deliverability optimization
- Testing across email clients
- Performance considerations

### Official Reference Links
- [Email Template Guide](https://developer.mautic.org)
- [Template Development](https://developer.mautic.org)
- [Design Best Practices](https://developer.mautic.org)

## Module 33: Developing Campaign Logic

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
- [Campaign Builder](https://docs.mautic.org)
- [Creating Campaigns](https://docs.mautic.org)
- [Campaign Troubleshooting](https://kb.mautic.org)

## Module 34: Advanced Email and Campaign Customization

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
- [Advanced Customization](https://developer.mautic.org)
- [Custom Actions](https://developer.mautic.org)
- [Integration Guide](https://developer.mautic.org)

## Module 35: Testing and Debugging

### Learning Objectives
- Set up comprehensive testing environments
- Implement debugging strategies
- Create automated test suites

### Context
Testing and debugging are crucial for maintaining high-quality Mautic installations and custom development. This module covers tools and techniques for effective testing.

### Key Topics
- Testing environment setup
- Debugging tools and techniques
- Automated testing strategies
- Performance testing
- Security testing
- Integration testing
- Continuous integration

### Official Reference Links
- [Troubleshooting Guide](https://kb.mautic.org)
- [Testing Environment Setup](https://developer.mautic.org)
- [Update Troubleshooting](https://kb.mautic.org)

## Module 36: Setting Up a Debugging Environment

### Learning Objectives
- Configure development debugging tools
- Implement logging and monitoring
- Set up performance profiling

### Context
A proper debugging environment is essential for efficient development and troubleshooting. This module covers setting up comprehensive debugging tools.

### Key Topics
- IDE debugging configuration
- Logging setup and management
- Performance profiling tools
- Error tracking and monitoring
- Database query debugging
- Frontend debugging
- Remote debugging techniques

### Official Reference Links
- [Debugging Setup](https://developer.mautic.org)
- [Development Tools](https://developer.mautic.org)
- [Troubleshooting Guide](https://kb.mautic.org)

## Module 37: Writing Unit Tests for Mautic

### Learning Objectives
- Create comprehensive unit tests
- Implement test-driven development
- Set up automated testing pipelines

### Context
Unit testing ensures code quality and prevents regressions. This module covers creating effective unit tests for Mautic development.

### Key Topics
- PHPUnit configuration
- Test case structure
- Mocking and fixtures
- Database testing
- API testing
- Plugin testing
- Test coverage analysis

### Official Reference Links
- [Unit Testing Guide](https://developer.mautic.org)
- [Testing Framework](https://developer.mautic.org)
- [Quality Standards](https://developer.mautic.org)

## Module 38: Testing API Endpoints and Plugins

### Learning Objectives
- Test API functionality comprehensively
- Implement plugin testing strategies
- Create integration test suites

### Context
API endpoints and plugins require specialized testing approaches. This module covers testing strategies for these components.

### Key Topics
- API endpoint testing
- Plugin functionality testing
- Integration testing
- Performance testing
- Security testing
- Automated testing pipelines
- Test documentation

### Official Reference Links
- [API Testing Guide](https://developer.mautic.org)
- [Plugin Testing](https://developer.mautic.org)
- [Integration Testing](https://developer.mautic.org)

## Assessment and Certification

### Certification Requirements
- Complete all modules with passing grades
- Pass the comprehensive certification exam (80 questions)
- Complete a capstone project demonstrating practical skills
- Maintain continuing education requirements

### Exam Format
**80 multiple-choice questions**
- **Basic Configuration** (10% - 8 questions)
- **Advanced Coding** (30% - 24 questions)
- **Advanced Configuration** (30% - 24 questions)
- **Situational Questions** (30% - 24 questions)

### Continuing Education
- Annual recertification required
- Participation in Mautic community events
- Contribution to open-source projects (optional)
- Advanced specialization tracks available

## Additional Resources

### Official Documentation
- [Mautic Documentation](https://docs.mautic.org)
- [Installation Guide](https://docs.mautic.org)
- [GitHub Documentation](https://github.com/mautic/mautic)
- [Knowledge Base](https://kb.mautic.org)
- [Official Website](https://mautic.org)

### Community Resources
- Mautic Community Forums
- Developer Slack Channel
- GitHub Issues and Discussions
- Community Events and Meetups
- Blog and Tutorial Resources

### Support
- Technical support through official channels
- Community support forums
- Professional services directory
- Training and consulting resources

