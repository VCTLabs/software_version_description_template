
(unreleased)
------------
- Recipes-art/lxde-icon-theme: fix sourceforge URI so it works again.
  [Stephen L Arnold]

  * at some point the icon theme got some extra path elements, yay
- Layer.conf: compatible layers: add dunfell, gatesgarth, drop warrior,
  zeus. [Max Krummenacher]
- Lxtask: update to 0.1.10. [Max Krummenacher]

  This fixes link errors with gcc 10::

    | ...ld: lxtask-callbacks.o:.../lxtask-0.1.9/src/interface.h:64: multiple definition of `column';
    |        lxtask-main.o:.../lxtask-0.1.9/src/interface.h:64: first defined here

- Gpicview: drop gdk-x11 dependency. [Max Krummenacher]

  Remove the only place where gdk-x11 is needed and thus make it
  work under gtk under wayland.

  Signed-off-by: Max Krummenacher <max.krummenacher@toradex.com>
  (cherry picked from commit c8d84165284d95c0775584537ab2a2e9490723ea)
- Gpicview: inherit mime-xdg. [Max Krummenacher]

  The desktop file has key 'MimeType' which mandates 'inhert mime-xdg'.
- Core-image-lxde: add a core image. [Max Krummenacher]
- Packagegroup-lxde-extended: recommend l3afpad. [Max Krummenacher]
- Obconf: update to latest git. [Max Krummenacher]

  This dropes the no longer available dependency on libglade and moves to gtk3+
- Lxmenu-data: refresh patch. [Max Krummenacher]
- Lxsession: update to 0.5.4. [Max Krummenacher]
- Lxtask: update to 0.1.8. [Max Krummenacher]
- Lxrandr: update to 0.3.2. [Max Krummenacher]
- README: fix invalid descriptions. [Ming Liu]

  Change to master.

  Signed-off-by: Ming Liu <ming.liu@toradex.com>
  (cherry picked from commit ef686d11201b780d7db650f94b3a850a0eb3a6f5)

  Adapted from thud to master:
- Layer.conf: add zeus, drop sumo, thud from compatible layers. [Max
  Krummenacher]
- Lxsession: drop object introspection. [Max Krummenacher]
- Layer.conf: add warrior, drop sumo from compatible layers. [Max
  Krummenacher]
- Lxde-common: cope with added openbox session. [Max Krummenacher]

  The openbox recipe now also provides x-session-manager. Adapt recipe,
  so that when lxde-common is installed the lxde session takes precedence.
- Layer.conf: Add thud to LAYERSERIES_COMPAT. [Max Krummenacher]
- Wireless-tools: re-add from openembedded-core. [Max Krummenacher]

  wireless-tools got removed from openembedded-core but the package libiw
  from the recipe is required for lxde panel. Re-add it here.
- Lxsession: follow changed dependencies for x11. [Max Krummenacher]
- Layer: add LAYERSERIES_COMPAT. [Max Krummenacher]
- Stop making lists with a series of += [Max Krummenacher]

  Using the following pattern is very inefficent, stop using it.

  SRC_URI  = "src1"
  SRC_URI += "src2"
- Lxterminal: update to 0.3.2. [Max Krummenacher]
- Revert "xserver-common_%.bbappend: don't start XDG autostart" [Max
  Krummenacher]

  meta-openembedded no longer uses that patchfile (or a follow up) which
  gets removed here.

  See http://git.openembedded.org/meta-openembedded/commit/meta-oe/recipes-graphics/xserver-common?id=2f6e45baba961629bfe023599144be6cfcd45728

  This reverts commit 42cf6a87c90c4e1e62c7e417bba6d7ad6343889b.
- Keybinder-3.0: update to 0.3.2 and use git. [Max Krummenacher]

  Updates to version 0.3.2.
  Uses the code from git rather than from a (changing) source tarball.
- README: change dependencies to use branch rocko. [Max Krummenacher]
- Packagegroup-lxde-extended: add lxhotkey. [Max Krummenacher]
- Lxhotkey: add recipe. [Max Krummenacher]
- Lxterminal: update to 0.3.1. [Max Krummenacher]

  Move back to use the versioned tar ball, as that is now supporting
  gtk3.
- Lxtask: update to 0.1.8. [Max Krummenacher]
- Lxsession: update to 0.5.3. [Max Krummenacher]

  The gtk3 patch is upstreamed now, but new code does not comply with
  gtk3.
- Lxlauncher: update to lxlauncher_0.2.5. [Max Krummenacher]
- Lxde-common: update to 0.99.2. [Max Krummenacher]
- Lxappearance: update to 0.6.3. [Max Krummenacher]
- Lxrandr: add patch to cope with i.mx 6 segfault. [Max Krummenacher]
- Lxappearance-obconf: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxpanel: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxterminal: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxtask: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxrandr: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 172: glib-gettextize: command not found.
- Lxinput: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Gpicview: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxlauncher: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxappearance: depends on glib-2.0-native. [Max Krummenacher]

  Fixes run.do_configure: line 169: glib-gettextize: command not found.
- Lxsession: depends on vala-native. [Max Krummenacher]

  Fixes do_compile:/bin/sh: valac: command not found.
- Lxsession-edit: add missing intltool-native. [Max Krummenacher]
- Recipes: remove unneeded RDEPENDS. [Max Krummenacher]
- Layer.conf: add layer dependencies. [Max Krummenacher]

  While at it clean-up and unify with other Toradex layers.
- Lxsession: with latest oe-core gobject-introspection is needed. [Max
  Krummenacher]

  Otherwise you get build errors like this::

    | error: Package `glib-2.0' not found in specified Vala API directories
    |   or GObject-Introspection GIR directories

