# Google Analytics Event Tracking Guide

Your website now tracks comprehensive user interactions. Here's what's being monitored:

## Main Page (index.html) Events

### Navigation Events
- **Event Name:** `navigation_click`
- **Parameters:** section, link_text
- **Triggered by:** Clicking any navigation link (Home, About, Skills, Experience, Wins, Recs, Contact)
- **Use case:** Track which sections users visit most

### Download Events
- **Event Name:** `download_cv`
- **Parameters:** file_name, file_type
- **Triggered by:** Clicking "Download CV" button
- **Use case:** Track resume downloads

### Social Media Events
- **Event Name:** `social_click`
- **Parameters:** platform (LinkedIn, GitHub, Email), url
- **Triggered by:** Clicking LinkedIn, GitHub, or Email social links
- **Use case:** Track external profile visits

### Skill Filter Events
- **Event Name:** `skill_filter_click`
- **Parameters:** category, button_text
- **Triggered by:** Clicking skill category filter buttons (All, Automation, API Testing, CI/CD, etc.)
- **Use case:** Track which skills users are most interested in

### Theme Toggle Events
- **Event Name:** `theme_toggle`
- **Parameters:** theme (light or dark)
- **Triggered by:** Clicking the theme toggle button
- **Use case:** Track user theme preferences

### Back to Top Events
- **Event Name:** `back_to_top_click`
- **Parameters:** timestamp
- **Triggered by:** Clicking back to top button
- **Use case:** Track page depth and scroll patterns

### Contact Form Events
- **Event Name:** `contact_form_submit`
- **Parameters:** form_name, message_length, timestamp
- **Triggered by:** Submitting the contact form
- **Use case:** Track contact form submissions
- **Privacy:** Only message length is tracked, not message content

### View Work Events
- **Event Name:** `view_work_click`
- **Parameters:** button_text, target_section
- **Triggered by:** Clicking "View My Work" button
- **Use case:** Track interest in work section

### Scroll Depth Events
- **Event Name:** `scroll_depth`
- **Parameters:** depth_percent (25, 50, 75, 100)
- **Triggered by:** Scrolling down the page
- **Use case:** Track engagement depth

### Page Visibility Events
- **Event Name:** `page_hidden` / `page_visible`
- **Parameters:** timestamp
- **Triggered by:** User leaves/returns to tab
- **Use case:** Track tab focus and engagement

### Time on Page Events
- **Event Name:** `time_on_page`
- **Parameters:** seconds (tracked every 5 minutes)
- **Triggered by:** Automatic tracking
- **Use case:** Measure average session duration

---

## Contact Page (contactme.html) Events

### Phone Call Events (Mobile Only)
- **Event Name:** `phone_call_click`
- **Parameters:** device_type, phone_masked
- **Triggered by:** Clicking the masked phone number on mobile devices
- **Use case:** Track phone inquiries
- **Privacy:** Number is masked (+91-960XXXXX13)

### Email Events
- **Event Name:** `email_click`
- **Parameters:** email_masked, action
- **Triggered by:** Clicking the email link
- **Use case:** Track email inquiries
- **Privacy:** Email is masked

### Page View Events
- **Event Name:** `page_view`
- **Parameters:** page_title, page_location
- **Triggered by:** Loading the contact page
- **Use case:** Track page visits

---

## Input Form Page (input.html) Events

### Form Field Events
- **Event Name:** `form_field_focus`
- **Parameters:** field_type, form_name
- **Triggered by:** User focuses on form field
- **Use case:** Track form interaction

### Form Field Change Events
- **Event Name:** `form_field_change`
- **Parameters:** field_type, form_name
- **Triggered by:** User changes form field value
- **Use case:** Track field engagement

### Form Submit Events
- **Event Name:** `form_submit`
- **Parameters:** form_name, form_action, timestamp
- **Triggered by:** User submits the form
- **Use case:** Track form submissions

### Page View Events
- **Event Name:** `page_view`
- **Parameters:** page_title, page_location
- **Triggered by:** Loading the form page
- **Use case:** Track page visits

---

## How to View Events in Google Analytics

### Step 1: Open Google Analytics
1. Go to [Google Analytics](https://analytics.google.com)
2. Select your property: **VigneshR32.github.io**
3. Click on **Reports** (left sidebar)

### Step 2: View Events
1. Go to **Reports** → **Events**
2. You'll see all events listed with:
   - Event name
   - Event count
   - Conversion rate
   - Parameters

### Step 3: Drill Down into Specific Events
1. Click on any event to see details
2. View breakdown by:
   - Date
   - Event parameters
   - User segments
   - Geographic location
   - Device type

### Step 4: Create Custom Reports
1. Go to **Explore** → **New Exploration**
2. Create custom reports with:
   - Event dimensions: event_name, section, platform, category
   - Metrics: event_count, engaged_sessions, conversion_rate

### Step 5: Set Up Alerts
1. Go to **Admin** → **Alerts**
2. Create alerts for:
   - High download CV activity
   - Contact form submissions
   - Traffic spikes

---

## Key Metrics to Monitor

| Metric | Purpose | Tracked By |
|--------|---------|-----------|
| Most clicked section | Measure interest | navigation_click |
| Resume downloads | Track recruitment interest | download_cv |
| Social profile visits | Track social presence | social_click |
| Contact inquiries | Track lead generation | contact_form_submit, phone_call_click, email_click |
| Scroll depth | Measure page engagement | scroll_depth |
| Time on page | Measure interest level | time_on_page |
| Form submissions | Track form effectiveness | form_submit |
| Skill interest | Track skill relevance | skill_filter_click |

---

## Privacy & Data Protection

✓ **Phone number masked** in events  
✓ **Email masked** in events  
✓ **No form content stored** (only metrics)  
✓ **No personally identifiable information** collected  
✓ **All tracking respects user privacy settings**  
✓ **Compliant with GDPR standards**

---

## Testing Events

To verify events are working:

1. Open your website
2. Open **Browser DevTools** (F12 or Cmd+Option+I)
3. Go to **Console**
4. Click any interactive element
5. Look for events logged in **Google Analytics Real-time** report

The event should appear within 1-3 seconds in Google Analytics Real-time view.

---

## Customization

To add more events or modify existing ones, edit the event tracking script in the respective HTML file and update the `gtag('event', 'event_name', { parameters })` calls.

For questions or to add new event tracking, refer to the [Google Analytics 4 Event Documentation](https://developers.google.com/analytics/devguides/collection/ga4/events).
