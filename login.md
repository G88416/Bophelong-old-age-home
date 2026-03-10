# Login Details

This portal uses Firebase email/password authentication.

## How to sign in
1. Open `index.html` in a browser (or the deployed site).
2. Enter the email address and password provided by your administrator.
3. Click **Sign In**.

Any valid Firebase email/password account can now sign in even if a matching
Firestore profile is missing or marked inactive. In those cases the portal opens
with standard staff access until an administrator assigns an active role profile.

The configured permanent admin account (`admin@oldage.com`) is the exception: it
always opens the admin workspace after sign-in so the main admin can recover
access even if the matching Firestore profile still needs to be synchronized.

## Need an account?
Ask an administrator to create a user account from the **Users** section
inside the portal. The admin must supply you with:
- Your email address
- Your temporary or permanent password (minimum 8 characters)

If you cannot sign in because of your email or password, contact your
administrator to reset your access.
