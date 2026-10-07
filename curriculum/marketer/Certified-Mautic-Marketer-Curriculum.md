# Certified Mautic Marketer Curriculum

## Course Overview

This comprehensive curriculum is designed to train marketers to become certified Mautic practitioners, covering everything from contact management through segmentation, multi-channel components, campaign automation, lead scoring and real-world campaign builds.

Unlike the Developer track, this certification assumes no PHP, Symfony or command-line skill. It tests the ability to plan, build, launch and measure marketing programmes inside a running Mautic instance.

**Target platform version:** Mautic 6.x
**Reference documentation baseline:** `https://docs.mautic.org/en/6.0/`

Every reference link points to the official Mautic 6.0 product documentation.

## Prerequisites

- Working knowledge of digital marketing concepts (lead capture, nurture, segmentation, lifecycle stages)
- Familiarity with email marketing practice
- Access to a working Mautic 6.x instance with scheduled background jobs configured, for hands-on practice

No installation or server administration skill is required, and none is assessed. Where a task belongs to an administrator, this curriculum teaches the Marketer to confirm it is in place, not to perform it.

## Module 1: Introduction to Mautic

### Learning Objectives
- Explain what Mautic is and the marketing problems it solves
- Describe how contacts, components, channels and campaigns relate to one another
- Identify where marketing results are reported in the platform

### Context
Mautic brings contact data, content components, delivery channels and automation into one platform. Before touching any single feature, a marketer needs the mental model of how those parts connect — this module establishes that map so every later module has somewhere to attach.

### Key Topics
- What marketing automation is; what Mautic is and what it offers
- How Mautic works end to end
- Contact management as the core data layer
- Components vs Channels vs Campaigns
- Where marketing results surface: the Dashboard, and Reports (Module 38)

### Hands-On Exercise
Walk an existing contact record end to end and narrate which part of the platform generated each piece of activity.