- Lxterminal: don't error out on faulty config for man pages. [Max
  Krummenacher]

  configure checks for XML catalogs from the host installation. If missing
  the resulting man/Makefile will fail in do_compile.

  Workaround this by ignoring that the man page can not be built.

  On Ubuntu were this was observed the following installs the required
  dependencies:
  sudo apt-get install docbook-xsl
  Better still one would fix lxterminal's configure to pick up OE's catalogs.
- Lxterminal: really add missing dependency to regenerate man. [Max
  Krummenacher]

  While libxslt-native is needed there are still docbook stylesheets and
  xmlto-native missing.
  xmlot-native pulls in all needed components so replacing libxslt-native
  with xmlto-native fixes the build.

  | make[2]: Entering directory '/build/krm/oe-core_V2.6.2/build_test/tmp-glibc/work/armv7at2hf-neon-angstrom-linux-gnueabi/lxterminal/git-r0/build/man'
  | /build/krm/oe-core_V2.6.2/build_test/tmp-glibc/sysroots/x86_64-linux/usr/bin/xsltproc -nonet http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl ../../git/man/lxterminal.xml
  | I/O error : Attempt to load network entity http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl
  | warning: failed to load external entity "http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl"
  | cannot parse http://docbook.sourceforge.net/release/xsl/current/manpages/docbook.xsl
  | Makefile:532: recipe for target 'lxterminal.1' failed
- Lxde-common, lxsession-edit, lxswession, obconf: fix rdepends. [Marcel
  Ziswiler]
- Gpicview: add dependency on adwaita-icon-theme. [Marcel Ziswiler]

  Without this many of the buttons are shown with an ugly place holder
  image::

    root@apalis-t30:~# gpicview
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'media-playback-start' for stock:
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-out' for stock: Icon 'zoom-out' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-in' for stock: Icon 'zoom-in' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-fit-best' for stock: Icon 'zoom-fit-best' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-original' for stock: Icon 'zoom-original' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'media-playback-start' for stock:
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-out' for stock: Icon 'zoom-out' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-in' for stock: Icon 'zoom-in' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-fit-best' for stock: Icon 'zoom-fit-best' not present in theme nuoveXT2
    (gpicview:657): Gtk-WARNING **: Error loading theme icon 'zoom-original' for stock: Icon 'zoom-original' not present in theme nuoveXT2

- Lxterminal: add missing dependency to regenerate man. [Max
  Krummenacher]

  Building from git requires regenerating the man pages with
  xsltproc. Thus the recipe must depend on libxslt-native.
- Lxterminal: remove now unused files. [Max Krummenacher]
- Update README to depend on the morty version. [Max Krummenacher]
- Lxpanel: fix gtk3 geometry issues. [Max Krummenacher]

  When the wnck pager is displayed the panel's width was set to the sum of
  all widgets, not the screen width.
  The with of a single task in the task bar was not reduced when all task's
  did no longer fit in the allocated taskbar width resulting in a panel which
  extended past the right side of the screen.
- Packagegroup-lxde-base: add lxappearance-obconf. [Max Krummenacher]
- Lxshortcut: add gtk2, gtk3 packageconfig and select gtk3 by default.
  [Max Krummenacher]
- Lxlauncher: add gtk2, gtk3 packageconfig and select gtk3 by default.
  [Max Krummenacher]
- Gpicview: add gtk2, gtk3 packageconfig and select gtk3 by default.
  [Max Krummenacher]
