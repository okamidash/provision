.. Copyright (c) 2017 RackN Inc.
.. Licensed under the Apache License, Version 2.0 (the "License");
.. Digital Rebar Provision documentation under Digital Rebar master license
.. index::
  pair: Digital Rebar Provision; Release Process

.. _rs_release_process:


Releases
~~~~~~~~


Version Scheme
--------------

There are two named releases and many semantic versioned releases.

* **tip** - This is the currently built master code.  It follows the bleeding edge of the trees.
* **stable** - This is the default release used by install.  It follows to most recently released code.

The other releases follow the v<Major>.<Minor>.<Patch> format.  e.g. **v3.0.0**

The :ref:`rs_install` process will default to **stable** but can be modified to use other releases.

The full version string generated by the build tool looks like this:

* v4.0.1 - A stable patch release
* v4.0.2-dev.1+gd012b1d6ba892c96c81c24ee93b668591663ca5c - A development tip build at this commit.  A potential v4.0.2 candidate.

The base form is semver tag, extra pieces, gits ahead of the current stable, and the actual git commit checksum.

The following are the pre-v4 schemas.  They are being phased out, but may still be seen.

* v3.0.0-tip-galthaus-dev-19-d012b1d6ba892c96c81c24ee93b668591663ca5c - a development tip build by a dev.
* v3.0.0-tip-16-e1fa235dc28f7d278bc34a0d4db87c306d9d3ba8 - A published tip build that is 16 commits ahead.
* v3.0.0-0-821108c416dfc1486919baa52dae284975d2ad8b - A stable release

The *dr-provision* server reports its version on start-up or can be queried by running:

  ::

    dr-provision --version

The *drpcli* client reports its version by running:

  ::

    drpcli version


Release Process
---------------

Each dev build will generate a new **tip** release and report that in the catalog.  These builds will be available through
the catalog as well.

Additionally, as releases cut at stable points, the **stable** build in the catalog will update to the most recent tagged build.
Both the **stable** and tagged build will be available through the catalog.

Release Notes
-------------

Each of the release specific changes are annotated in the Release Notes documentation.  You can find the release notes
at:

   https://github.com/digitalrebar/provision/v4/releases
