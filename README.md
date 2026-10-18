# JWT Verification API

Deploy on Render using the included `render.yaml` Blueprint.

- `POST /verify` accepts `{"token":"<JWT>"}`
- Validates RS256 signature, issuer, audience, expiration, and required claims.
- Valid token returns `valid`, `email`, `sub`, and `aud`.
- Invalid token returns HTTP 401.

Local test:
```bash
pip install -r requirements.txt
uvicorn main:app --reload
```
