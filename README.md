# bigfix-site-webui-jgstew

BigFix Repository Site for BigFix WebUI apps and related content. Requires BigFix 11.0.7 or later.

## Structure

```none
BigFixContent/   .bes files (Fixlets, Tasks, Analyses); subfolders become digests
ServerFiles/     server-side files, such as WebUI apps (NonClientFiles)
ClientFiles/     files gathered by clients (OtherFiles)
site.xml         site-level relevance (optional)
siteConfig.xml   maps the folder names above
```

Name .bes files with a unique numeric ID prefix, such as `42- Example Task.bes`. The number becomes the Fixlet ID. Files with no ID or a duplicate ID are skipped.

## WebUI extensions

`ServerFiles/` holds WebUI extension packages (`.webui` files), such as `relevance-query.webui`. To install one:

1. Turn on Extensions Management with the WebUI server setting `_WebUIAppEnv_ENABLE_EXTENSIONS_MANAGEMENT=1`, then restart WebUI.
2. In WebUI, open **Extensions Management** and click **Install extension from file** (or **Install extension from site**).

History and docs:

- WebUI extensions were introduced in the [December 2022 WebUI release](https://forum.bigfix.com/t/bigfix-webui-new-release-available-december-2022/43756) (site "WebUI Extensions" version 1). That came out the same day as [BigFix 10.0 Patch 8](https://forum.bigfix.com/t/bigfix-10-0-patch-8-is-now-available/43749).
- "WebUI Extensions" site versions in later WebUI releases: 3 in [May 2023](https://forum.bigfix.com/t/bigfix-webui-new-release-available-may-2023/45100), 8 in [May 2024](https://forum.bigfix.com/t/bigfix-webui-new-release-available-may-2024/48647), 11 in [March 2025](https://forum.bigfix.com/t/bigfix-webui-new-release-available-march-2025/51122), 12 in [April 2025](https://forum.bigfix.com/t/bigfix-webui-new-release-available-april-2025/51420), and 14 in [April 2026](https://forum.bigfix.com/t/bigfix-webui-new-release-available-april-2026/54434).
- HCL docs: Get Started with Extensions Management ([10.0](https://help.hcl-software.com/bigfix/10.0/mcm/WebUI/Users_Guide/c_get_started_with_extension.html), [11.0](https://help.hcl-software.com/bigfix/11.0/mcm/WebUI/Users_Guide/c_get_started_with_extension.html)), [WebUI server settings](https://help.hcl-software.com/bigfix/11.0/mcm/WebUI/Admin_Guide/c_server_settings_definitions.html), and [Accessing WebUI server settings](https://help.hcl-software.com/bigfix/11.0/mcm/WebUI/Admin_Guide/c_access_webui_server_settings.html).
- Building extensions without the HCL template, plus the full SDK API list: [bigfix-content/webui_apps](https://github.com/jgstew/bigfix-content/tree/main/webui_apps).

## See also

- [BigFix Repository Sites documentation](https://help.hcl-software.com/bigfix/11.0/platform/Platform/Config/c_repository_site.html)
- [Reporting content site: bigfix-site-reporting-jgstew](https://github.com/jgstew/bigfix-site-reporting-jgstew)
- [BigFix Developer](https://developer.bigfix.com) · [BigFix Forum](https://forum.bigfix.com)
