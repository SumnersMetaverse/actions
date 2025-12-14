# Developer Credentials for Miagos Vault

This file (`developer-credentials.json`) is used to store developer credentials for integration with Miagos vault.

## Structure

The credentials file contains:
- **version**: Version of the credentials schema
- **description**: Description of the file's purpose
- **developers**: Array of developer credential objects

### Developer Object Fields

Each developer entry includes:
- `id`: Unique identifier for the developer
- `name`: Developer's full name
- `email`: Developer's email address
- `role`: Developer's role (e.g., "Developer", "Admin", "Contributor")
- `access_level`: Access level (e.g., "standard", "elevated", "admin")
- `credentials`: Object containing API keys and secrets
  - `api_key`: API key for authentication
  - `secret_key`: Secret key for secure operations
- `created_at`: Timestamp when the credentials were created
- `status`: Current status (e.g., "active", "inactive", "suspended")

## Usage

1. Add your developer credentials to the `developers` array in `developer-credentials.json`
2. Replace placeholder values (`YOUR_API_KEY_HERE`, etc.) with actual credentials
3. Ensure the file is properly secured and not committed with real credentials if sensitive
4. Use this file for Miagos vault integration to manage and store credentials securely

## Security Notes

⚠️ **Important**: 
- Never commit actual API keys or sensitive credentials to version control
- Use environment variables or secure vault systems for production credentials
- This template file contains placeholder values that should be replaced with actual credentials only in secure environments
- Consider adding `developer-credentials.json` to `.gitignore` if it will contain sensitive data

## Adding a New Developer

To add a new developer:

```json
{
  "id": "dev-002",
  "name": "New Developer Name",
  "email": "newdev@example.com",
  "role": "Developer",
  "access_level": "standard",
  "credentials": {
    "api_key": "YOUR_API_KEY_HERE",
    "secret_key": "YOUR_SECRET_KEY_HERE"
  },
  "created_at": "2025-12-14T22:27:36.463Z",
  "status": "active"
}
```

Add this object to the `developers` array in the main JSON file.
