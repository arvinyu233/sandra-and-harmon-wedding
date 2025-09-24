# 🔍 Detailed Guide to Find All Field IDs

## 📋 Step-by-Step Instructions:

### Method 1: Complete HTML Source Search
1. Go to your Google Form: https://docs.google.com/forms/d/e/1FAIpQLSen6cQc5eLPjLnEKOaLcztdfaStOCr_5bTKlixXAkNNs27xBg/viewform
2. Press **F12** to open Developer Tools
3. Click the **"Elements"** tab
4. Press **Ctrl+A** to select all the HTML
5. Press **Ctrl+C** to copy all HTML
6. Open a text editor (Notepad) and paste it
7. Press **Ctrl+F** and search for `entry.`
8. You should see ALL field IDs listed

### Method 2: Form Response URL Method
1. Go to your Google Form
2. Right-click on the form and select **"Inspect"**
3. In the Elements tab, press **Ctrl+F** and search for `formResponse`
4. Look for the form action URL
5. The field IDs are usually listed in the HTML around that area

### Method 3: Network Tab Method
1. Open Developer Tools (F12)
2. Go to **"Network"** tab
3. Fill out your form with test data
4. Click Submit
5. Look for the form submission request
6. The field IDs will be in the request data

### Method 4: Alternative - Use Form Embed Code
1. Go to your Google Form
2. Click **"Send"** button
3. Click **"<>"** (embed) icon
4. Copy the embed code
5. The field IDs are in the iframe src URL

## 🎯 What You're Looking For:
You should find 4 different entry numbers:
- `entry.671845706` (Name - already found)
- `entry.2055545111` (Email - already found)
- `entry.XXXXXXXXX` (Guests - need this one)
- `entry.XXXXXXXXX` (Attendance - need this one)

## 📝 If You Still Can't Find Them:
Let me know and I can help you with an alternative approach using the embed method or we can test the form with just the 2 field IDs you have to see what happens.
