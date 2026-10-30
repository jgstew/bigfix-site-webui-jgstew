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

## See also

- [BigFix Repository Sites documentation](https://help.hcl-software.com/bigfix/11.0/platform/Platform/Config/c_repository_site.html)
- [Reporting content site: bigfix-site-reporting-jgstew](https://github.com/jgstew/bigfix-site-reporting-jgstew)
- [BigFix Developer](https://developer.bigfix.com) · [BigFix Forum](https://forum.bigfix.com)