### Official Reference Links
- [Mautic overview](https://docs.mautic.org/en/6.0/overview/overview.html)

## Module 2: Tracking Setup and Instance Readiness

### Learning Objectives
- Deploy the tracking script and verify contacts are being tracked
- Identify what must already be in place before campaigns can run
- Recognise when a marketing result has failed for an instance reason, and escalate it accurately

### Context
A Marketer does not install or administer Mautic. They do, however, own the consequences when the instance is not ready: nothing automates itself without the scheduled background jobs, and no behaviour is tracked without the tracking script. This module teaches the Marketer to confirm both, and to tell the difference between a campaign that is built wrong and an instance that is not running — so the right person is asked for the right fix.

### Key Topics
- The tracking script: Global Configuration → Tracking Settings; the snippet; installing it through a CMS integration
- Tracking depth: the tracking pixel, embedding the pixel, identifying visitors by tracking URL, how contacts are tracked
- The scheduled background jobs marketing depends on: segments, campaigns, custom fields
- Scheduled jobs behind specific features: the email queue and scheduled broadcasts
- Reading a symptom correctly: a segment that does not fill, a campaign step that never fires, a visitor who leaves no record

### Hands-On Exercise
Deploy the tracking script to a test page and confirm a visitor record appears. Then, given a segment that has not updated and a campaign step that has not fired, identify which scheduled job each is waiting on and write the escalation you would send to whoever administers the instance.

### Official Reference Links
- [Cron jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html)
- [Segment scheduled jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#segment-cron-jobs)
- [Campaign scheduled jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#campaign-cron-jobs)
- [Custom Field scheduled jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#custom-field-cron-jobs)
- [Tracking script](https://docs.mautic.org/en/6.0/configuration/tracking_script.html)
- [Managing Contacts — Contact tracking](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html#contact-tracking)
- [How are Contacts tracked with the tracking script](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html#how-are-contacts-tracked-with-the-tracking-script)
- [Cookies used by Mautic](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html#cookies-used-by-mautic)

## Module 3: UI Walkthrough

### Learning Objectives
- Navigate the Mautic interface and locate each functional area
- Build and customise a Dashboard for a marketing team
- Use Categories and search operators to find and organise records

### Context
Mautic's feature set is broad and its navigation is not self-evident. This module orients the candidate to where everything lives, then covers the three cross-cutting tools that make a large instance workable: the Dashboard, Categories, and the search syntax.

### Key Topics
- Guided tour of the main areas: Contacts, Channels, Segments, Campaigns, Components, Reports, Dashboard, Settings
- Dashboard: date range filter, widgets, widget ordering, dashboard import/export, widget cache, permissions
- Categories: creating and managing, using categories for contacts
- Search operators and per-entity search filters (Contacts, Segments, Emails, Forms, Landing Pages, Focus Items, Stages, Reports)
- The Publish/Unpublish control and where it applies across entities

### Hands-On Exercise
Build a marketing dashboard with at least four widgets, export it, and re-import it into a second user account. Then use search operators to isolate all contacts in a given segment who opened a specific email.

### Official Reference Links
- [Dashboard](https://docs.mautic.org/en/6.0/dashboard/dashboard.html)
- [Categories](https://docs.mautic.org/en/6.0/categories/categories-overview.html)
- [Searching Mautic](https://docs.mautic.org/en/6.0/search/search_operators.html)

## Module 4: Marketer-Facing Configuration

### Learning Objectives
- Locate and interpret the configuration settings that change marketing outcomes
- Distinguish the settings a Marketer owns from those that belong to an administrator, and know what to ask for

### Context
Configuration governs how the whole instance behaves, but only part of it is the Marketer's to touch. Mail transport, queues and monitored inboxes are infrastructure. What a Marketer must be able to find and reason about are the settings that decide whether opens are tracked, how often a contact can be messaged, and how imports and merges treat their data.

### Key Topics
- System settings and system defaults
- Open and link tracking
- The default frequency rule, and unsubscribe settings
- Contact settings: merge settings, list settings, import and export settings
- Segment, Company, Landing Page, Form and Tracking settings
- Which settings are out of the Marketer's hands, and how to raise a change request for them

### Hands-On Exercise
Confirm email open and link tracking are enabled, set a default frequency rule, and produce a short list separating the settings you changed from the settings you would need an administrator to change.

### Official Reference Links
- [Mautic configuration settings](https://docs.mautic.org/en/6.0/configuration/settings.html)

## Module 5: Users, Roles and Permissions

### Learning Objectives
- Explain what roles and permissions control in Mautic
- Work effectively within the permissions you have, and request the ones you need

### Context
Creating users and shaping roles is administrator work. A Marketer still needs to understand the model, because permissions are why a button is missing, why a publish fails, and why a colleague cannot see the segment you built. Understanding this turns a bug report into an access request.

### Key Topics
- What roles control, and how permissions surface in the interface as missing or disabled actions
- Full system access versus granular permissions
- The permission options and what each one allows
- Recognising a permission problem rather than a platform fault

### Hands-On Exercise
Inspect your own role's permissions and identify which activities in this curriculum you can perform, which need a colleague, and which need an administrator. Produce the access request you would send, naming the specific permissions required.

### Official Reference Links
- [Managing Users](https://docs.mautic.org/en/6.0/users_roles/managing_users.html)
- [Roles](https://docs.mautic.org/en/6.0/users_roles/managing_roles.html)

## Module 6: Working with Integrated Systems

### Learning Objectives
- Describe what an existing integration makes available in Mautic, and what it does not
- Specify the field mapping marketing needs, for an integrator to implement
- Recognise when contact data is stale because a sync has failed

### Context
Mautic is rarely the only system holding customer data. Installing and configuring an integration is integrator work, but the Marketer is the one who knows which fields marketing actually needs, and the one who notices first when synced data stops arriving. This module covers consuming an integration, not building one.

### Key Topics
- Which systems commonly integrate with Mautic, and what a plugin adds
- How synced fields appear on a contact record, and how to tell them from fields Mautic owns
- Using synced fields in segment filters and campaign conditions
- The limits of a sync: direction, timing, and fields that do not come across
- Spotting stale data, and what to report when a sync has stopped

### Hands-On Exercise
Given a CRM field list, write the mapping specification you would hand an integrator: which Mautic fields must exist first, which segments and campaigns depend on them, and which direction each field needs to sync.

### Official Reference Links
- [Mautic Marketplace](https://docs.mautic.org/en/6.0/marketplace/marketplace.html)
- [Plugin resources](https://docs.mautic.org/en/6.0/plugins/plugin_resources.html)

## Module 7: Contact Fundamentals

### Learning Objectives
- Distinguish between visitors (unidentified) and standard contacts
- Explain how Mautic tracks anonymous visitors and converts them to known contacts

### Context
Mautic tracks people before it knows who they are. Understanding the visitor-to-contact transition explains where a contact's early history comes from and why some records appear with activity but no name.

### Key Topics
- Contact types: visitors (formerly "anonymous leads") vs standard contacts
- Changing the contact list view

### Hands-On Exercise
Identify a visitor record in the instance and trace which action converted a visitor into a known contact.

### Official Reference Links
- [Contacts](https://docs.mautic.org/en/6.0/contacts/contacts_overview.html)

## Module 8: Adding Contacts

### Learning Objectives
- Add contacts individually and in bulk
- Prepare and execute a CSV import with correct field mapping
- Use a background import to avoid browser timeouts on large files

### Context
Most instances are populated by import, and a bad import is expensive to undo. This module covers file preparation, the mapping step where data quality is won or lost, and the choice between an in-browser and a background import.

### Key Topics
- Quick add and Add new Contact
- Import file requirements and field mapping
- Types of import: browser-based vs background job
- Import job list, starting and stopping imports
- Exporting contact lists

### Hands-On Exercise
Import a 100-row CSV containing at least two custom fields using a background import job, then verify field mapping accuracy on five sample records.

### Official Reference Links
- [Managing Contacts — Importing Contact lists](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html#importing-contact-lists)
- [Import Contacts](https://docs.mautic.org/en/6.0/contacts/import_contacts.html)

## Module 9: Managing Contacts

### Learning Objectives
- Edit, merge, batch-action and organise contact records
- Read a contact's engagement history and interpret it for campaign decisions
- Create and publish custom fields and apply tags

### Context
This is the day-to-day work of the role. A marketer spends more time reading and correcting contact records than building anything, and the engagement history is the primary evidence behind every segmentation and campaign decision.

### Key Topics
- Editing contacts, managing duplicates, merging two contacts, batch actions
- Individual contact details: engagements chart, history, notes, changing segments and campaigns
- Contact tracking: website monitoring, tracking pixel, mobile monitoring, cookies
- Custom fields: adding, publishing, locally defined countries and regions
- Tags: creating, adding to contacts, and using tags in campaigns, forms and segments

### Hands-On Exercise
Merge two duplicate contacts, add a custom field for "Industry", tag 20 contacts by industry via batch action, and use a tag-based segment filter to isolate them.

### Official Reference Links
- [Managing Contacts](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html)
- [Manage Custom Fields](https://docs.mautic.org/en/6.0/contacts/custom_fields.html)
- [Tags](https://docs.mautic.org/en/6.0/contacts/tags.html)

## Module 10: Consent, Tracking Permission and Communication Frequency

### Learning Objectives
- Identify what Mautic tracks, and which controls govern it
- Configure frequency rules to control contact fatigue
- Build a preference centre and wire it into emails
- Distinguish a marketing send from a transactional one, and know why it matters

### Context
Consent is not a single setting in Mautic. It is spread across what the tracking script records, what the contact chooses in the preference centre, how often frequency rules allow a message, and whether a send counts as marketing or transactional. This module gathers those controls into one place so a Marketer can reason about them together, rather than meeting each one in isolation.

The curriculum teaches the controls Mautic provides. What any particular organisation is required to do with them is a legal question and is deliberately out of scope.

### Key Topics
- What Mautic records about a visitor: the tracking script, the tracking pixel, and the cookies Mautic sets
- The Anonymize IP setting and what it is for
- Frequency rules: global and per-contact, and the Do Not Contact limit
- Transactional versus marketing email, and why only one of them is subject to the frequency limit
- Preference centre: preferred channels and frequency, contact categories, contact segments, unsubscribe preferences
- Creating a Preference Center landing page, preference tokens, setting preference pages in emails
- Double opt-in as the record of a subscription
- What the Marketer decides, and what belongs to the organisation's legal position
- Where deliverability sits: sender authentication and domain reputation are administrator work and are not assessed here; the Marketer's contribution is list hygiene, frequency discipline and honouring unsubscribes

### Hands-On Exercise
Build a preference centre page with channel and category options and link it from an email footer using the correct preference token. Then trace one contact end to end: what was tracked before they were known, what they have since chosen, and which of your planned sends would reach them.

### Official Reference Links
- [Frequency rules](https://docs.mautic.org/en/6.0/contacts/frequency_rules.html)
- [Preference center](https://docs.mautic.org/en/6.0/contacts/preference_center.html)
- [Cookies used by Mautic](https://docs.mautic.org/en/6.0/contacts/manage_contacts.html#cookies-used-by-mautic)
- [Tracking settings, including Anonymize IP](https://docs.mautic.org/en/6.0/configuration/settings.html#tracking-settings)
- [Contact settings, including the Do Not Contact frequency limit](https://docs.mautic.org/en/6.0/configuration/settings.html#contact-settings)

## Module 11: Adding and Managing Companies

### Learning Objectives
- Create company records and associate contacts with them
- Apply company scoring and identify a contact's primary company
- Use company data in campaigns and segments

### Context
B2B marketing needs an account-level view, not just a person-level one. Mautic's company records group contacts, carry their own fields and score, and can be assigned automatically — which makes them useful for segmentation but easy to duplicate if the assignment routes are not understood.

### Key Topics
- Creating and managing companies
- Company custom fields and company segments
- Identifying companies; company duplicates and merging companies
- Assigning companies to contacts: contact profile, contacts list view, via a campaign, through a form
- Company scoring and setting the primary company
- Company actions in campaigns; engagements/points chart

### Hands-On Exercise
Create five company records, auto-assign contacts through a form submission, set a primary company for a multi-company contact, and build a company-based segment.

### Official Reference Links
- [Companies](https://docs.mautic.org/en/6.0/companies/companies_overview.html)
- [Assigning Companies to Contacts](https://docs.mautic.org/en/6.0/companies/companies_overview.html#assigning-companies-to-contacts)
- [Configuration settings — Company settings](https://docs.mautic.org/en/6.0/configuration/settings.html)

## Module 12: Segment Fundamentals

### Learning Objectives
- Create a segment and choose the correct type for a use case
- Explain how segments are kept current

### Context
Segments are how audiences are addressed everywhere else in Mautic — emails, campaigns, dynamic content all take a segment as input. The critical concept is that segment membership is not always live: a dynamic segment is only as current as the last scheduled rebuild.

### Key Topics
- Creating a segment; public segments and preference-centre availability; the published toggle
- Viewing contact segments; exporting contacts of a segment
- Deleting all contacts in a segment; deleting vs deactivating a segment
- Segment rebuild dependency on the scheduled background job

### Hands-On Exercise
Create two segments for the same audience — one static, one dynamic — and compare membership after a data change and a scheduled rebuild.

### Official Reference Links
- [Managing Segments — Creating a Segment](https://docs.mautic.org/en/6.0/segments/manage_segments.html#creating-a-segment)
- [Viewing Contact Segments](https://docs.mautic.org/en/6.0/segments/manage_segments.html#viewing-contact-segments)
- [Deleting or deactivating a Segment](https://docs.mautic.org/en/6.0/segments/manage_segments.html#deleting-or-deactivating-a-segment)
- [Segment scheduled jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#segment-cron-jobs)

## Module 13: Static Segments

### Learning Objectives
- Populate a static segment through each supported method
- Choose static segmentation appropriately (event lists, imported lists, manual cohorts)

### Context
A static segment holds exactly who was put into it and nothing more. It suits fixed cohorts — an event attendee list, an imported list, a manually curated group — and Mautic documents five distinct ways contacts get in, each belonging to a different part of the platform.

### Key Topics
- Static segments are not filter-based
- Manually moving contacts: batch updating contacts, adding individual contacts
- Using a campaign action to add to a segment
- Form submit action
- Points trigger
- CSV upload

### Hands-On Exercise
Populate one static segment using all five documented methods and verify the membership count after each.

### Official Reference Links
- [Static Segments](https://docs.mautic.org/en/6.0/segments/manage_segments.html#static-segments)
- [Manually moving Contacts](https://docs.mautic.org/en/6.0/segments/manage_segments.html#manually-moving-contacts)
- [Using a Campaign action](https://docs.mautic.org/en/6.0/segments/manage_segments.html#using-a-campaign-action)
- [Form submit action](https://docs.mautic.org/en/6.0/segments/manage_segments.html#form-submit-action)
- [Points trigger](https://docs.mautic.org/en/6.0/segments/manage_segments.html#points-trigger)
- [CSV upload](https://docs.mautic.org/en/6.0/segments/manage_segments.html#csv-upload)

## Module 14: Dynamic Segments

### Learning Objectives
- Build filter-based segments using the correct operators
- Apply date filters, including relative and anniversary-style expressions
- Predict how contacts move into and out of a dynamic segment

### Context
Dynamic segments are filter-driven, and Mautic moves contacts in and out as the underlying data changes. Choosing the right operator — and understanding the date filter vocabulary — is what separates a segment that returns the intended audience from one that silently returns nobody.

### Key Topics
- How Mautic moves contacts in and out based on applied filters
- Configuring segment filters; AND/OR logic
- Operators; matching part of a string (starts with, ends with, contains, like, regular expression)
- Using date filters and date options — relative formats and text date formulas

### Hands-On Exercise
Build three dynamic segments: one behavioural (email opened), one demographic (custom field), one date-based (activity in the last 30 days). Verify each after a scheduled rebuild.

### Official Reference Links
- [Dynamic Segments](https://docs.mautic.org/en/6.0/segments/manage_segments.html#dynamic-segments)
- [Configuring Segment filters](https://docs.mautic.org/en/6.0/segments/manage_segments.html#configuring-segment-filters)
- [Operators](https://docs.mautic.org/en/6.0/segments/manage_segments.html#operators)
- [Matching part of a string](https://docs.mautic.org/en/6.0/segments/manage_segments.html#matching-part-of-a-string)
- [Using Date Filters](https://docs.mautic.org/en/6.0/segments/manage_segments.html#using-date-filters)
- [Date options](https://docs.mautic.org/en/6.0/segments/manage_segments.html#date-options)

## Module 15: Working with Assets

### Learning Objectives
- Upload, categorise and publish downloadable assets
- Track asset downloads as contact activity and attribute them with UTM codes
- Use a gated asset as a lead-capture mechanism

### Context
Assets turn a file download into a tracked, attributable marketing event. Gating an asset behind a form is one of the most common lead-capture patterns, and UTM codes on the asset make the resulting traffic measurable.

### Key Topics
- Managing assets and asset categories
- Creating a new asset: uploading, using remote assets, adding UTM codes
- Viewing, editing and deleting an asset
- Displaying assets directly in the browser

### Hands-On Exercise
Publish a gated PDF as an asset with UTM codes, deliver it via a form submit action, and confirm the download appears in the contact's history.

### Official Reference Links
- [Assets](https://docs.mautic.org/en/6.0/components/assets.html)
- [Creating a new Asset](https://docs.mautic.org/en/6.0/components/assets.html#creating-a-new-asset)

## Module 16: Introduction to Forms

### Learning Objectives
- Distinguish campaign forms from standalone forms and choose correctly
- Configure form-level settings and understand progressive profiling

### Context
The first decision when building any Mautic form is its type, and it cannot be changed casually afterwards. A campaign form hands control to a campaign workflow; a standalone form executes its actions immediately. Getting this wrong constrains everything the form can do.

### Key Topics
- Campaign Form — triggers a campaign on submission; fewer immediate submit actions
- Standalone Form — executes many submit actions immediately on submission
- Creating a new form; form details; configuring forms
- Progressive profiling
- Blocking form submissions from specified domains
- Reading form results

### Hands-On Exercise
Build one campaign form and one standalone form for the same offer and document which submit actions are available to each.

### Official Reference Links
- [Forms — Creating a new Form](https://docs.mautic.org/en/6.0/components/forms.html#creating-a-new-form)
- [Configuring Forms](https://docs.mautic.org/en/6.0/components/forms.html#configuring-forms)
- [Progressive profiling](https://docs.mautic.org/en/6.0/components/forms.html#progressive-profiling)
- [Blocking Form submissions from specified domains](https://docs.mautic.org/en/6.0/components/forms.html#blocking-form-submissions-from-specified-domains)

## Module 17: Creating Various Forms

### Learning Objectives
- Select and configure the correct field type for each data need
- Map form fields to contact and company fields
- Apply validation, CAPTCHA and conditional field logic
- Configure submit actions

### Context
A form is only as useful as the data it lands in the right field. This module covers the full field palette, the mapping that connects a form field to a contact field, and the submit actions that turn a submission into segmentation, scoring and delivery.

### Key Topics
- Field types and field options: general, mapped field, validation, properties, attributes, behavior
- CAPTCHA
- Checkbox group, radio group and select fields; description area; file upload; text
- Field order
- Creating conditional form fields
- Form actions (submit actions)
- Layout control: applying styling classes to lay a form out in two columns

### Hands-On Exercise
Build a multi-field registration form with a conditional field, CAPTCHA, a mapped custom field, and three submit actions (add to segment, send email, adjust points).

### Official Reference Links
- [Fields](https://docs.mautic.org/en/6.0/components/forms.html#fields)
- [Field options](https://docs.mautic.org/en/6.0/components/forms.html#field-options)
- [Creating conditional Form fields](https://docs.mautic.org/en/6.0/components/forms.html#creating-conditional-form-fields)
- [Form actions](https://docs.mautic.org/en/6.0/components/forms.html#form-actions)

## Module 18: Embedding Forms on Webpages

### Learning Objectives
- Deploy a Mautic form on an external website using each supported method
- Choose the right embed method for a given CMS and tracking requirement

### Context
A form that lives only inside Mautic captures nothing. Mautic offers four routes onto an external site, and they differ in how much control the marketer has and how reliably the submission is tracked — so the choice is a real decision, not a formality.

### Key Topics
- Adding forms to pages
- Via JavaScript (automatic embed)
- Via iframe
- Self-hosted (manual copy of the form markup)
- Shortcodes for WordPress and Joomla

### Hands-On Exercise
Embed the same form three ways — automatic embed, iframe and self-hosted — on test pages and compare tracking behaviour for each.

### Official Reference Links
- [Adding Forms to Pages](https://docs.mautic.org/en/6.0/components/forms.html#adding-forms-to-pages)
- [Via JavaScript](https://docs.mautic.org/en/6.0/components/forms.html#via-javascript)
- [Via iframe](https://docs.mautic.org/en/6.0/components/forms.html#via-iframe)
- [Self-hosted](https://docs.mautic.org/en/6.0/components/forms.html#self-hosted)
- [Shortcodes](https://docs.mautic.org/en/6.0/components/forms.html#shortcodes)

## Module 19: Introduction to Landing Pages and Building Landing Pages

### Learning Objectives
- Create a landing page in Mautic and apply a theme
- Use the drag-and-drop builder to construct a responsive page
- Work with landing page drafts, preview and publish scheduling
- Build a Preference Center landing page

### Context
Landing pages are where campaign traffic converts. Mautic's drag-and-drop builder lets a marketer assemble a responsive page without code, apply a branded theme, and schedule the page to be live only for a defined window.

### Key Topics
- Setting up a simple landing page end to end
- The drag-and-drop builder: blocks, styling, responsive design, structure panel, code view, asset manager
- Enabling the builder; switching back to the legacy builder
- Templates and themes; custom fonts
- Landing page drafts: Save as Draft / Apply Draft / Discard Draft; one draft per page; previewing a draft
- Publish-up and publish-down scheduling against the system timezone
- Embedding a form and a raw content block on a page
- Customizing the Preference Center

### Hands-On Exercise
Build a landing page with a hero, an embedded form and an asset download link, applied to a chosen theme. Save a draft, preview it, then schedule it to publish for a fixed window.

### Official Reference Links
- [Email & Landing Page Builder](https://docs.mautic.org/en/6.0/builders/email_landing_page.html)
- [Manage Themes](https://docs.mautic.org/en/6.0/themes/manage_themes.html)
- [Landing Pages](https://docs.mautic.org/en/6.0/components/landing_pages.html)

## Module 20: Dynamic Web Content

### Learning Objectives
- Explain how Dynamic Web Content personalises a webpage per visitor
- Implement Dynamic Web Content slots on a website
- Build both campaign-based and filter-based dynamic content

### Context
Dynamic Web Content lets a marketer show different content to different people in a defined region of a webpage. It works in two modes — driven by a campaign decision, or by a standalone contact filter — and always needs default content for visitors who match nothing.

### Key Topics
- Preparation; website configuration; Mautic configuration
- Creating Dynamic Web Content slots
- Campaign-based Dynamic Web Content: creating the request, creating the filters, pushing the content
- Filter-based Dynamic Web Content: creating filters
- Implementing Dynamic Web Content and setting default content
- Slot placement on the site, and the WordPress and Joomla shortcode routes

### Hands-On Exercise
Place a Dynamic Web Content slot on a test page with default content, then serve two different variants — one campaign-driven, one filter-driven — and verify each renders for the right contact.

### Official Reference Links
- [Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html)
- [Creating Dynamic Web Content slots](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html#creating-dynamic-web-content-slots)
- [Campaign-based Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html#campaign-based-dynamic-web-content)
- [Filter-based Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html#filter-based-dynamic-web-content)
- [Implementing Dynamic Web Content](https://docs.mautic.org/en/6.0/components/dynamic_web_content.html#implementing-dynamic-web-content)

## Module 21: Introduction to Emails

### Learning Objectives
- Choose between Template and Segment (Broadcast) emails
- Personalise emails with tokens, signatures and owner-based sending
- Send, schedule and test an email
- Configure tracking and unsubscribe handling

### Context
Email remains the primary channel for most Mautic users, and the first decision — Template or Segment email — determines how the message can be sent and whether it can be A/B tested. This module also covers the operational side a Marketer is accountable for: tracking and unsubscribes.

### Key Topics
- Email types: Template emails, Segment (Broadcast) emails, excluding segments
- Email formats
- Managing emails: email overview, drafts, previewing drafts, translations, cloning
- Tokens: default value, encoded value, date formats
- Mailer as owner; sending from the contact owner; overriding the setting
- Signatures
- Scheduling a send via the publish date, picked up by the scheduled broadcast job; the email must have a published date and be currently published
- Testing an email before sending
- Tracking opened emails and tracking links in emails
- Unsubscribing; online version; contact replies
- Troubleshooting emails

### Hands-On Exercise
Create one template email and one segment email for the same message. Schedule the segment email to send at a set time and verify the scheduled broadcast fires it.

### Official Reference Links
- [Emails](https://docs.mautic.org/en/6.0/channels/emails.html)
- [Email types](https://docs.mautic.org/en/6.0/channels/emails.html#email-types)
- [Template Emails](https://docs.mautic.org/en/6.0/channels/emails.html#template-emails)
- [Segment (Broadcast) Emails](https://docs.mautic.org/en/6.0/channels/emails.html#segment-broadcast-emails)
- [Tokens](https://docs.mautic.org/en/6.0/channels/emails.html#tokens)
- [Tracking Opened Emails](https://docs.mautic.org/en/6.0/channels/emails.html#tracking-opened-emails)
- [Unsubscribing](https://docs.mautic.org/en/6.0/channels/emails.html#unsubscribing)
- [Troubleshooting Emails](https://docs.mautic.org/en/6.0/channels/emails.html#troubleshooting-emails)
- [Send scheduled broadcasts (Segment Emails)](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#send-scheduled-broadcasts-segment-emails-cron-job)
- [Process Email queue](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#process-email-queue-cron-job)

## Module 22: Designing Email Templates

### Learning Objectives
- Build a branded, responsive email template using the drag-and-drop builder
- Apply and preview an approved theme
- Run an A/B test on a segment email and declare a winner
- Work within an approved theme, and know what to ask a designer for when it does not fit

### Context
Brand consistency across sends comes from themes, which a designer or administrator supplies. The drag-and-drop builder is where a Marketer assembles a template within that theme, without writing code. A/B testing sits alongside this: it is how a template's subject line and content decisions get validated rather than assumed.

### Key Topics
- Email builder overview
- Applying an approved theme; templates; custom fonts
- Previewing a theme before committing to it
- What a theme fixes and what the builder still lets you change
- A/B testing: create the parent, create the variant, set traffic weight (the sum across all variants must be no more than 100%), choose winner criteria (asset download rate, email read rate, clickthrough rate, form submission rate), declare a winner. A/B testing is available for Segment emails only.
- Translations, and previewing A/B and translation variants

### Hands-On Exercise
Choose an approved theme, build a branded template email from it with a header, two content blocks and a footer containing the unsubscribe and preference-centre links. Then create a segment email with two subject-line variants at 50/50 weight and set clickthrough rate as the winner criterion.

### Official Reference Links
- [Email & Landing Page Builder](https://docs.mautic.org/en/6.0/builders/email_landing_page.html)
- [Manage Themes](https://docs.mautic.org/en/6.0/themes/manage_themes.html)
- [Emails — Translations](https://docs.mautic.org/en/6.0/channels/emails.html#translations)

## Module 23: Introduction to Focus Items

### Learning Objectives
- Explain what a Focus Item is and when to use one
- Configure engagement triggers and frequency
- Deploy a Focus Item and measure its performance

### Context
Focus Items are Mautic's on-site engagement layer — bars, modals, notifications and full-page overlays that appear based on visitor behaviour. The engagement options are what make them tolerable rather than intrusive, so they deserve as much attention as the content itself.

### Key Topics
- Focus Item settings
- Engagement options: animate; when to engage (upon arrival, after slightly scrolling down, after scrolling to the middle, after scrolling to the bottom, visitor intends to leave); timeout before engage; how often to engage; stop engaging after conversion; stop engaging after closing
- Content: basic, editor, HTML
- Colors
- Creating a Focus Item and using the Focus Item builder
- Deploying to a website; deploying through a campaign
- Measuring success
- UTM tagging a Focus Item for attribution

### Hands-On Exercise
Create an exit-intent Focus Item, deploy it to a test page, and configure it to stop engaging after conversion. Review its performance metrics after test traffic.

### Official Reference Links
- [Focus Items](https://docs.mautic.org/en/6.0/channels/focus_items.html)
- [Focus Item settings](https://docs.mautic.org/en/6.0/channels/focus_items.html#focus-item-settings)
- [Engagement options](https://docs.mautic.org/en/6.0/channels/focus_items.html#engagement-options)
- [Creating a Focus Item](https://docs.mautic.org/en/6.0/channels/focus_items.html#creating-a-focus-item)
- [Using the Focus Item builder](https://docs.mautic.org/en/6.0/channels/focus_items.html#using-the-focus-item-builder)
- [Deploying to a website](https://docs.mautic.org/en/6.0/channels/focus_items.html#deploying-to-a-website)
- [Deploying through a Campaign](https://docs.mautic.org/en/6.0/channels/focus_items.html#deploying-through-a-campaign)
- [Measuring success](https://docs.mautic.org/en/6.0/channels/focus_items.html#measuring-success)
- [Using UTM tags in Focus Items](https://docs.mautic.org/en/6.0/channels/utm_tags.html#using-utm-tags-in-focus-items)

## Module 24: Exploring the Different Focus Items

### Learning Objectives
- Correctly distinguish Focus Item types from Focus Item styles
- Select the right type and style combination for a marketing objective

### Context
Mautic separates what a Focus Item *does* (its type) from how it *appears* (its style). These two axes are routinely conflated, and confusing them produces Focus Items that cannot achieve the objective they were built for — a notice styled as a bar cannot collect data, for instance.

### Key Topics
- Types of Focus Item — the three documented types:
  - **Collect Data** — presents a form, which must already exist, within the Focus Item
  - **Display a Notice** — presents a message to visitors
  - **Emphasize a link** — drives visitors to a specific link
- Styles — the four display formats: Bar, Modal, Notification, Full page
- Choosing a type and style pairing to match a stated marketing goal

### Hands-On Exercise
Build three Focus Items — one of each type — and present the same one in two different styles. Justify each type/style pairing against a stated marketing goal.

### Official Reference Links
- [Types of Focus Item](https://docs.mautic.org/en/6.0/channels/focus_items.html#types-of-focus-item)
- [Styles](https://docs.mautic.org/en/6.0/channels/focus_items.html#styles)
- [Bar](https://docs.mautic.org/en/6.0/channels/focus_items.html#bar)
- [Modal](https://docs.mautic.org/en/6.0/channels/focus_items.html#modal)
- [Notification](https://docs.mautic.org/en/6.0/channels/focus_items.html#notification)
- [Full page](https://docs.mautic.org/en/6.0/channels/focus_items.html#full-page)

## Module 25: Creating Marketing Messages

### Learning Objectives
- Explain how a Marketing Message delivers on a contact's preferred channel
- Create a Marketing Message across multiple channels
- Predict channel fallback behaviour under frequency rules, and recognise which channels an instance actually has available

### Context
A Marketing Message is one message that Mautic delivers on whichever channel the contact prefers, with Email as the default when no preference is set. It is the mechanism that turns channel preference from a stated wish into actual delivery behaviour, and it interacts directly with frequency rules.

### Key Topics
- What Marketing Messages are: one message, delivered on the channel the contact prefers
- Email as the default channel when no preference is set
- Channels must be configured first or they do not appear as options
- Enabling each channel and selecting or creating the message
- Interaction with frequency rules and per-channel pausing — when a limit is exceeded Mautic uses another channel with available frequency
- How a second channel changes delivery, using SMS as the worked case — note that SMS needs a channel an administrator has configured, and is not assessed
- Dynamic Web Content as the complementary on-site personalisation channel (taught in Module 20)

### Hands-On Exercise
Create a Marketing Message using the channels your instance has configured, set a contact's channel preference in the preference centre, and confirm delivery follows it. Then describe what would change if a second channel were enabled.

### Official Reference Links
- [Marketing Messages](https://docs.mautic.org/en/6.0/channels/marketing_messages.html)
- [What are Marketing Messages?](https://docs.mautic.org/en/6.0/channels/marketing_messages.html#what-are-marketing-messages)
- [Creating a Marketing Message](https://docs.mautic.org/en/6.0/channels/marketing_messages.html#creating-a-marketing-message)
- [Preference center](https://docs.mautic.org/en/6.0/contacts/preference_center.html)

## Module 26: Introduction to Campaigns

### Learning Objectives
- Recognise the three campaign types the documentation describes, and shape a campaign to the brief
- Explain why a campaign is used rather than a one-off send
- Explain how contacts enter and progress through a campaign

### Context
The documentation broadly categorises campaigns into three types: time driven, contact driven and mixed. They are a way of thinking about what starts a campaign and what carries a contact through it, not a fixed taxonomy to be memorised — most real campaigns mix timing and behaviour.

### Key Topics
- Why use a campaign
- Campaign types
- Time-driven campaigns
- Contact-driven campaigns
- Mixed campaigns

### Hands-On Exercise
Given three marketing briefs, describe for each what starts the campaign and what carries a contact through it, then say which type it leans toward and where the line blurs.

### Official Reference Links
- [Campaigns overview](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html)
- [Campaign types](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html#campaign-types)
- [Time driven Campaigns](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html#time-driven-campaigns)
- [Contact driven Campaigns](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html#contact-driven-campaigns)
- [Mixed Campaigns](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html#mixed-campaigns)

## Module 27: Creating Campaign Forms and Emails

### Learning Objectives
- Identify and prepare the prerequisites a campaign depends on
- Build the specific forms and emails a campaign will call

### Context
Mautic will not let a campaign reference assets that do not yet exist. Segments, forms and emails must be built first, which makes campaign asset preparation a discipline in its own right rather than something improvised inside the builder.

### Key Topics
- Campaign prerequisites — segments, forms and emails must exist first
- Campaign forms vs standalone forms in a campaign context
- Template emails as campaign-callable assets

### Hands-On Exercise
Prepare a complete campaign asset set before building any campaign: one segment, one campaign form, three template emails and one landing page.

### Official Reference Links
- [Creating Campaigns — Prerequisites](https://docs.mautic.org/en/6.0/campaigns/creating_campaigns.html#prerequisites)
- [Forms — Creating a new Form](https://docs.mautic.org/en/6.0/components/forms.html#creating-a-new-form)
- [Emails — Template Emails](https://docs.mautic.org/en/6.0/channels/emails.html#template-emails)

## Module 28: Building New Campaigns

### Learning Objectives
- Build a campaign in the Campaign Builder using contact sources, decisions, actions and conditions
- Read and construct green and red paths correctly
- Apply delays, smart scheduling and date-based triggers

### Context
The Campaign Builder is the centre of the platform. Three event types drive everything: decisions record what the contact does, actions are what Mautic does, and conditions test what is true about the contact. Green and red paths then branch the flow on whether a decision was met.

### Key Topics
- Creating a campaign; contact sources — contact segments and contact forms, and mixing both
- **Decisions** — what the contact does
- **Actions** — what Mautic does
- **Conditions** — what is true about the contact
- Green paths (positive or affirmative) and red paths (non-action)
- Notes on campaign actions; notes on delayed conditions and dates
- Using a custom date field to trigger a campaign
- Smart event schedule; scheduling events; triggering campaign events; cloning campaign events
- Adding or removing contacts in batch

### Hands-On Exercise
Build a five-step campaign containing at least one decision with both green and red paths, one condition, one delay and one action that changes segment membership. Launch it against a test segment.

### Official Reference Links
- [Creating Campaigns](https://docs.mautic.org/en/6.0/campaigns/creating_campaigns.html)
- [Using the Campaign Builder](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html)
- [Getting started with Campaign Builder](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#getting-started-with-campaign-builder)
- [Decisions](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#decisions)
- [Actions](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#actions)
- [Conditions](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#conditions)
- [Green paths](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#green-paths)
- [Red paths](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#red-paths)
- [Using a custom date field to trigger a Campaign](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#using-a-custom-date-field-to-trigger-a-campaign)
- [Smart event schedule](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#smart-event-schedule)

## Module 29: Managing and Troubleshooting Campaigns

### Learning Objectives
- Monitor a running campaign and interpret its statistics
- Quantify campaign drop-off using Reports, covered in Module 38
- Diagnose the common reasons a campaign step fails to fire
- Stop a running campaign safely

### Context
A launched campaign is not a finished campaign. Marketers must be able to read the overview screen, quantify drop-off through Reports, and recognise the documented reasons a step silently fails — most commonly testing while logged in as an administrator, whose activity Mautic ignores.

### Key Topics
- The campaign overview screen: Details drop-down, Campaign Statistics panel, Preview / Decisions / Actions / Conditions / Contacts tabs, Recent Activity panel
- Where campaign numbers actually come from: the Campaign Events data source in Reports (Module 38)
- Why page visits are not recognised: testing while logged in as an administrator, contact not in the campaign, sequential execution, URL pattern matching without a wildcard
- Campaign dependency on the scheduled background job
- Stopping a campaign by unpublishing it

### Hands-On Exercise
Deliberately break a campaign (for example a page-visit decision that never fires), diagnose it against the troubleshooting page, and fix it. Then use the Campaign Events data source, as taught in Module 38, to quantify the drop-off.

### Official Reference Links
- [Managing Campaigns](https://docs.mautic.org/en/6.0/campaigns/managing_campaigns.html)
- [Troubleshooting Campaigns](https://docs.mautic.org/en/6.0/campaigns/troubleshooting_campaigns.html)
- [Reports — Data sources](https://docs.mautic.org/en/6.0/reports/reports.html#data-sources)
- [Campaign scheduled jobs](https://docs.mautic.org/en/6.0/configuration/cron_jobs.html#campaign-cron-jobs)

## Module 30: Manage Actions (Point Actions)

### Learning Objectives
- Define point actions that award or deduct points from contact behaviour
- Design a scoring model that reflects real buying intent
- Apply decay and suppression to keep scores meaningful

### Context
Point actions are the times when a contact's point total changes, positively or negatively, based on a behaviour the marketer has chosen to value. A scoring model is only useful if it discriminates — which means deciding what is genuinely high-intent and what merely looks busy.

### Key Topics
- Point actions: those times when a contact receives a change in their point total — positive or negative, based on a determined action
- Behaviours that can award points
- Mapping trust and intent: low value, high value, decreasing value actions
- Decay models and suppression segments
- Points troubleshooting: point actions fire only once per contact; they do not register for logged-in administrators; URL patterns must match exactly or use wildcards

### Hands-On Exercise
Build a five-action scoring model (page visit, form submit, email open, email click, asset download) and validate that scores accrue correctly on a test contact.

### Official Reference Links
- [Points](https://docs.mautic.org/en/6.0/points/points.html)
- [Point Actions](https://docs.mautic.org/en/6.0/points/points.html#point-actions)
- [Points troubleshooting](https://docs.mautic.org/en/6.0/points/points_troubleshooting.html)

## Module 31: Manage Triggers (Point Triggers)

### Learning Objectives
- Configure point triggers that fire once a point threshold is reached
- Distinguish triggers from actions confidently
- Build an MQL alert from a point threshold

### Context
Where point actions change the score, point triggers react to it: once a contact reaches a minimum point total, a trigger fires an event. Conflating actions with triggers is the most common conceptual error in Mautic scoring, and it produces models that award points but never act on them.

### Key Topics
- Point triggers: once a contact has accumulated a point total, trigger an action — fired on reaching a minimum point threshold
- The distinction from point actions: actions award or deduct points from behaviour, triggers fire events once a total is reached
- Campaign triggers, contact triggers, email triggers, add-on triggers
- Designing an MQL alert: when to trigger it, and who should receive it

### Hands-On Exercise
Create a trigger that, at 50 points, adds the contact to an "MQL" segment and notifies the contact owner.

### Official Reference Links
- [Point Triggers](https://docs.mautic.org/en/6.0/points/points.html#point-triggers)
- [Campaign triggers](https://docs.mautic.org/en/6.0/points/points.html#campaign-triggers)
- [Contact triggers](https://docs.mautic.org/en/6.0/points/points.html#contact-triggers)
- [Email triggers](https://docs.mautic.org/en/6.0/points/points.html#email-triggers)

## Module 32: Point Groups

### Learning Objectives
- Score contacts on multiple independent scales rather than one global total
- Use point groups across campaigns, forms, segments and reports

### Context
A single global score cannot distinguish between a contact interested in one product and a contact broadly engaged with everything. Point groups provide independent scoring scales, and they surface across campaigns, forms, segments and reports.

### Key Topics
- Managing point groups; point groups usage
- Using point actions and point triggers with groups
- Campaign condition; campaign action; form action; segment filters
- Contact details; group report; webhooks

### Hands-On Exercise
Create two point groups (for example "Product Interest" and "Engagement"), score against both, and build a segment that requires a threshold in each.

### Official Reference Links
- [Point Groups](https://docs.mautic.org/en/6.0/points/point_groups.html)
- [Point Groups usage](https://docs.mautic.org/en/6.0/points/point_groups.html#point-groups-usage)

## Module 33: Stages

### Learning Objectives
- Model a marketing lifecycle using stages
- Move contacts between stages and visualise progression
- Align stages to a business workflow

### Context
Stages model the lifecycle a contact moves through, and two rules govern them: a contact only moves to a stage of equal or higher weight, and the move requires a campaign action rather than a manual edit. Both constraints shape how a lifecycle must be designed.

### Key Topics
- What stages are and why they are used
- Creating stages: name, description, weight, published/active state
- The weight rule — contacts only move to a stage of equal or higher weight
- Moving contacts between stages requires a campaign action, "Change Contact's Stage"; stage changes are campaign-driven, not manual
- Visualising stage movement
- Lifecycle; aligning stages with business workflows

### Hands-On Exercise
Define a four-stage lifecycle (Subscriber, Lead, MQL, SQL), build the campaign actions that move contacts between them, and review the stage movement visualisation.

### Official Reference Links
- [Stages](https://docs.mautic.org/en/6.0/stages/stages.html)
- [Creating Stages](https://docs.mautic.org/en/6.0/stages/stages.html#creating-stages)
- [Moving Contacts between Stages](https://docs.mautic.org/en/6.0/stages/stages.html#moving-contacts-between-stages)
- [Visualizing Stage movement](https://docs.mautic.org/en/6.0/stages/stages.html#visualizing-stage-movement)
- [Lifecycle](https://docs.mautic.org/en/6.0/stages/stages.html#lifecycle)

## Module 34: Welcome Series Campaign

### Learning Objectives
- Build a multi-email onboarding sequence with time delays and behavioural branching
- Implement double opt-in as the entry point

### Context
The welcome series is the canonical first campaign: a form captures a subscriber, a confirmation step records their opt-in, and a timed sequence builds the relationship. It exercises segments, forms, template emails, delays and decision branching together.

Mautic ships no example campaigns and no campaign template library, so this module is an applied build: it composes the segments, forms, emails, delays and decisions taught in earlier modules into one working sequence.

### Key Topics
- Time-based drip pattern: segment entry, email 1 immediately, email 2 after 7 days, email 3 after 14 days
- Condition-based branching: an "Email sent" trigger, then an "Opened email" decision — green path sends the next email, red path waits a day and sends an alternative
- Double opt-in structure: subscription form, add to a pending segment, send the opt-in email, decide on a visit to the verification page, then swap segments and send the welcome email; if not confirmed, wait and resend
- Three-segment model: pending, confirmed, welcomed
- Monitoring subscriptions and best practices

### Hands-On Exercise
Build a complete double opt-in welcome series: form, confirmation email, welcome email, then a two-email nurture with an open-based branch. Test the form end to end.

### Official Reference Links
- [Using the Campaign Builder](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html)
- [Form actions](https://docs.mautic.org/en/6.0/components/forms.html#form-actions)
- [Template Emails](https://docs.mautic.org/en/6.0/channels/emails.html#template-emails)
- [Static Segments — Form submit action](https://docs.mautic.org/en/6.0/segments/manage_segments.html#form-submit-action)

## Module 35: Event Promotion Campaign

### Learning Objectives
- Build a time-driven campaign anchored to a fixed event date
- Combine registration capture, progressive profiling, reminder sequencing and post-event follow-up

### Context
An event campaign is the clearest case of a time-driven campaign: everything is scheduled backwards from a fixed date. It also shows progressive profiling at its most useful, enriching a registrant's record across several touches rather than demanding everything up front.

This module is an applied build. There is no single feature to learn here — the campaign is assembled from mechanics taught earlier, and the references below point at each of those in turn.

### Key Topics
- Time-driven campaign model
- Event campaign shape: invitation email with a registration link, immediate confirmation, progressive profiling capturing additional attributes across touches, a pre-event logistics email, one automated reminder to non-registrants, and a post-event follow-up
- Registration form as the campaign entry point
- Segment separation of registrants versus non-registrants
- Delay-based reminder sequencing
- Focus Item or landing page for on-site promotion
- UTM tagging for attribution
- Known platform limitation: Mautic cannot natively segment by time of day, which constrains "X hours before the event" reminders — teach date-level reminders and state the constraint

### Hands-On Exercise
Build an end-to-end webinar promotion campaign: landing page and registration form with progressive profiling, a three-email reminder sequence, a Focus Item promoting the event, and a post-event follow-up split by attendance.

### Official Reference Links
- [Campaigns overview — Time driven Campaigns](https://docs.mautic.org/en/6.0/campaigns/campaigns_overview.html#time-driven-campaigns)
- [Using the Campaign Builder](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html)
- [Forms — Progressive profiling](https://docs.mautic.org/en/6.0/components/forms.html#progressive-profiling)
- [Email & Landing Page Builder](https://docs.mautic.org/en/6.0/builders/email_landing_page.html)
- [Focus Items](https://docs.mautic.org/en/6.0/channels/focus_items.html)
- [UTM tags](https://docs.mautic.org/en/6.0/channels/utm_tags.html)

## Module 36: Birthday Greetings Campaign

### Learning Objectives
- Build a recurring date-triggered campaign
- Apply anniversary and date-formula segment filters correctly
- Anticipate the documented limitations of date-based triggering

### Context
A birthday campaign looks trivial and is not. Mautic documents three constraints that defeat the obvious build: conditions evaluate immediately rather than waiting to become true, the recommended "date equals today" segment pattern does not apply to the Anniversary option, and a contact passes through a campaign only once even if the date value later changes.

### Key Topics
- Using a custom date field to trigger a campaign: select the date field in a contact-field condition, then select date as the operator; in the Anniversary option only day and month values can be entered
- Documented constraint 1: conditions evaluate immediately — contacts do not wait for a condition to become true
- Documented constraint 2: the recommended pattern is a segment filtered on a date field equal to today, driving the campaign — but this does not work for the Anniversary option
- Documented constraint 3: a contact passes through a campaign only once, even if the date value later changes — the key constraint for yearly birthday sends
- Segment date formulas, including birthday and anniversary expressions with offsets, plus relative date formats

### Hands-On Exercise
Create a birthday date custom field, build a date-based segment using an anniversary formula, drive a greeting campaign from it, and document how the "passes through once" constraint is handled for annual repetition.

### Official Reference Links
- [Using a custom date field to trigger a Campaign](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#using-a-custom-date-field-to-trigger-a-campaign)
- [Notes on delayed conditions and dates](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html#notes-on-delayed-conditions-and-dates)
- [Managing Segments — Using Date Filters](https://docs.mautic.org/en/6.0/segments/manage_segments.html#using-date-filters)
- [Date options](https://docs.mautic.org/en/6.0/segments/manage_segments.html#date-options)
- [Manage Custom Fields](https://docs.mautic.org/en/6.0/contacts/custom_fields.html)

## Module 37: Feedback Request Campaign

### Learning Objectives
- Trigger a feedback request from a behavioural, score or stage-based signal
- Capture structured responses without a survey tool, using a one-click auto-submitting form
- Route responses back into segmentation and branch on them

### Context
Mautic has no survey feature, so structured feedback is collected with a form rather than a questionnaire. The documented pattern uses two campaigns: one that requests feedback and chases non-responders, and one that processes the response and branches on it.

This module is an applied build, assembled from the campaign, form, stage and segment mechanics taught earlier.

### Key Topics
- The two-campaign feedback-loop pattern:
  1. *Request campaign:* the signal fires, the contact is added to a filterless static "Needs Feedback" segment, a delay follows, the request email is sent, the contact is removed from the campaign, and the cycle repeats until answered
  2. *Response mechanic:* the email carries one-click buttons linking to a landing page holding an embedded auto-submitting form, one per response option
  3. *Process campaign:* on submission the contact is removed from "Needs Feedback" and branched by response, each branch taking a different downstream action
- Adapting the pattern for customer-facing feedback: campaign entry from a stage change, point threshold or asset download
- Feedback form design: rating fields, conditional follow-up fields, mapped custom fields
- Form submit actions to tag, score and segment on the response
- Delay-and-remind logic for non-responders
- Frequency rules so a feedback request does not collide with other sends

### Hands-On Exercise
Build a post-purchase feedback campaign: stage-change entry, a one-click feedback email, a landing page with an auto-submitting form, tag and segment by response, a reminder for non-responders after 3 days, and branch handling per response.

### Official Reference Links
- [Using the Campaign Builder](https://docs.mautic.org/en/6.0/campaigns/campaign_builder.html)
- [Stages — Moving Contacts between Stages](https://docs.mautic.org/en/6.0/stages/stages.html#moving-contacts-between-stages)
- [Creating conditional Form fields](https://docs.mautic.org/en/6.0/components/forms.html#creating-conditional-form-fields)
- [Form actions](https://docs.mautic.org/en/6.0/components/forms.html#form-actions)
- [Tags](https://docs.mautic.org/en/6.0/contacts/tags.html)
- [Frequency rules](https://docs.mautic.org/en/6.0/contacts/frequency_rules.html)

## Module 38: Reports and Measurement

### Learning Objectives
- Choose the right data source for a marketing question
- Build a report with the columns, filters, ordering and grouping that answer it
- Add graphs, and reuse them in a Dashboard widget
- Schedule a report for recurring delivery, and export its data

### Context
Every preceding module builds something. This one measures it. Reports is where marketing activity becomes numbers a Marketer can act on and defend — which emails earned engagement, which forms convert, where contacts fall out of a campaign. The skill is less about operating the report builder than about choosing the data source that can answer the question being asked, because each data source exposes a different set of columns, filters and graphs.

### Key Topics
- Getting to Reports, and what the reporting tools are for: tracking marketing metrics, identifying what is working or needs improvement, and investigating why something is happening
- Data sources, and the parent/child pattern — the parent gives a high-level summary, the child a more granular view of contact behaviour including custom fields
- The data sources that answer marketing questions:
  - Emails, and Emails Sent
  - Campaigns → Campaign Events
  - Forms, and Form Submissions
  - Assets, and Asset Downloads
  - Contacts → Segment Membership, Do Not Contact, UTM Codes, Contact Point Log, and the attribution sources
  - Pages → Landing Pages and Page hits
  - Companies
- Report details: name, description, published, visible for all logged-in Users, owner
- Dynamic filter settings: opened by default, and hiding the date range
- Data: choosing columns and why ID is recommended in every report; ordering, and how multiple order fields interact; filters, including the common Email Not Empty filter for identified contacts; dynamic filters for the reader
- Group by, to show one row per contact rather than per event, and calculated columns — count, average, sum, minimum, maximum — which are only available alongside a grouping
- Graphs, and using them in Dashboard widgets
- Scheduling a report for delivery, and the scheduled job behind it
- Report options and exporting; the totals row that calculated columns add is not included in an export

### Hands-On Exercise
Build three reports that answer three different questions: engagement for one segment's last email, form submissions grouped so each contact appears once, and campaign event drop-off for a running campaign. Add a graph to one, schedule it for weekly delivery, and export another to confirm what the export does and does not contain.

### Official Reference Links
- [Reports](https://docs.mautic.org/en/6.0/reports/reports.html)
- [Data sources](https://docs.mautic.org/en/6.0/reports/reports.html#data-sources)
- [Data — columns, order, filters, group by, calculated columns](https://docs.mautic.org/en/6.0/reports/reports.html#data)
- [Graphs](https://docs.mautic.org/en/6.0/reports/reports.html#graphs)
- [Schedule](https://docs.mautic.org/en/6.0/reports/reports.html#schedule)
- [Cron job to schedule Reports](https://docs.mautic.org/en/6.0/reports/reports.html#cron-job-to-schedule-reports)
- [Report options](https://docs.mautic.org/en/6.0/reports/reports.html#report-options)
- [Exporting Reports](https://docs.mautic.org/en/6.0/reports/reports.html#exporting-reports)

---

## Certification Requirements

To earn the Certified Mautic Marketer certification, candidates must:

1. Complete all 38 modules
2. Pass the certification exam with a score of 80% or higher
3. Pay the examination entry fee
4. Verify identity via the online examination platform

> **Open decision:** confirm whether the Marketer exam adopts the same 80% threshold as the published Developer track requirements, or a track-specific rule.

## Exam Details

- **Total Questions**: 75
- **Duration**: 90 minutes
- **Passing Score**: 80%
- **Question Format**: scenario-based and direct multiple choice, four options each, with a small proportion of multiple-response questions

Sizing is set for a no-code track rather than inherited from the Developer track: 75 questions in 90 minutes allows just over a minute per question. Candidates come to this exam with marketing experience behind them, so the paper tests applied judgement at working pace rather than rewarding slow deliberation. Questions are drawn from the accompanying question bank for each sitting.

## Continuing Education

Certified marketers are encouraged to:
- Review the Mautic 6.0 documentation thoroughly, module by module
- Complete every hands-on exercise on a live Mautic 6.x instance with scheduled background jobs running
- Stay active in the Mautic community
- Build at least two complete campaigns end to end before sitting the exam
- Maintain knowledge of new versions and features
- Recertify when a new major Mautic version enters Long Term Support
