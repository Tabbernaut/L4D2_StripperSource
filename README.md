L4D2-Stripper Source
====================

Just the http://hg.alliedmods.net/strippersource/ (7b6b696412c5) Stripper:Source build, with some adjustments to make it work on servers with outdated glibc version libraries (2.12 where 2.15+ is required).

Thanks to Crepes, who explained to me why Stripper didn't work on some linux systems.

Note: this is really only to build L4D2-working versions for linux builds that have outdated glibc libraries. It may require copying tier0_srv and vstdlib_srv files into a number of hlsdk*/lib/linux directories, if you really want it to compile the full package.
I wouldn't trust this build for anything but a L4D2 fix.


1.2.3a Update
=============

Two cvars added:

stripper_cfg_path_base<br/>
stripper_cfg_path_fixes<br/>

These cvars, if set to properly structured stripper config directories, will load additional configs. The idea is that you can build directories with shared "base" stripper configs for your matchmode, and/or "fixes" stripper changes, like exploit fixes.
This should make it easier to update/manage stripper changes, especially when dealing with vast amounts of configs on a server.
