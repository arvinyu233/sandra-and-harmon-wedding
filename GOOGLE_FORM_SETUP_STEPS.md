# 🔧 Google Form Setup Steps

## 📝 Current Status
Your Google Form at https://docs.google.com/forms/d/e/1FAIpQLSen6cQc5eLPjLnEKOaLcztdfaStOCr_5bTKlixXAkNNs27xBg/viewform currently only has the attendance question.

## ✅ What You Need To Do:

### Step 1: Add Missing Fields to Your Google Form
1. Go to your Google Form: https://docs.google.com/forms/d/e/1FAIpQLSen6cQc5eLPjLnEKOaLcztdfaStOCr_5bTKlixXAkNNs27xBg/viewform
2. Click the **pencil icon** to edit the form
3. Add these fields **BEFORE** the attendance question:

#### Field 1: Name
- Click **"+"** to add question
- **Type:** Short answer
- **Question:** "First & Last Name"
- **Required:** ✅ Yes

#### Field 2: Email
- Click **"+"** to add question  
- **Type:** Short answer
- **Question:** "Email Address"
- **Required:** ✅ Yes

#### Field 3: Number of Guests
- Click **"+"** to add question
- **Type:** Multiple choice
- **Question:** "Number of Guests"
- **Options:**
  - 1 Guest
  - 2 Guests
  - 3 Guests
  - 4 Guests
  - 5+ Guests
- **Required:** ✅ Yes

### Step 2: Update Attendance Question
- Change the current question from "Will you be attending??" to "Will you be attending?"
- Update options to:
  - Will Attend
  - Regretfully Declines

### Step 3: Get Field IDs
1. **Save** your form
2. **Right-click** on the form and select **"Inspect"** or press **F12**
3. Look for the input fields and find the `name` attributes like:
   - `name="entry.1234567890"` (for name field)
   - `name="entry.0987654321"` (for email field)
   - `name="entry.1122334455"` (for guests field)
   - `name="entry.5566778899"` (for attendance field)

### Step 4: Update Your Website
Replace the `entry.XXXXXXXXX` placeholders in your `index.html` with the actual field IDs you found.

## 🎯 Final Form Order Should Be:
1. First & Last Name
2. Email Address  
3. Number of Guests
4. Will you be attending?

## 📧 What You'll Receive:
Each RSVP will include all the information in a Google Sheet with email notifications!
