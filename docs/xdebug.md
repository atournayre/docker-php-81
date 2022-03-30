# Xdebug

The default Docker stack is shipped **with** [Xdebug](https://xdebug.org/),
a popular debugger and profiler for PHP.

## Debugging with Xdebug and PHPStorm

You can use the **Xdebug extension** for [Chrome](https://chrome.google.com/webstore/detail/xdebug-helper/eadndfjplgieldjbigjakmdgkmoaaaoc) or [Firefox](https://addons.mozilla.org/fr/firefox/addon/xdebug-helper-for-firefox/) if you want to debug on the browser (don't forget to configure it).

If you don't want to use it, add on your request this query param: `XDEBUG_SESSION=PHPSTORM`.

On PHPStorm, click on `Start Listening for PHP Debug Connections` in the `Run` menu.

Otherwise, you can create a [PHP Remote Debug](https://www.jetbrains.com/help/phpstorm/creating-a-php-debug-server-configuration.html) configuration with the following parameters:

* Server:
  * Name: `symfony` (must be the same as defined in `PHP_IDE_CONFIG`)
  * Host: `https://localhost` (or the one defined with `SERVER_NAME`)
  * Port: `443`
  * Debugger: `Xdebug`
  * Absolute path on the server: `/srv/app`
* IDE key: `PHPSTORM`

You can now use the debugger.

## Troubleshooting

Inspect the installation with the following command. The Xdebug version should be displayed.

```console
$ docker-compose exec php php --version

PHP ...
    with Xdebug v3.1.2 ...
```
