## Volcengine Mem0 Memory Plugin - Installed

**Next steps:**

1. **Set credentials** (if not prompted above):
   Add to `~/.hermes/.env`:
   ```
   VOLCENGINE_MEM0_API_KEY=your-api-key
   VOLCENGINE_MEM0_HOST=https://your-host:8000
   ```

2. **Activate the provider:**
   ```bash
   hermes plugins
   ```
   Go to **Provider Plugins > Memory Provider** and select `volcengine_mem0`.

3. **Verify:**
   ```bash
   hermes memory setup
   ```

4. **Restart gateway** (if using messaging platforms):
   ```bash
   hermes gateway restart
   ```

Tools available after activation: `volcmem0_search`, `volcmem0_conclude`, `volcmem0_profile`
