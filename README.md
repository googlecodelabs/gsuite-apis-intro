# Google Workspace APIs Intro codelab

This codelab introduces developers to Google Workspace ([formerly G Suite](https://cloud.google.com/blog/products/workspace/introducing-google-workspace)) APIs (Gmail, Google Drive, Calendar, Sheets, Slides, etc.) by writing a simple Python script that lists the first 100 files/folders in a user's Google Drive. Access it at http://g.co/codelabs/gsuite-apis-intro.

## Prerequisites

- A Google account (Google Workspace accounts may require administrator approval)
- Familiarity with shell commands on POSIX-compliant systems (Linux, Mac OS X); [Windows users](http://docs.python.org/faq/windows) also welcome
- Ability to create source files with either a code editor or shell commands.
- Basic skills in [Python](http://python.org) (2 or 3), but you use [any supported language](http://developers.google.com/api-client-library)
- Some files and/or folders in your [Google Drive](http://drive.google.com)

## Description

This repo is part of the [codelab](http://g.co/codelabs/gsuite-apis-intro) introducing developers to using Google Workspace (REST/HTTP) APIs. The example will be done in Python for brevity and wide availability, but [all common languages are supported](http://developers.google.com/api-client-library). The tutorial shows how to use the developer console to create and manage projects, including obtaining the credentials needed in your apps, then moves on to the primary code sample that displays the first 100 files & folders in your Google Drive by using the Drive API.

### Caveat

**`oauth2client` library deprecated**:
The [`oauth2client`](https://github.com/googleapis/oauth2client) library was [deprecated](https://google-auth.readthedocs.io/en/latest/oauth2client-deprecation.html) in [2017](https://github.com/googleapis/oauth2client/commit/00926f2058e23da7f6772ad6477e64d7506415e5) in favor of newer replacements. However the newer libraries [do not yet support](https://google-auth.readthedocs.io/en/latest/oauth2client-deprecation.html#replacement) either user authorization nor user credentials storage, two features that are required in this codelab. When those features become available, we will migrate to the newer libraries. For now, `oauth2client` still works, even in maintenance mode, and provides automated, threadsafe, and 2.x/3.x-compatible storage of and access to OAuth2 tokens for users whereas the newer libraries do not (yet).

### Cost

Use of the Google Drive API (and most Google Workspace APIs) are covered by a [monthly subscription fee](http://gsuite.google.com/pricing.html), including the free consumer Google/Gmail accounts (monthly fee of $0USD), meaning you can use the APIs as long as you stay within each API's daily/monthly limits. Exceeding the limits will result in failed requests/exceptions. Some APIs have a [support page to request additional quota](https://developers.google.com/drive/api/v3/handle-errors#quota).

## Repo files

Filename | Description
--- | ---
`drive_list.py` | The original sample app as featured in codelab
`drive_list-new.py` | Same as `drive_list.py` but uses newer auth libraries (not threadsafe nor easily Python 2-3 compatible nor handles auth tokens [extra JSON storage code])

## Support

- [Codelab to build code sample](https://g.co/codelabs/gsuite-apis-intro)
- [Code deep dive blogpost](https://goo.gl/cdm3kZ)
- [Code deep dive video](https://goo.gl/ZIgf8k)
- [Google Drive API home page](https://developers.google.com/drive)
- [Other Google Drive API videos](https://developers.google.com/drive/api/v3/videos)
- [Google Workspace REST APIs intro video](https://goo.gle/3ateIIQ)
- [Google Workspace REST APIs "world tour" video](https://youtu.be/kkp0aNGlynw)
- [Drive Service on Apps Script](https://developers.google.com/apps-script/reference/drive)
- [Advanced Drive Service on Apps Script](https://developers.google.com/apps-script/advanced/drive)
- [Google Workspace developers home page](https://developers.google.com/workspace)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/google-drive-sdk)

If you've found an error in the codelab or the sample app, check the [Issues](https://github.com/googlecodelabs/gsuite-apis-intro/issues) tab to see if there's an open issue or file a new one. Patches are encouraged; please refer to [CONTRIBUTING](CONTRIBUTING.md) for details.
