# Login Details

This portal uses Firebase email/password authentication. **There are no default
credentials stored in this repository.**

## How to sign in
1. Open `index.html` in a browser (or the deployed site).
2. Enter the email address and password provided by your administrator.
3. Click **Sign In**.

## First-time admin setup
If no admin account exists yet, the app opens on a **Create Your Permanent Admin Account** screen.

1. Enter your name, email address, department, and password.
2. Submit the form to create the permanent admin account.
3. The app signs you in automatically and locks first-time setup.

The app stores a one-time lock in `config/bootstrap` so the first-run admin form is only available
until the first permanent admin is created. If you ever need to rerun setup, delete
`config/bootstrap` in the Firebase console and deploy the updated Firestore rules if needed.

## Need an account?
Ask an administrator to create a user account from the **Staff & Users** section
inside the portal. The admin must supply you with:
- Your email address
- Your temporary or permanent password (minimum 8 characters)

If your account is inactive or you cannot sign in, contact your administrator to
activate or reset your access.
