# Login Details

This portal uses Firebase email/password authentication. **There are no default
credentials stored in this repository.**

## How to sign in
1. Open `index.html` in a browser (or the deployed site).
2. Enter the email address and password provided by your administrator.
3. Click **Sign In**.

## First-time admin setup (temporary login)
If no admin accounts exist yet, use the **First-time setup: Create admin** button on the login screen.

Before using it, **set a private bootstrap code** and deploy matching Firestore rules:
1. Update `BOOTSTRAP_CODE` in `index.html` to a private code (the default is blank).
2. Update `bootstrapCode()` in `firestore.rules` to the same value.
3. Deploy the rules (`firebase deploy --only firestore:rules`).

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
