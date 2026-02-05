# Installing

The Server could be installed in 2 ways:

## 1. Via install script

This case requires the next points==:==

* create version tag for some release, which give direct link to ZIP archive examples:
  * tags: [https://github.com/Overdose-Digital/magento2-cms-management/tags](https://github.com/Ovice Weeklyerdose-Digital/magento2-cms-management/tags)
  * link: <https://github.com/Overdose-Digital/magento2-cms-management/archive/refs/tags/v2.0.4.zip>
* in service download folder must be added installer script:
  * ex: curl http://db-manager-cli.bridge2.digital/download/server-install


And to executing installation could be executed the next comma

```javascript
curl http://db-manager-cli.bridge2.digital/download/dbvisor-agent-install | sh
```

Possible curl parameters:

* -v - verbose, will show all warnings
* -k - will ignore SSL certificates validating
* -L - locations, in case it used will go through all redirects till page return 200 or 404 ( or other final state )

The command will download archive with server tool, unpack it to default directory: **.**dbvisor-agent and executes **setup** script


Variables in install script:

```javascript
APP_VERSION - tool version
APP_GIT_REPO_NAME - name of a repository, used for correct unpack code
APP_DOWNLOAD_LINK - link to archive
APP_DIR - default directory
```


Installation script ( support using sh and bash ):

[dbvisor-agent-install 2032](uploads/9f56bcd5-07d0-4467-a6ea-4f73c0b2c828/ed66cb65-b27d-49f4-a8ef-a5e341ae9825/dbvisor-agent-install)


## 2. Manually with setup command

This  way for cases when customer directly download source code.

Then him must execute command:

```bash
./dbvisor-agent setup
```


\
## Steps after tool installing:

After successful installing need to execute are next commands:

```bash
dbvisor-agent app:server:add
```

those command will authorize the server in service.

The next one:

```bash
dbvisor-agent app:cron:install
```

those command will install required cron jobs, the command will automatically executed on non-docker case