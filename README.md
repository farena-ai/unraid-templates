# Unraid templates (Backstage Coding)

[Community Applications](https://docs.unraid.net/community-applications/) templates for Unraid.

| Template | App |
|---|---|
| [`templates/sara.xml`](templates/sara.xml) | [Sara](https://github.com/farena-ai/sara), a self-hosted AI companion and coding partner (image `ghcr.io/farena-ai/sara`, linux/amd64 and linux/arm64) |

## Sara on Unraid

1. *Apps* → search **Sara** → *Install*. Keep the data path (`/mnt/user/appdata/sara`) or pick your own.
2. Open the WebUI within an hour of the first start. Sara asks for an 8-character **setup code**:
   click Sara's icon on the *Docker* tab → *Logs* and look for "setup code". She then shows your
   owner token once; keep it in your password manager. Missed the hour? Restart the container for
   a new code.
3. Add an AI model in Sara's Settings (Ollama in another container, or your own provider account).

Plain HTTP is fine on your home network. For access from outside, put an HTTPS reverse proxy in
front and set *Secure cookies* and *Trust proxy* to 1 (advanced view).

The template is made in Sara's own repository (`packaging/unraid/sara.xml`) and copied here at
each change. Support: https://github.com/farena-ai/sara/issues
