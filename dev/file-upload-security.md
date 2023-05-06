*For web frontends accepting files from users*

---

The most concerning attack vectors available to bad actors are Filename, Metadata, and Content. And the most common attack is typically a cross-site-script (XSS).

To defend against XSS and other malicious intent, we should always ensure the following:
- **Name sanitation**: Rename the user-submitted file before doing anything with it (i.e `POST` to a backend).
- **Extension whitelisting**: Use the `accept` attribute on your `<input>` elements in order to explicitly specify which MIME types may be uploaded.
- **Metadata validation**: Whenever possible, check and confirm the meta attributes of the file match what is expected. If something looks off, reject the upload:
  - Size
  - MIME-type
  - Last Modified Date

Regarding the file ***Content***, our options for thwarting bad actors are more limited and will depend on the accepted MIME types and the general purpose of the upload. One important point to be aware of is that `image` files are more high-risk given the fact that they can embed scripts.

### References & Further Reading

1. [OWASP: File Upload Protection](https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html#file-upload-protection)
2. [BruteLogic: File Upload XSS](https://brutelogic.com.br/blog/file-upload-xss/)
3. [FileReader API](https://developer.mozilla.org/en-US/docs/Web/API/FileReader)
