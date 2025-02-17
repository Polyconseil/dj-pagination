Version History
***************


Next version
============

* Add support for Python 3.11 and 3.12
* Add support for Django 4.2 and 5.0
* Add support for Python 3.8 to 3.10
* Drop support for Django 2.2 and 3.0, add support for Django 3.2


.. _version_2_4_0:

Version 2.4.0
==============

* Markdown readme
* Formal support for Django 2.0 and 2.1
* Remove support for unsupported versions of Python and Django

Version 2.3.3
==============

* Formal support for Django 2.0 and 2.1
* Remove support for unsupported versions of Python and Django


Version 2.3.2
==============

Fixed extras_require for py2/3 differences

.. _version_2_3_1:

Version 2.3.1
==============

use extras_require for py2/3 differences

.. _version_2_3_0:

Version 2.3.0
=============

Add request object to context

.. _version_2_0_4:

Version 2.0.4
=============

This is a micro release to push minor fixes to a PyPI release.


.. _version_2_0_2:

Version 2.0.2
=============

This is an another micro release. There are no code changes (apart from
setup.py). The only change is to make it pip-friendly by using new integration
mode with versiontools.

.. _version_2_0_1:


Version 2.0.1
=============

This is a micro release. There are no code changes so there is no need to
upgrade. The only changes are to documentation and infrastructure files.

The following changes are included:

* Improve documentation for using custom pagination templates
* Document multiple paginations per page
* Use correct template name in do_paginate docstring
* Provide correct link to installation instructions
* Fix documentation referencing all project name
* Ignore vim swap files
* Add templates from the test project to MANIFEST.in


.. _version_2_0:

Version 2.0
===========


* Revived the project as a fork of
  git://github.com/ericflo/django-pagination.git. The project now has a new
  maintainer (Zygmunt Krynicki) and a new home (on pypi and launchpad).

* Merged a lot of branches of the old project. In general this was made to show
  people "here is the new good stuff" and to get as much contributions, back
  into the trunk, as possible.

* Merge a lot of translations: de, es, fr, it, nn, no, pl, pt, pt_BR, ru and
  tr. Translations are still in a bad state (they are not built automatically,
  they are in incorrect place) but the first step is done.

* Add support for custom pagination templates. You can now use the optional
  argument on paginate to use different template::

    {% autopaginate obj_list %}
    ...
    {% paginate using "something/custom_template.html" %}

* Pagination template has support for specific blocks. Those blocks are
  'previouslink', 'pagelinks' and 'nextlink'.  Make sure to base your template
  on pagination/pagination.html end extend the blocks you care about.

* Add support for using multiple paginations on a single page. Simply use
  multiple autopaginate/paginate tags. The only limitation is that you must use
  paginate before using the next autopaginate tag. For an example see the test
  project and the example application inside.

* Simplify building documentation. To build the documentation simply run
  `setup.py build_sphinx`. You will need sphinx installed obviously.

* Simplify running tests. To run tests just invoke `setup.py test`. That's all!
  This is based on the goodness of django-testproject that simplifies setting
  up helper projects just for testing.


Version 1.0.7
=============

* Last release from previous upstream developer.