- Lxtask: add gtk3 packageconfig and enable it. [Max Krummenacher]
- Lxrandr: add gtk3 packageconfig and enable it. [Max Krummenacher]
- Lxsession: add gtk3 packageconfig and enable it. [Max Krummenacher]

  While at it remove patches which no longer applied.
- Lxappearance-obconf: add gtk3 packageconfig and enable it. [Max
  Krummenacher]

  While at it add missing depends reported by do_package_qa
- Lxappearance: add gtk3 packageconfig and enable it. [Max Krummenacher]
- Lxinput: add gtk3 packageconfig and enable it. [Max Krummenacher]
- Lxterminal: add recipe which fetches from git. [Max Krummenacher]

  This builds for gtk3 and vte with API 2.91
- Lxterminal: make it compatible with vte api 2.91 and move to gtk+ 3.
  [Max Krummenacher]

  While at it remove unneeded RDEPENDS, these are pulled in automatically
  by oe.
- Lxpanel: move to gtk+ 3. [Max Krummenacher]
- Keybinder: add gtk3 flavour. [Max Krummenacher]
- Keybinder: update to 0.3.1. [Max Krummenacher]

  While at it change the license string to MIT as the license text is an
  exact MIT copy and limit the checksummed part to only the license header.
- Keybinder: inherit gobject-introspection. [Max Krummenacher]

  Fixes do_compile::

    | make[1]: *** No rule to make target 'Keybinder-0.0.typelib', needed by 'all-am'.  Stop.

- Lxde-common: fix autoconf. [Max Krummenacher]
- Lxde-common: remove unneeded depends. [Max Krummenacher]
- Lxde-common: remove dangling patch. [Max Krummenacher]
- Lxsession: add missing depends on intltool-native. [Max Krummenacher]
- Lxpanel: add missing depends on intltool-native. [Max Krummenacher]
- Lxappearance: add missing depends on intltool-native. [Max
  Krummenacher]
- Gpicview: add missing depends on intltool-native. [Max Krummenacher]
- Recipes: stop using base_contains. [Max Krummenacher]

  The base_contains function is deprecated and we ought to use
  bb.utils.contains instead.
- Xserver-common_%.bbappend: don't start XDG autostart. [Max
  Krummenacher]

  This is also done by the session manager effectively starting the
  autostart items twice.
- Gdk-pixbuf_%.bbappend: build for x11. [Max Krummenacher]
- Obconf: update to 2.0.4. [Max Krummenacher]

  This also fixes a compile error against openbox 3.5.2 and later.
- Openbox: drop recipe in favour of meta-oe. [Max Krummenacher]
- Imlib2: drop recipe in favour of meta-oe. [Max Krummenacher]
- Remove unneeded PR variables. [Max Krummenacher]
- Gpicview: update to 0.2.5. [Max Krummenacher]
- Lxappearance-obconf: update to 0.2.3. [Max Krummenacher]
- Lxappearance: update to 0.6.2.bb. [Max Krummenacher]
- Lxtask: update to 0.1.7. [Max Krummenacher]
- Lxrandr: update to 0.3.1. [Max Krummenacher]
- Lxinput: update to 0.3.5. [Max Krummenacher]
- Lxpanel: update to 0.8.2. [Max Krummenacher]
- Lxmenu-data: update to 0.1.5. [Max Krummenacher]
- Lxde-common: update to 0.99.1. [Max Krummenacher]
- EADME: update branch to jethro. [Max Krummenacher]
- README: update branch to fido. [Stefan Agner]
- README: add dependency and contribution information. [Stefan Agner]
- Lxpanel: update to 0.8.1. [Max Krummenacher]
- Pcmanfm: drop in favour of oe-core. [Max Krummenacher]
- Libfm: drop in favour of oe-core. [Max Krummenacher]
- Menu-cache: drop in favour of oe-core. [Max Krummenacher]
- Lxsession: add libunique to DEPENDS. [Max Krummenacher]
- Recipes: don't use ${PN} as a recipe name placeholder. [Max
  Krummenacher]

  ${PN} might be extended with some magic prefix, so don't use it in SRC_URI
  assignments et. al.
- Recipes: replace short DESCRIPTION with SUMMARY. [Max Krummenacher]

  The SUMMARY variable gives a short description of the package (<72 chars).
  A missing DESCRIPTION is automatically set to the content of SUMMARY.
- Packagegroup-lxde: only lxde components but not DM/WM. [Max
  Krummenacher]
