# Siberian CLI Documentation

[Edit this on Github](https://github.com/Xtraball/SiberianCMS-Doc/edit/master/docs/cli/siberian.md)

## Introduction

Siberian ships with a CLI to help debugging & troubleshooting.

## CLI available methods

|Method|Min. version|Params|Description|
|------|------------|------|-----------|
|export-schemas|4.13.10|-|Exports the current schema tables (only schemas) to `var/schema/CURRENT_VERSION/TABLE.php` this is useful to prepare db files for your custom modules|
|export-database|4.13.10|-|Exports the current mysql database|
|version|4.13.10|version|Updates `lib/Siberian/Version.php` with the given version|
|user:create|4.13.10|-|This action will ask for an e-mail and a password to create a new backoffice user|
|user:update-password|4.13.10|-|This action will ask for an e-mail and a password, usefull to change a lost backoffice password|
|dev / development|4.13.10|-|Fast switch in development mode|
|prod / production|4.13.10|-|Fast switch in production mode|
|cache:design|4.14.0|`sae`, `mae`, `pe`|Rebuilds SAE/MAE/PE cache for design files|
|cache:clear|4.14.4|-|Clear `var/cache`, `var/log` & `var/tmp`|
|app:manifest|4.14.6|-|Rebuilds the app manifest|
|help|4.14.0|-|Display the command help manual|

### Examples

```bash
prompt $ ./cli export-schemas

prompt $ ./cli export-database
Filename for the export: dump.sql
Export done.

prompt $ ./cli version 4.13.7

prompt $ ./cli user:create
Input new backoffice user e-mail: demo@demo.com
Input new backoffice user password: ********
Your new user is now created.

prompt $ ./cli user:update-password
Input backoffice user e-mail to change: demo@demo.com
Your new password (min 8 characters): ********
Password successfully changed.

prompt $ ./cli dev


prompt $ ./cli prod
prompt $ ./cli prod

prompt $ ./cli cache:design <sae|mae|pe>

prompt $ ./cli cache:clear

prompt $ ./cli app:manifest

prompt $ ./cli help
```