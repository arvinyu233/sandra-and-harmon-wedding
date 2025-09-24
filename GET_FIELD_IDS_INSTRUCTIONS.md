# 🔍 How to Get Google Form Field IDs

## 📋 Step-by-Step Instructions:

### Step 1: Open Your Form in Edit Mode
1. Go to your Google Form: https://docs.google.com/forms/d/e/1FAIpQLSen6cQc5eLPjLnEKOaLcztdfaStOCr_5bTKlixXAkNNs27xBg/viewform
2. Click the **pencil icon** (✏️) in the top-right to edit the form

### Step 2: Get Field IDs
1. **Right-click** on the first field ("First & Last Name")
2. Select **"Inspect"** or **"Inspect Element"**
3. Look for a line that contains: `name="entry.XXXXXXXXX"`
4. **Copy the entry number** (the XXXXXXXXX part)

### Step 3: Repeat for Each Field
Do this for all 4 fields:
- **Field 1:** First & Last Name → `entry.XXXXXXXXX`
- **Field 2:** Email Address → `entry.XXXXXXXXX`  
- **Field 3:** Number of Guests → `entry.XXXXXXXXX`
- **Field 4:** Will you be attending? → `entry.XXXXXXXXX`

### Step 4: Alternative Method (Easier)
1. Go to your form: https://docs.google.com/forms/d/e/1FAIpQLSen6cQc5eLPjLnEKOaLcztdfaStOCr_5bTKlixXAkNNs27xBg/viewform
2. Press **F12** to open Developer Tools
3. Click the **"Elements"** tab
4. Press **Ctrl+F** and search for `entry.`
5. You'll see all the field IDs listed

## 📝 What You're Looking For:
```html
<input type="text" name="entry.1234567890" ...>  <!-- Name field -->
<input type="email" name="entry.0987654321" ...>  <!-- Email field -->
<select name="entry.1122334455" ...>              <!-- Guests field -->
<input type="radio" name="entry.5566778899" ...>  <!-- Attendance field -->
```

## 🎯 Once You Have the IDs:
Send me the 4 entry numbers and I'll update your website immediately!

Example format:
- Name field: entry.1234567890
- Email field: entry.0987654321
- Guests field: entry.1122334455
- Attendance field: entry.5566778899
