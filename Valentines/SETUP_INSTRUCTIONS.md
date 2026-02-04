# Valentine's Day Page - Setup Instructions

## 📧 Email Notification Setup

To receive an email when she clicks "Yes", follow these steps:

### Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Sign up for a free account (100 emails/month free)

### Step 2: Add Email Service
1. Go to "Email Services" in your dashboard
2. Click "Add New Service"
3. Choose your email provider (Gmail recommended)
4. Connect your email account
5. Copy the **Service ID** (e.g., `service_abc123`)

### Step 3: Create Email Template
1. Go to "Email Templates"
2. Click "Create New Template"
3. Use this template:

**Subject:** `{{subject}}`

**Content:**
```
Hi {{to_name}},

{{message}}

Best regards,
Your Valentine's Day Page
```

4. Save and copy the **Template ID** (e.g., `template_xyz789`)

### Step 4: Get Public Key
1. Go to "Account" → "General"
2. Copy your **Public Key** (e.g., `abcdefghijklmnop`)

### Step 5: Update the HTML File
1. Open `Valentines.html` in a text editor
2. Find the `sendEmailNotification()` function (around line 883)
3. Replace these three values:
   - `YOUR_SERVICE_ID` → Your Service ID
   - `YOUR_TEMPLATE_ID` → Your Template ID
   - `YOUR_PUBLIC_KEY` → Your Public Key

Example:
```javascript
const serviceID = 'service_abc123';
const templateID = 'template_xyz789';
const publicKey = 'abcdefghijklmnop';
```

## 🌐 How to Share with Her

### Option 1: GitHub Pages (Free & Easy)
1. Create a GitHub account at https://github.com
2. Create a new repository
3. Upload `Valentines.html` to the repository
4. Go to Settings → Pages
5. Select "main" branch and save
6. Your page will be at: `https://yourusername.github.io/repository-name/Valentines.html`
7. Share this link with her!

### Option 2: Netlify (Free & Super Easy)
1. Go to https://www.netlify.com/
2. Sign up for free
3. Drag and drop your `Valentines.html` file
4. Get your link instantly (e.g., `https://random-name-123.netlify.app/Valentines.html`)
5. Share the link!

### Option 3: Vercel (Free)
1. Go to https://vercel.com/
2. Sign up
3. Upload your HTML file
4. Get your link and share!

### Option 4: Google Drive (Simple but limited)
1. Upload `Valentines.html` to Google Drive
2. Right-click → Share → Get link
3. Change access to "Anyone with the link"
4. Copy the link and share (she'll need to download and open it)

## 📸 Adding Your Photo

1. Replace the placeholder image URL in the HTML
2. Find this line (around line 814):
   ```html
   <img src="https://picsum.photos/500/400?random=1" ...>
   ```
3. Replace with your photo:
   - Option A: Upload to Imgur, get direct link
   - Option B: Upload to your hosting service with the HTML file
   - Option C: Use a service like Cloudinary

Example:
```html
<img src="https://i.imgur.com/your-image-id.jpg" ...>
```

## ✅ Testing

1. Open the HTML file in your browser
2. Click "Yes" to test
3. Check your email (christopherahh6@gmail.com)
4. If email doesn't arrive, check the browser console (F12) for errors

## 🎉 You're All Set!

Once everything is configured and hosted, share the link with her and wait for that "YES" notification! 💕

