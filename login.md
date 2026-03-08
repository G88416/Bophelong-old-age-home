# Login Details

This portal uses Firebase email/password authentication. **There are no default
credentials stored in this repository.**

## How to sign in
1. Open `index.html` in a browser (or the deployed site).
2. Enter the email address and password provided by your administrator.
3. Click **Sign In**.

## First-time admin setup (temporary login)
If no admin accounts exist yet, use the **Create demo admin account** button on the login screen.

This repository now ships with a temporary demo setup code:

- **Demo setup code:** `BophelongDemoAdmin2026`

Anyone with access to the HTML source can see the code, so rotate it immediately after setup and
only use this flow in a trusted environment.
1. Open **Create demo admin account**.
2. Enter your name, email address, password, and the demo setup code above.
3. Create the temporary admin and sign in.
4. Create your permanent admin from **Staff & Users**.
5. Change `BOOTSTRAP_CODE` in `index.html`, update `bootstrapCode()` in `firestore.rules` to match,
   and deploy the rules (`firebase deploy --only firestore:rules`).

Then use the setup form to create your first admin user. The app stores a one-time
lock in `config/bootstrap` so additional bootstrap admins cannot be created. After you
create permanent users, change the bootstrap code again (or remove the setup path) and
redeploy the rules. If you ever need to rerun setup, delete `config/bootstrap` in the
Firebase console and deploy with a new code.

## Need an account?
Ask an administrator to create a user account from the **Staff & Users** section
inside the portal. The admin must supply you with:
- Your email address
- Your temporary or permanent password (minimum 8 characters)

If your account is inactive or you cannot sign in, contact your administrator to
activate or reset your access.
