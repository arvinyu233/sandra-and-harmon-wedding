# 📧 EmailJS Setup Guide for RSVP Form

## 🚀 Quick Setup (5 minutes)

### Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Click "Sign Up" and create a free account
3. Verify your email address

### Step 2: Add Email Service
1. In your EmailJS dashboard, go to **"Email Services"**
2. Click **"Add New Service"**
3. Choose your email provider:
   - **Gmail** (recommended for personal use)
   - **Outlook/Hotmail**
   - **Yahoo**
   - **Custom SMTP**
4. Follow the setup instructions for your chosen provider
5. **Copy your Service ID** (you'll need this later)

### Step 3: Create Email Template
1. Go to **"Email Templates"**
2. Click **"Create New Template"**
3. Use this template content:

**Subject:** New RSVP Response - Sandra & Harmon Wedding

**Content:**
```
New RSVP Response for Sandra & Harmon Wedding

Guest Details:
- Name: {{name}}
- Email: {{email}}
- Number of Guests: {{guests}}
- Attendance: {{attendance_text}}
- Response Date: {{date}} at {{time}}

{{#if (eq attendance "yes")}}
🎉 Great news! They're coming to celebrate with us!
{{else}}
💙 They won't be able to make it, but we'll miss them.
{{/if}}

---
This RSVP was submitted through the wedding website.
```

4. **Copy your Template ID** (you'll need this later)

### Step 4: Get Your Public Key
1. Go to **"Account"** → **"General"**
2. **Copy your Public Key**

### Step 5: Update Your Website
Replace these placeholders in your `index.html` file:

```javascript
// Line 267: Replace YOUR_PUBLIC_KEY
emailjs.init("YOUR_PUBLIC_KEY");

// Line 297: Replace YOUR_SERVICE_ID and YOUR_TEMPLATE_ID
emailjs.send('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', formData)
```

**Example:**
```javascript
emailjs.init("user_abc123def456");
emailjs.send('service_gmail', 'template_rsvp', formData)
```

## 🎯 What You'll Receive

When someone submits an RSVP, you'll get an email with:
- ✅ Guest's full name
- ✅ Email address
- ✅ Number of guests
- ✅ Attendance decision (Yes/No)
- ✅ Date and time of response
- ✅ Appropriate emoji based on their response

## 🔧 Alternative Solutions

### Option 1: Formspree (Even Easier)
1. Go to [https://formspree.io/](https://formspree.io/)
2. Create account and get your form endpoint
3. Replace the form action with your Formspree URL

### Option 2: Netlify Forms (If hosting on Netlify)
1. Add `netlify` attribute to your form
2. Deploy to Netlify
3. Forms are automatically handled

### Option 3: Google Forms (Simplest)
1. Create a Google Form
2. Embed it in your website
3. Responses go to Google Sheets

## 🆓 Free Limits

**EmailJS Free Plan:**
- 200 emails per month
- Perfect for wedding RSVPs

**Formspree Free Plan:**
- 50 submissions per month
- Good for smaller weddings

## 🚨 Important Notes

1. **Test the form** before going live
2. **Check spam folder** for test emails
3. **Keep your keys secure** - don't share them publicly
4. **Monitor your email limits** to avoid hitting the free tier limits

## 🎉 You're All Set!

Once configured, your RSVP form will:
- ✅ Send emails directly to your inbox
- ✅ Show loading states and success messages
- ✅ Handle errors gracefully
- ✅ Reset automatically after submission
- ✅ Work on any device

Need help? Check the EmailJS documentation or contact support!