- Packagegroup-lxde-base: consistent whitespace. [Max Krummenacher]
- Lxsession: clarify DEPENDS/RDEPENDS. [Max Krummenacher]
- Add missing DEPENDS as reported by QA WARNINGS. [Max Krummenacher]
- Change to autotools-brokensep. [Max Krummenacher]

  change all recipe which fail out of tree builds to autotools-brokensep
- Pcmanfm: update to 1.2.3. [Max Krummenacher]

  Patch is sent to the oe-core layer. As this will not make it into dizzy
  add it here until we have it available from openembedded/meta.
- Menu-cache: update to 1.0.0. [Max Krummenacher]

  Patch is sent to the oe-core layer. As this will not make it into dizzy
  add it here until we have it available from openembedded/meta.
- Libfm: update to 1.2.3. [Max Krummenacher]

  Patch is sent to the oe-core layer. As this will not make it into dizzy
  add it here until we have it available from openembedded/meta.
- Lxde-common: update to 0.99.0. [Max Krummenacher]
- Lxterminal: update to 0.2.0. [Max Krummenacher]
- Lxsession: update to 0.5.2, obsoletes lxpolkit. [Max Krummenacher]

  lxsession now includes lxpolkit, remove receipe and package from
  packagegroup
- Lxpanel: update to 0.8.0. [Max Krummenacher]

  Add a libkeybinder recipe, as lxpanel now depends on it.

  While at it, remove old recipes.
- Gpicview: remove old recipe. [Max Krummenacher]
- Lxappearance-obconf: update to 0.2.2. [Max Krummenacher]
- Lxappearance: update to 0.6.1. [Max Krummenacher]
- Lxinput: update to 0.3.4. [Max Krummenacher]
- Lxlauncher: update to 0.2.4. [Max Krummenacher]
- Menu-cache: update to 1.0.0. [Max Krummenacher]
- Lxmenu-data: update to 0.1.4. [Max Krummenacher]
- Lxrandr: update to 0.3.0. [Max Krummenacher]
- Lxtask: update to 0.1.6. [Max Krummenacher]
- Lxde-icon-theme: update to 0.5.1. [Max Krummenacher]
- Lxdm: remove LXDM 0.4.1 in favor of LXDM 0.5 of meta-openembedded.
  [Stefan Agner]

  Remove LXDM 0.4.1 receipts in favor of LXDM 0.5 from meta-openembedded.
  The version 0.5 also supports systemd-logind as login/session manager
  which allows to remove now unsupported ConsoleKit without losing
  functionality.
- Lxpolkit: disable XDG autostart. [Stefan Agner]

  Disable XDG autostart of lxpolkit. lxsessions starts lxpolkit
  automatically without the need of a extra XDG autostart file.
- Lxsession: fix Hibernate button, gets disabled now. [Stefan Agner]

  The Hibernate function doesn't exist in our kernels, using DBus
  and systemd-logind, the lxsession should determine whether there
  is Hibernate support or not. However, due to a bug in the result
  parsing of lxsession, this did not work properly. Add patch to
  fix this issue.
- Lxrandr: don't use symlink for configure.ac. [Stefan Agner]

  Do not use symlink for configure.ac since autoconf don't like
  both, configure.in and configure.ac in place.
- Lxrandr: use symlink to create configure.ac. [Stefan Agner]

  Solves issue when building lxrandr with persistent work directory:
  | mv: cannot stat '/build/linuxdev/yocto-autobuilder/yocto-worker/toradex/build/build/out-eglibc/work/armv7ahf-vfp-neon-angstrom-linux-gnueabi/lxrandr/0.1.2-r0/lxrandr-0.1.2/configure.in': No such file or directory
- Obconf: force overwrite language files by autopoint. [Stefan Agner]

  This fixes errors when a second machine is built with the same work
  folder:
  | autopoint: File config.rpath has been locally modified.
  | autopoint: File po/Makefile.in.in has been locally modified.
  | autopoint: *** Some files have been locally modified. Not overwriting them because --force has not been specified. For your convenience, you find the local modifications in the file '/tmp/gtf3UV2x/autopoint.diff'.
  | autopoint: *** Stop.
  | ERROR: autopoint failed
- Obconf: add mirror for git. [Max Krummenacher]
- Lxsession: fix autoconf build. [Max Krummenacher]
- Lxpolkit: fix autoconf build. [Max Krummenacher]
- Lxmenu-data: fix gnu-gettext changes. [Max Krummenacher]
- Lxdm: fix autoconf build and add depends. [Max Krummenacher]
- Gpicview: deploy icon. [Max Krummenacher]
- Lxtask: add now required depends. [Max Krummenacher]
- Lxinput: add now required depends. [Max Krummenacher]
- Lxshortcut: add now required depends. [Max Krummenacher]
- Lxde: move base recipes from meta-toradex to meta-lxde. [Max
  Krummenacher]

  while at it, add attional DEPENDS for lxrandr
