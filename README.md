# Edge Sidebar Not Working

**Issue:**
The Bing Image Creator is not showing in the Edge sidebar, nor in the "Plus" or "Apps" sections.

**Cause:**
This issue occurs because Microsoft Edge on Linux is missing the `HubApps` file.

**On Windows:**
The `HubApps` file is typically located at:

```
C:\Users\<username>\AppData\Local\Microsoft\Edge\User
```

**On Linux (Ubuntu):**
You need to manually create or copy the `HubApps` file to the following directory:

```
~/.config/microsoft-edge/Default/
```

**Solution:**

1. Copy the `HubApps` file from a valid source (e.g., from a Windows machine or a shared repository):

   ```bash
   cp /path/to/HubApps ~/.config/microsoft-edge/Default/
   ```
2. Set the correct file permissions:

   ```bash
   chmod 644 ~/.config/microsoft-edge/Default/HubApps
   ```
3. Restart Microsoft Edge.

---