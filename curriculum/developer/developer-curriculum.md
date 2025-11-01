#  Mautic Developer Curriculum
*A structured learning path for becoming a Mautic developer.*

This reorganized curriculum follows a natural progression — from installing Mautic, to backend development, frontend customization, database mastery, plugins, events, reporting, and, testing.

---

##  Phase 1: Foundation & Setup

### **Module 1: Prerequisites for Mautic**
Before developers begin, they must understand the runtime environment needed for Mautic.

**Learning Objectives**
- PHP version requirements and extensions
- Database requirements (MySQL/MariaDB)
- Apache/Nginx configuration
- Memory, security, and performance considerations

**Official References**
- https://devdocs.mautic.org/en/5.x/development-environment/getting_started.html

---

### **Module 2: Local Setup with DDEV**
With prerequisites understood, developers now create a consistent local environment.

**Learning Objectives**
- Install DDEV
- Set up Mautic using containers
- Configure debugging: Xdebug, Blackfire, Xhprof
- Unit testing setup in development

**Official References**
- https://ddev.readthedocs.io
- https://devdocs.mautic.org/en/5.x/development-environment/environments.html

>  **Transition**: With a running local instance, developers next explore Mautic from a user perspective.

---

### **Module 3: Mautic Platform Walkthrough**
A complete guided tour of the application.

**Learning Objectives**
- Contacts, segments, email & SMS campaigns
- Forms, landing pages, assets
- Dashboard, reports, configuration and permissions

**Official References**
- https://docs.mautic.org/en/5.x/getting_started/index.html

---

### **Module 4: Configuration & Administration**
Developers now learn how real-world Mautic instances are configured.

**Learning Objectives**
- Email transport settings
- Performance, caching, multi-tenancy
- Cron setup (high level)
- Security configurations

**Official References**
- https://docs.mautic.org/en/5.x/configuration/index.html

---

##  Phase 2: Core Development & Architecture

### **Module 5: Mautic + Symfony Architecture**
We now move into backend development.

**Learning Objectives**
- Bundle structure
- Services and DI container
- Forms, routing, validation, translations
- IntegrationsBundle basics

---

### **Module 6: Debugging, Logs & Performance**
Before building features, developers need debugging tools ready.

**Learning Objectives**
- Xdebug, profiler tools
- Log monitoring
- Browser devtools
- Remote debugging

---

### **Module 7: Security Best Practices**
Security first — especially in marketing automation.

**Key Topics**
- XSS, CSRF, SQL injection
- Secure API endpoints
- Permissions & roles
- File uploads and HTTPS

---

##  Phase 3: APIs & Integrations

### **Module 8: Mautic API Overview**
**Learning Objectives**
- Authentication (OAuth, Basic)
- Rate limits
- Endpoints overview

---

### **Module 9: Working with REST API**
**Learning Objectives**
- CRUD operations
- Contacts, campaigns, emails, assets, forms
- Error handling, pagination, bulk updates

---

### **Module 10: Creating Custom API Endpoints**
**Learning Objectives**
- Routes
- Controllers & serialization
- Authentication
- Documentation and testing

---

##  Phase 4: Plugin Development Track

### **Module 11: Plugin Ecosystem Overview**
**Learning Objectives**
- Installing, activating, configuring plugins
- Marketplace
- Version compatibility

---

### **Module 12: Plugin Architecture**
**Learning Objectives**
- Folder structure
- Config, services, events
- UI and forms
- Database integration

---

### **Module 13: Plugin Development Environment**
**Learning Objectives**
- IDE debugging
- Composer dependencies
- Version control
- CI setup

---

### **Module 14: Building Your First Plugin**
**Learning Objectives**
- Plugin scaffolding
- Event listeners/hooks
- Configuration forms
- Console commands

---

### **Module 15: Plugin Updates & Maintenance**
**Learning Objectives**
- Semantic versioning
- Database migrations
- Backward compatibility
- Packaging

---

### **Module 16: Testing Plugins**
Plugin testing sits *next to* plugin development to avoid a learning gap.

**Learning Objectives**
- Unit testing (PHPUnit)
- Functional testing workflows
- Fake data fixtures
- Automated CI pipeline

---

##  Phase 5: Code Quality & Community Participation

### **Module 17: Continuous Integration & Code Quality**
**Learning Objectives**
- PHPStan, Rector, CS Fixer
- PHPUnit test suites
- Code coverage
- GitHub Actions

---

### **Module 18: Contribution Guide**
**Learning Objectives**
- Fork, branch, pull request workflow
- Reporting issues
- Feature proposals
- Contributor License Agreement

---

##  Phase 6: UI, Themes & Email Development

### **Module 19: UI Customization**
**Learning Objectives**
- Themes
- Menu/navigation changes
- Dashboard widgets
- Permissions-based display

---

### **Module 20: Twig Templating**
**Learning Objectives**
- Blocks, inheritance, filters
- Debugging & performance
- Translations

---

### **Module 21: Landing Page Templates**
**Learning Objectives**
- Tokens, personalization
- Forms, responsive layouts
- SEO & performance

---

### **Module 22: Email Templates with MJML**
**Learning Objectives**
- MJML syntax
- Responsive emails
- Personalization
- Dark mode support

---

### **Module 23: Custom JS & CSS Integration**
**Learning Objectives**
- Asset bundling
- 3rd party libraries
- XSS protection
- Performance tuning

---

##  Phase 7: Database & ORM

### **Module 24: Database Architecture Overview**
**Learning Objectives**
- Key tables
- Queues, tracking tables
- Configuration storage

---

### **Module 25: Doctrine ORM in Mautic**
**Learning Objectives**
- Repository patterns
- Query builder
- Lazy loading
- Transactions

---

### **Module 26: Custom Entities**
**Learning Objectives**
- Entity mapping & relationships
- Forms & validation
- API exposure

---

### **Module 27: Migrations & Schema Updates**
**Learning Objectives**
- Migration files
- Rollbacks
- Deployment safety

---

##  Phase 8: Automation & Events

### **Module 28: CLI & Cron Jobs**
**Learning Objectives**
- Built-in commands
- Queue processing
- Custom console commands

---

### **Module 29: Event System Overview**
**Learning Objectives**
- Core event lifecycle
- Priority & performance

---

### **Module 30: Event Listeners**
**Learning Objectives**
- Listener classes
- Modifying event responses

---

### **Module 31: Event Subscribers**
**Learning Objectives**
- Multiple-event classes
- Conditional logic
- Testing subscribers

---

##  Phase 9: Marketing Logic Development

### **Module 32: Email & Campaign Development**
**Learning Objectives**
- Campaign builder integration
- Tracking & analytics
- Personalization

---

### **Module 33: Advanced Campaign Logic**
**Learning Objectives**
- Decision trees
- Scheduling
- Debugging

---

### **Module 34: Advanced Customization**
**Learning Objectives**
- Custom campaign actions
- External automation
- Custom analytics

---

##  Phase 10: Reporting

### **Module 35: Using & Extending Reports**
**Learning Objectives**
- Custom report types
- Query building
- Exporting & scheduling
- Widgets & data sources

---

##  Phase 11: Testing & Release Readiness

### **Module 36: Testing & Debugging**
**Learning Objectives**
- Unit, functional, integration tests
- Fixtures, mocks, CI pipelines
- Measuring code coverage

---