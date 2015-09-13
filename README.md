Put this in `~/.rakudobrew`, and add aliases for convenience.

It's quick and dirty, may be broken on your system. Please report any breakages.

Installing rakudobrew
---------------------

On *nix do:
```
git clone https://github.com/tadzik/rakudobrew ~/.rakudobrew
export PATH=~/.rakudobrew/bin:$PATH
rakudobrew init # Instructions for permanent installation.
```

On Windws do:
```
git clone https://github.com/tadzik/rakudobrew %USERPROFILE%\rakudobrew
SET PATH "%USERPROFILE%\rakudobrew\bin;%PATH%"
rakudobrew init # Instructions for permanent installation.
```

On Windws PowerShell do:
```
git clone https://github.com/tadzik/rakudobrew $Env:USERPROFILE\rakudobrew
$Env:PATH = "$Env:USERPROFILE\rakudobrew\bin;$Env:PATH"
rakudobrew init # Instructions for permanent installation.
```

Bootstrapping a Perl 6 implementation
-------------------------------------

Run something like:

```
$ rakudobrew build moar
```

to build the latest [Rakudo](https://github.com/rakudo/rakudo)
(in this case, on the [MoarVM](https://github.com/MoarVM/MoarVM) backend),
which should then be available as `perl6`. Then, to get the
[Panda module management tool](https://github.com/tadzik/panda), do:

```
$ rakudobrew build-panda
```


Upgrading your Perl 6 implementation
------------------------------------

```
$ rakudobrew build moar
```


Upgrading rakudobrew itself
---------------------------

```
$ rakudobrew self-upgrade
```


Uninstall rakudobrew and its Perl 6(s)
--------------------------------------

To remove rakudobrew and any Perl 6 implementations it's installed on your system,
just remove or rename the `~/.rakudobrew` directory.


Specifying custom git path
--------------------------

In case git is not in any standard `PATH` on your system, you can specify a custom path
to the git binary using a `GIT_BINARY` environment variable:

```
$ GIT_BINARY="%USERPROFILE%\Local Settings\Application Data\GitHub\PORTAB~1\bin\git.exe" rakudobrew build all
```

Command-line switches
---------------

Run `rakudobrew`


