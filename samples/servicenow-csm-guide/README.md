# ServiceNow Customer Service Management User Guide

**Version:** 1.0  
**Platform:** ServiceNow Customer Service Management (CSM)  
**Last Updated:** February 2026  
**Target Audience:** Customer Service Representatives

---

## Table of Contents

1. [Introduction](#introduction)
2. [Getting Started](#getting-started)
3. [Managing Customer Cases](#managing-customer-cases)
4. [Using the Agent Workspace](#using-the-agent-workspace)
5. [Knowledge Management](#knowledge-management)
6. [Customer Communications](#customer-communications)
7. [Reporting and Analytics](#reporting-and-analytics)
8. [Best Practices](#best-practices)

---

## Introduction

ServiceNow Customer Service Management (CSM) is a comprehensive platform designed to streamline customer support operations, improve response times, and enhance customer satisfaction. This guide covers the essential features that customer service teams use daily to deliver exceptional customer experiences.

### What You'll Learn

This guide will help you:
- Create and manage customer cases efficiently
- Navigate the Agent Workspace interface
- Leverage knowledge base articles to resolve issues faster
- Communicate effectively with customers across multiple channels
- Track performance metrics and customer satisfaction

### Prerequisites

Before using this guide, you should have:
- Active ServiceNow CSM user account
- Assigned role of `sn_customerservice_agent` or higher
- Basic understanding of your organization's customer service processes
- Access to your company's ServiceNow instance

---

## Getting Started

### Logging Into ServiceNow

1. Navigate to your organization's ServiceNow URL (typically `yourcompany.service-now.com`)
2. Enter your username and password
3. Complete multi-factor authentication if required
4. You'll land on the ServiceNow homepage

### Understanding Your Role

Your ServiceNow role determines which features you can access:

| Role | Permissions | Typical Use Case |
|------|-------------|------------------|
| Customer Service Agent | Create/update cases, view knowledge, respond to customers | Frontline support staff |
| Customer Service Manager | All agent permissions + reporting, SLA management | Team leads, supervisors |
| Customer Service Admin | Full system configuration and user management | System administrators |

To check your current role:
1. Click your profile icon in the top right corner
2. Select **Impersonate User** (if available, you have admin privileges)
3. Your assigned roles display under your name

### Navigating the Interface

**Application Navigator (Left Panel)**
- Use the search bar to quickly find modules
- Star frequently used modules for quick access
- Common shortcuts:
  - `Cases > All` - View all customer cases
  - `Knowledge > Articles` - Access knowledge base
  - `Dashboards > My Dashboard` - View personal metrics

**Content Frame (Center)**
- Displays lists, forms, and detailed views
- Use filters to narrow down records
- Right-click column headers to personalize views

**Connect Chat (Bottom Right)**
- Real-time collaboration with team members
- Share case links with colleagues
- Request assistance from specialists

---

## Managing Customer Cases

Cases are the central record type in CSM, representing customer inquiries, issues, or requests.

### Creating a New Case

**Method 1: Manual Case Creation**

1. Navigate to **Customer Service > Cases > Create New**
2. Fill in required fields:
   - **Contact**: Select or create the customer contact
   - **Subject**: Brief description of the issue (e.g., "Login error")
   - **Description**: Detailed information about the customer's issue
   - **Category**: Select appropriate category (Technical, Billing, Account, etc.)
3. Click **Submit** to create the case

**Method 2: Email-to-Case**

ServiceNow can automatically create cases from customer emails sent to your support address:

1. Customer emails `support@yourcompany.com`
2. System creates case automatically
3. Case number is emailed back to customer
4. Agent receives assignment notification

**Method 3: Portal Self-Service**

Customers can create cases through your customer portal:
1. Customer logs into portal
2. Clicks "Get Help" or "Create Case"
3. Fills out web form
4. Case is created and assigned based on routing rules

### Case Fields Explained

Understanding key case fields ensures accurate record-keeping:

**Contact Information**
- **Contact**: The person reporting the issue
- **Email**: Primary email for case updates
- **Phone**: Contact number for urgent follow-up

**Case Details**
- **Subject**: One-line summary visible in lists and notifications
- **Description**: Full details of the customer's issue or request
- **Category**: Classifies the type of request
- **Subcategory**: More specific classification within category

**Assignment and Tracking**
- **Assigned to**: Individual agent responsible for resolution
- **Assignment group**: Team responsible (e.g., Billing)
- **State**: Current status (e.g., Open, Resolved, Closed)
- **Priority**: Importance of case (1-Critical, 2-High, 3-Medium, 4-Low, 5-Planning)

### Working a Case: Step-by-Step

**Step 1: Review Case Details**

When a case is assigned to you:
1. Open the case from your queue or notification
2. Read the **Description** field completely
3. Review **Work Notes** and **Activity** for added context
4. Check if related cases exist 

**Step 2: Acknowledge the Case**

Respond to the customer within SLA timeframe:
1. Scroll to **Activities** section
2. Click **Customer Communication** tab
3. Select template or compose message:
   ```
   Hello [Customer Name],
   
   Thank you for contacting us. I've received your request regarding [brief issue summary] 
   and am looking into this for you. I'll update you within [timeframe] with my findings.
   
   Case #: [CASE NUMBER]
   
   Best regards,
   [Your Name]
   ```
4. Click **Post** to send

**Step 3: Investigate and Troubleshoot**

Use available resources:
- **Knowledge Base**: Search for articles related to the issue
- **Related Cases**: Review how similar issues were resolved
- **Product Documentation**: Access technical references

**Step 4: Document Your Work**

Keep detailed notes in **Work Notes** (internal only):
- What you've tried
- Customer responses
- Information from other teams
- Next steps planned

Example work note:
```
2/12/2026 10:30 AM - Reviewed customer's account settings. 
Password reset attempted. Confirmed MFA is enabled. 
Checking with IT team on potential system-wide authentication issues.
```

**Step 5: Resolve the Case**

Once issue is resolved:
1. Communicate solution to customer
2. Include any follow-up steps customer should take
3. Update **Resolution Code**
4. Add **Resolution Notes** explaining the fix
5. Set **State** to **Resolved**
6. Click **Update**

If the customer is satisfied with the resolution, set the state to **Closed**. Cases may automatically move from Resolved to Closed after a configured period (for example, 3–7 days) if the customer does not respond.

### Case States and Workflow

Understanding case states helps you manage your workload:

| State | Meaning | When to Use |
|-------|---------|-------------|
| New | Just created, not yet acknowledged | System assigns this automatically |
| Open | Being actively worked | Set when you begin working the case |
| Resolved | Solution provided, awaiting confirmation | Set when issue is fixed |
| Closed | Case complete, no further action | Auto-set after resolution period |
| Cancelled | Invalid or duplicate case | Set when case shouldn't have been created |

### Using Case Queues

Queues help you organize and prioritize your work.

**Accessing Your Queue**

1. Navigate to **Customer Service > Cases > My Open Cases**
2. This displays all cases assigned to you that aren't resolved/closed

**Filtering Your Queue**

Use filters to focus on specific case types:
1. Right-click any column header
2. Select **Filter**
3. Choose filter criteria (e.g., Priority = 1-Critical)
4. Click **Run**

**Saving Custom Filters**

Save frequently used filters:
1. Apply your filter criteria
2. Click **Save filter** (filter icon at top)
3. Name your filter (e.g., "High Priority Cases")
4. Set visibility (Personal or Public if sharing with team)

**Recommended Queue Views**
- **By Priority**: Sort by Priority descending to handle critical cases first
- **By Category**: Group similar cases for efficient batch processing

---

## Using the Agent Workspace

The Agent Workspace is a unified interface designed for efficient case management.

### Workspace Overview

The Agent Workspace consists of three main areas:

**Left Panel: Case List**
- Displays your assigned cases
- Filter by state, priority, or custom criteria
- Quick search to find specific cases

**Center Panel: Case Details**
- Full case information and form fields
- Activities timeline (emails, notes, updates)
- Related records and knowledge articles

**Right Panel: Context Assistance**
- Suggested knowledge articles
- Similar cases for reference
- Contact and account information
- Quick actions menu

### Using Suggested Knowledge

The system automatically suggests relevant knowledge articles:

1. Open a case in Agent Workspace
2. View **Similar Articles** in right panel
3. Click an article title to preview
4. If helpful, click **Attach to Case** to link it

**Manually Searching Knowledge:**
1. Click **Search Knowledge** in right panel
2. Enter keywords related to the issue
3. Review search results
4. Click **View** to open full article
5. Use article content to resolve case

### Macros for Efficiency

Macros automate repetitive tasks with a single click.

**Example Macro Configuration**

1. Open a case
2. Click **Apply Macro** button (top right)
3. Browse available macros (e.g., "Request More Info")
4. Click macro name to apply

**What Macros Can Do:**
- Set field values automatically (State, Priority, Assignment)
- Send templated customer communications
- Add standardized work notes
- Update multiple fields simultaneously

**Example Macro: "Escalate to Technical Support"**
- Sets Assignment Group to "Technical Support"
- Adds work note: "Escalating for advanced troubleshooting"
- Sends customer email: "Your case has been escalated to our technical team"
- Changes Priority to 2-High

**Creating Custom Macros** (requires admin role)
1. Navigate to **Customer Service > Macros**
2. Click **New**
3. Configure actions, field updates, and communications
4. Save and share with team

### Timeline and Activity History

The Activities section provides complete case history:

**Tabs Available:**
- **All**: Combined view of all activity
- **Customer Communication**: Only emails sent/received
- **Work Notes**: Internal notes (customer doesn't see)
- **System Activity**: Automated updates and field changes

**Reading the Timeline:**
- Most recent activity appears at top
- Each entry shows timestamp and author
- Hover over entries to see full content
- Click **Show More** to expand truncated messages

**Adding Activities:**
- **Customer Communication**: Click to compose email to customer
- **Work Note**: Click to add internal documentation
- **@Mention**: Type @ followed by colleague's name for notification

---

## Knowledge Management

Knowledge articles help resolve cases faster by providing standardized solutions.

### Searching the Knowledge Base

**Basic Search**

1. Navigate to **Knowledge > Articles**
2. Enter keywords in search bar
3. Press Enter to see results
4. Click article title to view full content

**Common Search Filters:**
- **Category**: Filter by product area or topic
- **Published**: Only show approved articles
- **Rating**: Sort by most helpful articles

**Search Tips for Better Results:**
- Use specific product names or error codes
- Include symptoms, not just product names (e.g., "email bouncing" not just "email")
- Try different phrasings if first search yields no results
- Use quotes for exact phrases

### Using Knowledge Articles

**Reading an Article**

Articles typically contain:
- **Symptom**: Description of the problem
- **Cause**: Root cause explanation
- **Resolution**: Step-by-step fix instructions
- **Workaround**: Temporary solution if available

**Applying Article to Case**

1. Open knowledge article relevant to case
2. Click **Attach to Case**
3. Select the case from dropdown
4. Article is now linked in case's Related Lists

**Rating Articles**

Help improve knowledge quality:
1. After using an article, scroll to bottom
2. Click star rating (1-5 stars)
3. Add comment if article needs improvement
4. Submit rating

### Creating Knowledge Articles

Share solutions with your team by creating articles:

**When to Create an Article:**
- Multiple customers report the same problem
- A workaround exists for a known bug
- New product feature needs documentation

**Article Creation Process**

1. Navigate to **Knowledge > Create New Article**
2. Fill in required fields:
   - **Short Description**: Clear, searchable title
   - **Category**: Appropriate classification
   - **Article Body**: Full description
  
For example, use this template structure when detailing a resolved problem:
```
Problem:
[Describe the symptom or error the customer experiences]

Cause:
[Explain what causes this issue]

Resolution:
Step 1: [First action to take]
Step 2: [Second action to take]
Step 3: [Continue until resolved]

Expected Result:
[What the customer should see after following steps]

Notes:
[Any additional context, limitations, or alternative methods]
```

4. Click **Submit for Approval**
5. Knowledge manager reviews and publishes

**Article Best Practices:**
- Write in clear, plain language
- Number all steps for easy following
- Include screenshots for visual clarity
- Test your own steps before submitting
- Keep articles focused on one issue
- Update articles when processes change

---

## Customer Communications

Effective communication is essential for customer satisfaction.

### Communication Channels

ServiceNow CSM supports multiple communication methods:

**Email**
- Primary channel for detailed updates
- Automatically logged in case timeline
- Customers can reply directly to create case updates

**Phone**
- Document calls in work notes immediately after
- Include: who called, summary, next steps, callback number if needed
- Use phone interactions for urgent/complex issues

**Chat** (if enabled)
- Real-time messaging with customers
- Transcript automatically attached to case
- Best for quick questions and status updates

**Portal** (Customer Self-Service)
- Customers view case status and history
- Submit updates without email
- Access knowledge articles independently

### Email Templates

Templates ensure consistent, professional communication.

**Using a Template**

1. In case Activities section, click **Customer Communication**
2. Click **Templates** dropdown
3. Select appropriate template (e.g., "Case Acknowledgment", "Request Information")
4. Template populates with case details automatically
5. Customize message as needed
6. Click **Post** to send

**Example Template Structure:**

```
Subject: Case ${number} - ${short_description}

Hello ${contact.name},

Thank you for contacting us regarding ${short_description}. 
I've reviewed your case and [your update here].

[Specific information based on template purpose]

If you have any questions, please reply to this email or 
reference case number ${number}.

Best regards,
${assigned_to.name}
${assigned_to.title}
```

### Writing Effective Customer Messages

**Message Structure Guidelines:**

1. **Greeting**: Use customer's name
2. **Acknowledgment**: Reference their specific issue
3. **Information/Update**: Provide relevant details
4. **Next Steps**: Explain what customer should expect
5. **Closing**: Offer additional help and sign off professionally

**Example Messages:**

**Initial Response:**
```
Hello Sarah,

Thank you for reaching out about the login error you're experiencing 
on our mobile app. I understand how frustrating this must be, especially 
when you're trying to access your account on the go.

I've reviewed your account and I'm investigating the cause. I'll test 
a few solutions on my end and will update you within 2 hours with 
either a fix or next steps.

In the meantime, you can access your account through our website at 
www.example.com as a temporary workaround.

Case Number: CS0012345

Best regards,
Michael Chen
Customer Support Specialist
```

**Resolution Message:**
```
Hello Sarah,

Good news! I've resolved the login issue with your mobile app. 

The problem was caused by outdated app data. Here's what I did:
1. Cleared your cached login credentials on our server
2. Reset your mobile app permissions

To log in now:
1. Close the mobile app completely (swipe up to force close)
2. Reopen the app
3. Enter your username and password
4. You should log in successfully

I tested this on our end and confirmed it's working. Please try logging 
in and let me know if you encounter any issues. If everything works 
well, this case will automatically close in 3 business days.

Thank you for your patience!

Best regards,
Michael Chen
Customer Support Specialist
```

**Requesting Information:**
```
Hello Sarah,

To help resolve your login issue, I need a bit more information:

1. What error message appears when you try to log in? (Please share the 
   exact text if possible)
2. Are you able to log in on our website, or is this issue happening 
   on both mobile and web?
3. When did you first notice this problem?

Once I have this information, I'll be able to pinpoint the cause and 
get you back into your account quickly.

Please reply to this email with the details above.

Case Number: CS0012345

Best regards,
Michael Chen
Customer Support Specialist
```

## Reporting and Analytics

Track performance and identify improvement opportunities with built-in reporting.

### Accessing Reports and Dashboards

**Personal Dashboard**

1. Navigate to **Customer Service > Dashboards > My Performance**
2. View key metrics:
   - Cases assigned to you
   - Open case count by priority
   - Average resolution time
   - Customer satisfaction scores
   - SLA compliance rate

**Team Dashboard**

1. Navigate to **Customer Service > Dashboards > Team Performance**
2. View team-wide metrics:
   - Total cases by state
   - Cases by assignment group
   - Response time trends
   - Knowledge article usage
   - Channel distribution (email, phone, chat)

### Key Performance Indicators (KPIs)

Understanding metrics helps you improve service quality. Here are some example metrics and targets to shoot for:

**First Contact Resolution (FCR)**
- Percentage of cases resolved in first interaction
- **Target**: 70% or higher
- **How to improve**: Use knowledge base, thorough initial investigation

**Average Handle Time (AHT)**
- Average time from case open to resolution
- **Target**: Varies by category (ideally 24-48 hours)
- **How to improve**: Efficient workflows, macros, knowledge articles

**Customer Satisfaction Score (CSAT)**
- Survey rating from customers (1-5 scale)
- **Target**: 4.0 or higher
- **How to improve**: Clear communication, timely updates, follow-through

### Running Reports

**Pre-Built Reports**

1. Navigate to **Reports > View/Run**
2. Search for report name
3. Click report name
4. Adjust filters if needed (date range, assignment group)
5. Click **Run**
6. View results in table or chart format

**Common Reports:**
- **Cases by Priority**: Distribution of case urgency levels
- **Cases by Category**: Volume breakdown by request type
- **Resolution Time Trends**: Average time to resolve over time periods
- **Reopened Cases**: Cases that were resolved but reopened by customer

**Exporting Reports**

For users with permission to export and scheudle reports:

1. Run the report you want to export
2. Click **Export** dropdown (top right)
3. Select format:
   - **PDF**: For sharing in meetings
   - **Excel**: For additional analysis
   - **CSV**: For importing into other systems
4. Open or save the file

**Scheduling Reports**

Send reports automatically:
1. Run desired report
2. Click **Schedule** button
3. Set frequency (Daily, Weekly, Monthly)
4. Enter recipient email addresses
5. Choose format (PDF or Excel Spreadsheet)
6. Click **Schedule**

### Using Analytics for Improvement

**Identifying Trends**

Review reports to spot patterns:
- **Spike in specific category**: May indicate product issue or need for knowledge article
- **High average handle time**: Could signal training opportunity or process inefficiency
- **Low CSAT scores**: Review customer feedback to identify service gaps

**Taking Action on Insights**

Based on reporting data:
1. **High volume in category**: Create knowledge article to deflect future cases
2. **Long resolution times**: Identify bottleneck
3. **Repeated cases from same account**: Proactive outreach to address root cause
4. **Low knowledge article usage**: Training on knowledge search techniques

---

## Quick Reference

### Field Definitions Quick Lookup

| Field | Definition |
|-------|------------|
| Contact | Person who reported the issue |
| Account | Company or organization contact belongs to |
| Assignment Group | Team responsible for resolving case |
| Priority | Importance level |
| State | Current status in case lifecycle |
| Category | Type classification for routing |
| SLA | Service level agreement with target times |
| Resolution Code | Reason case was resolved |

### Case State Quick Reference

- **New**: Just created, not yet worked
- **Open**: Currently being worked
- **Resolved**: Solution provided, customer notification sent
- **Closed**: Case complete, no further action needed

---

## Getting Help

**Support Resources**
- **ServiceNow Docs**: docs.servicenow.com
- **ServiceNow Community**: community.servicenow.com

---
