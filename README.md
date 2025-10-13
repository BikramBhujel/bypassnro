# Windows Setup Bypass 🚀

**Tired of the Microsoft Account / Network required prompts during Windows OOBE?**

This repository provides a script that automates parts of the Windows Out-of-Box Experience (OOBE). It helps streamline initial setup by handling network prompts, skipping privacy screens, creating local accounts defined in an `unattend.xml`, and removing selected pre-installed applications.

> ⚠️ **Disclaimer & Safety**
>
> This project is intended to help system administrators and advanced users automate legitimate Windows deployments. Use it only on systems you own or are authorized to manage. Bypassing security controls or licensing requirements on devices you don't control may be illegal or violate terms of service. The author and contributors are not responsible for misuse.

---

## Features

* Automates portions of the Windows OOBE flow
* Skips network/online-account prompts where possible
* Applies local accounts from a provided `unattend.xml`
* Removes common pre-installed (OEM) applications (bloat)

---

## Requirements

* A Windows machine at the initial OOBE screen (before user account setup)
* Network access to download the script (or copy it locally to removable media)
* Administrative access in the Command Prompt opened from OOBE

---

## How to Use

1. When you reach the **initial OOBE screen** (the screen that asks for region and/or network), open a Command Prompt by pressing:

```
Shift + F10
```

2. From the Command Prompt, download the script. Example using `curl`:

```powershell
curl -L bikrambhujel.com.np/bypass -o skip.cmd
```

3. Run the downloaded script:

```powershell
skip.cmd
```

> If your environment restricts `curl`, you may copy the script to a USB drive and run it from there instead.

---

## Unattend.xml

If you want the script to create local accounts automatically, include an `unattend.xml` file configured with the desired local account information and place it where the script expects it (or modify the script to point to your `unattend.xml`). Ensure credentials and account details are handled securely.

---

## Troubleshooting

* If the download fails, make sure the machine has network access or use removable media.
* If the script does not run, confirm you opened an elevated Command Prompt from OOBE (Shift + F10) and that execution policies or Windows restrictions are not blocking script execution.
* Test on a controlled lab machine before using in production.

---

## Contributing

Contributions, issues, and feature requests are welcome. If submitting changes:

1. Open an issue describing the problem or feature.
2. Submit a clear pull request with a description of changes and the testing performed.

Please do not submit or request assistance for bypassing licensing or other protections that are illegal or unethical.

---

## Notes

* Always validate scripts from the internet before running them.
* Keep backups of data and system images before performing automated setup changes.

---

*Made with care — use responsibly.*