- Lxdm: add runtime dependency xinit. [Stefan Agner]

  Add xinit as runtime dependency since its required by LXDM.
- Lxappearance: update to 0.5.5. [Max Krummenacher]
- Lxsession: backport of lxsession-logout. [Max Krummenacher]

  0.4.9.2 segfaults when systemd's logind is installed.
- Menu-cache: update to 0.5.1. [Max Krummenacher]
- Lxappearance: update to 0.5.4. [Max Krummenacher]
- Gpicview: update to 0.2.4. [Max Krummenacher]
- Lxpanel: fix paths in git repo. [Max Krummenacher]
- Lxpanel: update to 0.6.1. [Max Krummenacher]
- Lxtask: backport Patch that resolves -1% CPU. [Max Krummenacher]

  http://lxde.git.sourceforge.net/git/gitweb.cgi?p=lxde/lxtask;a=commit;h=963dea395cc58eae940b85e242f0d84fb7d2eaa5
- DEPENDS: replace ${RDEPENDS} with the explicit deps. [Max
  Krummenacher]

  DEPENDS lists required built recipes at build time,
  whereas RDEPENDS does list required packages at runtime.
  So don't confuse the two namespaces by using one to define the other.
- Lxsession: enable dbus. [Max Krummenacher]
- Lxde: use packagegroup instead of task. [Max Krummenacher]
- Lxde: use packagegroup instead of task. [Max Krummenacher]
- Lxpanel: add wireless-tools to dependencies. [Max Krummenacher]
- Convert to new ALTERNATIVE_${PN} syntax. [Max Krummenacher]
- Task-lxde-extended: remove package lxsession-edit, this is now part of
  lxsession. [Max Krummenacher]
- Lxsession: update to 0.4.9.2. [Max Krummenacher]
- Lxpanel: add libwnck as a dependency. [Max Krummenacher]
- Lxpanel: update to 0.5.12. [Max Krummenacher]
- Lxinput: update to 0.3.2. [Max Krummenacher]
- Lxappearance: update to 0.5.2. [Max Krummenacher]
- Gpicview: update to 0.2.3. [Max Krummenacher]
- Lxde-icon-theme: update to 0.5.0. [Max Krummenacher]
- Add _${PN} to all DEPENDS variable definitions. [Max Krummenacher]
- Add missing autoconf tests required by newer autoconf version
  Backported a bugfix to lxdm (lxdm used 100% CPU) [Max Krummenacher]
- Add missing dependency to openbox. [Max Krummenacher]
- Split layer meta-lxde from github.com/tworaz/oe-tworaz. [Max
  Krummenacher]
- Corrected indentation to not upset bitbake. [Steve Phillips]
- Lxde-icon-theme RDEPEND on gnome-icon-theme. Without it some
  applications miss certain icons. [Peter Tworek]
- Fix lxappearance crash when empty cursors are used. [Peter Tworek]
- Add task-lxde-extended. [Peter Tworek]
- Fix lxde-icon-theme and lxappearance recipes. [Peter Tworek]
- Add lxsession-edit recipe. [Peter Tworek]
- Add lxpolkit recipe. [Peter Tworek]
- Add lxshortcut recipe. [Peter Tworek]
- Add lxinput recipe. [Peter Tworek]
- Add gpicview recipe. [Peter Tworek]
- Simplify lxappearance recipe. [Peter Tworek]
- Fix lxdm's xinitrc script to work with OE's default run-parts. [Peter
  Tworek]
- Move gcalctool to meta-jlime. It's not LXDE specific. [Peter Tworek]
- Move libgtkstylus from meta-lxde to meta-jlime. [Peter Tworek]
- Add recipe for task-lxde-base. [Peter Tworek]
- Add recipe for lxdm 0.4.1. [Peter Tworek]
- Import and fix libgtkstylus 0.5 recipe. [Peter Tworek]
- Add gcalctool 5.32.2 recipe. [Peter Tworek]
- Add obconf 2.0.3+git recipe. [Peter Tworek]
- Add lxtask 0.1.4 recipe. [Peter Tworek]
- Inherit pkgconfig instead of explicitly depending on pkgconfig-native.
  [Peter Tworek]
- Import some more LXDE recipes. [Peter Tworek]
- Openbox: don't depend on gtk-engines. [Peter Tworek]
- New layer: meta-lxde. Most stuff is imported from classic oe. [Peter
  Tworek]


