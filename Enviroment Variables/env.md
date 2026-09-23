## What are Environment Variables?

---

**Environment variables** are variables used to store configuration values outside the source code.

They are commonly used for sensitive or environment-specific information such as:

- Database URL
- API keys
- JWT secret
- Port number
- Passwords

### Simple Example

Create a `.env` file:

```env
PORT=5000
DB_URL=mongodb://localhost:27017/mydb
JWT_SECRET=mysecret123