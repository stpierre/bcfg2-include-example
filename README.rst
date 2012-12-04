This repo shows off some examples of the Bcfg2 TemplateHelper
``include.py`` example, which can be used to provide a far superior
replacement for deprecated ``.cat`` files in Bcfg2 1.3.x.  Two
examples are provided:

* ``/etc/passwd`` is a fairly simple example, in which a base list of
  users is given, and then the include helper includes other group-
  and host-specific files to add supplementary users.  (Note that this
  is actually a bad example, since Bcfg2 1.3 has built-in support for
  handling users and groups, so you should use that instead.  This is
  included because it was specifically requested.)
* ``/etc/sysconfig/iptables`` is a more complex example, showing
  inclusion of different files for different tables (filter, nat,
  mangle, and raw) in different places in the master template (i.e.,
  not just at the end).  This more clearly shows the superiority of
  this approach to .cat files.
