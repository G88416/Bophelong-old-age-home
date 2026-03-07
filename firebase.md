# Firebase Deployment

## Rules and indexes
Security rules and index definitions live in the repository root:
- `firestore.rules`
- `storage.rules`
- `firestore.indexes.json`

## Deploying
Use the Firebase CLI to deploy the rules and indexes:
```
firebase deploy --only firestore:rules,firestore:indexes,storage
```
