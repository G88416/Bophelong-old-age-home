# Login Details

This portal uses Firebase email/password authentication. **There are no default
credentials stored in this repository.**

## How to sign in
1. Open `index.html` in a browser (or the deployed site).
2. Enter the email address and password provided by your administrator.
3. Click **Sign In**.

## First-time admin setup (temporary login)
If no admin accounts exist yet, use the **Create demo admin account** button on the login screen.

This build ships with a temporary setup code already configured so the bootstrap flow works out of
the box. Anyone with access to the HTML source can see that code, so rotate it immediately after
setup and only use this flow in a trusted environment.
1. Open **Create demo admin account**.
2. Enter your name, email address, password, and the temporary setup code configured for this build.
3. Create the temporary admin and sign in.
4. Create your permanent admin from **Staff & Users**.
5. Change `BOOTSTRAP_CODE` in `index.html`, update `bootstrapCode()` in `firestore.rules` to match,
   and deploy the rules (`firebase deploy --only firestore:rules`).

The app stores a one-time lock in `config/bootstrap` so additional bootstrap admins
cannot be created. The temporary bootstrap admin is allowed to write that lock during
first-time setup, but only when its profile still carries the matching bootstrap code.
After you create your permanent admin, change the bootstrap code
again (or remove the setup path) and redeploy the rules. If you ever need to rerun
setup, delete `config/bootstrap` in the Firebase console and deploy with a new code.

## Need an account?
Ask an administrator to create a user account from the **Staff & Users** section
inside the portal. The admin must supply you with:
- Your email address
- Your temporary or permanent password (minimum 8 characters)

If your account is inactive or you cannot sign in, contact your administrator to
activate or reset your access.
