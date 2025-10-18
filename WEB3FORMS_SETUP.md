# Web3Forms Integration Setup

This project now uses Web3Forms for handling contact form submissions and sending emails directly to your specified email addresses.

## Setup Instructions

### 1. Get Your Web3Forms Access Keys

You'll need **two separate access keys** for different email routing:

**For General Inquiry Form:**

1. Visit [Web3Forms.com](https://web3forms.com/)
2. Click "Create your Access Key"
3. Enter `info@everestsustainability.com` as the recipient email
4. Copy the access key provided

**For Quotation Request Form:**

1. Visit [Web3Forms.com](https://web3forms.com/)
2. Click "Create your Access Key"
3. Enter `nishchalbaniya@everestsustainability.com` as the recipient email
4. Copy the access key provided

### 2. Configure Environment Variables

Create a `.env.local` file in your project root directory with the following content:

**Project Structure:**

```
ESF/
├── .env.local                    ← Create this file here (project root)
├── src/
│   ├── components/
│   │   └── contact-section.tsx   ← Web3Forms integration is here
│   └── ...
├── package.json
├── README.md
└── ...
```

**Environment File Location:**
Create the `.env.local` file at the root level of your project (same level as `package.json`).

```env
# Web3Forms Configuration - Dual Access Keys
NEXT_PUBLIC_WEB3FORMS_INQUIRY_ACCESS_KEY=your_inquiry_access_key_here
NEXT_PUBLIC_WEB3FORMS_QUOTATION_ACCESS_KEY=your_quotation_access_key_here
```

Replace the placeholder values with the actual access keys you received from Web3Forms.

### 3. Email Routing

Each form uses its own Web3Forms access key to ensure proper email routing:

- **General Inquiry Form**: Uses `WEB3FORMS_INQUIRY_ACCESS_KEY` → Sends to `info@everestsustainability.com`
- **Quotation Request Form**: Uses `WEB3FORMS_QUOTATION_ACCESS_KEY` → Sends to `nishchalbaniya@everestsustainability.com`

The access keys are configured when you create them on Web3Forms.com, so each form will automatically send to the correct email address. You can modify these email addresses in the `contact-section.tsx` file if needed.

## Features

✅ **Direct Email Delivery**: Form submissions are sent directly to your email inbox
✅ **No Backend Required**: Web3Forms handles all the backend processing
✅ **Form Validation**: Built-in client-side validation
✅ **Loading States**: Shows loading indicators during submission
✅ **Success/Error Feedback**: Clear feedback messages for users
✅ **GDPR Compliant**: Web3Forms doesn't store form submissions
✅ **Customizable**: Easy to modify form fields and email routing

## How It Works

1. User fills out the contact form
2. Form data is sent to Web3Forms API
3. Web3Forms processes the data and sends an email to your specified address
4. User receives immediate feedback about the submission status

## Testing

To test the integration:

1. Make sure you've added both Web3Forms access keys to `.env.local`
2. Start your development server: `npm run dev`
3. Navigate to the contact section
4. Test both forms:
   - Fill out and submit a **General Inquiry** form → Check `info@everestsustainability.com`
   - Fill out and submit a **Quotation Request** form → Check `nishchalbaniya@everestsustainability.com`
5. Verify that each form sends emails to the correct recipient

## Troubleshooting

- **"Invalid access key" error**: Make sure both access keys are correct and properly set in `.env.local`
- **Forms not sending**: Check your internet connection and ensure both access keys are valid
- **Emails not received**: Check your spam folder and verify the recipient email addresses
- **Wrong email recipient**: Ensure each access key is configured with the correct recipient email on Web3Forms.com

For more information, visit the [Web3Forms documentation](https://docs.web3forms.com/).
