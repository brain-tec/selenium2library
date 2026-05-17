=====================
SeleniumLibrary 6.9.0
=====================


.. default-role:: code


SeleniumLibrary_ is a web testing library for `Robot Framework`_ that utilizes
the Selenium_ tool internally. SeleniumLibrary 6.9.0 is a new release with several
enhancements and bug fixes. A couple new keywords, for drag and drop as well as
getting css properties, have been added. Secret type support has be added. An issue
with using lists with chaining locators has been fixed. Several of the minim required
versions have been updated. More information about all the bug fixes and enhancements
can be found in these release notes.

If you have pip_ installed, just run

::

   pip install --upgrade robotframework-seleniumlibrary

to install the latest available release or use

::

   pip install robotframework-seleniumlibrary==6.9.0

to install exactly this version. Alternatively you can download the source
distribution from PyPI_ and install it manually.

SeleniumLibrary 6.9.0 was released on Sunday May 17, 2026. SeleniumLibrary supports
Python 3.10 through 3.14, Selenium 4.29.0 through 4.44.0 and
Robot Framework 6.1.1 and 7.4.2.

.. _Robot Framework: http://robotframework.org
.. _SeleniumLibrary: https://github.com/robotframework/SeleniumLibrary
.. _Selenium: http://seleniumhq.org
.. _pip: http://pip-installer.org
.. _PyPI: https://pypi.python.org/pypi/robotframework-seleniumlibrary
.. _issue tracker: https://github.com/robotframework/SeleniumLibrary/issues?q=milestone%3Av6.9.0


.. contents::
   :depth: 2
   :local:

Most important enhancements
===========================

- "Open Browser" keyword documentation has broken links which were fixed (`#1976`_)
- Chaining locators with lists does not work with Robot Framework 6.1 or above (`#1962`_)
  There was an issue with the types which prevented using chained locators as lists. This
  has been resolved in this release.
- Fix deprecation warnings and improve logging in tests (`#1974`_)
- Added "Drag And Drop Across Frames" keyword for cross-frame drag and drop support (`#1953`_)
  Note the still remains an issue with Firefox related to drag and drop. This change does
  note resolve the issue within gecko driver and Firefox.
- Input Password does not accept Secret type (`#1966`_)
  We have added support for the Secret Type into this release.
- Added "Get CSS Property Value" keyword to retrieve computed CSS values (`#1969`_)
- Selenium manager fails to download firefox/edge with lower versions of selenium (`#1986`_)

There were also several changes that are focused on internal processes and operations
- Migrate lint/format tooling to Ruff, update CI matrix, and stabilize cross-platform/firefox tests (`#1978`_)
- Update cookie validation regex in Get Cookies test (`#1973`_)
- Added new GitHub Actions workflow and performed yearly update on cookie test suite (`#1955`_)

Acknowledgements
================

I want to give a large shout out to [Yuri](https://github.com/yuriverweij) who had a large hand in getting
this release out the door including resolving issues, reviewing code changes, and fixing up our processes
and tooling, amongst all the other contributions he made towards this release. Some of these include

- Update cookie validation regex in Get Cookies test (`#1973`_)
- Fix deprecation warnings and improve logging in tests (`#1974`_)
- Review restriction on running ApprovalTests under Windows (`#1884`_)
- Migrate lint/format tooling to Ruff, update CI matrix, and stabilize cross-platform/firefox tests (`#1978`_)

Yuri along with [Tatu](https://github.com/aaltat) brought in the Secret type into this release.

- Input Password does not accept Secret type (`#1966`_)

I also want to thank a couple of first time contributors. Let me thank [Vamsi](https://github.com/b-vamsipunnam) for a
couple new keywords

- Added "Drag And Drop Across Frames" keyword for cross-frame drag and drop support (`#1953`_)
- Added "Get CSS Property Value" keyword to retrieve computed CSS values (`#1969`_)

And I also want to recognize and thank [Jaroslav Cerman](https://github.com/antivirak) for fixing a type error in deprecation message (`#1947`_).
Great job Jaroslav and Vamsi on these first time contributions!

I also want to thank
- [jjaakkola-atostek](https://github.com/jjaakkola-atostek) for reporting that chaining locators with lists does not work with Robot Framework 6.1 or above (`#1962`_)
- [Slava Semushin](https://github.com/php-coder) for reporting the "Open Browser" keyword documentation has broken links (`#1976`_)

And I once again want to recognize and give my thanks to the ongoing support by Tatu Aalto.


Full list of fixes and enhancements
===================================

.. list-table::
    :header-rows: 1

    * - ID
      - Type
      - Priority
      - Summary
    * - `#1962`_
      - bug
      - critical
      - Chaining locators with lists does not work with Robot Framework 6.1 or above
    * - `#1973`_
      - bug
      - high
      - Update cookie validation regex in Get Cookies test
    * - `#1953`_
      - enhancement
      - high
      - Add "Drag And Drop Across Frames" keyword for cross-frame drag and drop support
    * - `#1955`_
      - enhancement
      - high
      - Added new GitHub Actions workflow and performed yearly update on cookie test suite
    * - `#1966`_
      - enhancement
      - high
      - Input Password does not accept Secret type
    * - `#1969`_
      - enhancement
      - high
      - Add "Get CSS Property Value" keyword to retrieve computed CSS values
    * - `#1974`_
      - enhancement
      - high
      - Fix deprecation warnings and improve logging in tests
    * - `#1978`_
      - enhancement
      - high
      - Migrate lint/format tooling to Ruff, update CI matrix, and stabilize cross-platform/firefox tests
    * - `#1986`_
      - enhancement
      - high
      - Selenium manager fails to download firefox/edge with lower versions of selenium
    * - `#1947`_
      - bug
      - medium
      - Fix typo in deprecation message
    * - `#1976`_
      - bug
      - medium
      - "Open Browser" keyword documentation has broken links
    * - `#1921`_
      - enhancement
      - medium
      - Use Dependabot to update deps automatically
    * - `#1884`_
      - ---
      - medium
      - Review restriction on running ApprovalTests under Windows
    * - `#1967`_
      - ---
      - medium
      - Bump actions/upload-artifact from 4 to 7
    * - `#1963`_
      - bug
      - ---
      - `#1962`_ fix cascading locators
    * - `#1956`_
      - ---
      - ---
      - Dependabot
    * - `#1971`_
      - ---
      - ---
      - Fixed doc formating issue within xpath examples

Altogether 17 issues. View on the `issue tracker <https://github.com/robotframework/SeleniumLibrary/issues?q=milestone%3Av6.9.0>`__.

.. _#1962: https://github.com/robotframework/SeleniumLibrary/issues/1962
.. _#1973: https://github.com/robotframework/SeleniumLibrary/issues/1973
.. _#1953: https://github.com/robotframework/SeleniumLibrary/issues/1953
.. _#1955: https://github.com/robotframework/SeleniumLibrary/issues/1955
.. _#1966: https://github.com/robotframework/SeleniumLibrary/issues/1966
.. _#1969: https://github.com/robotframework/SeleniumLibrary/issues/1969
.. _#1974: https://github.com/robotframework/SeleniumLibrary/issues/1974
.. _#1978: https://github.com/robotframework/SeleniumLibrary/issues/1978
.. _#1986: https://github.com/robotframework/SeleniumLibrary/issues/1986
.. _#1947: https://github.com/robotframework/SeleniumLibrary/issues/1947
.. _#1976: https://github.com/robotframework/SeleniumLibrary/issues/1976
.. _#1921: https://github.com/robotframework/SeleniumLibrary/issues/1921
.. _#1884: https://github.com/robotframework/SeleniumLibrary/issues/1884
.. _#1967: https://github.com/robotframework/SeleniumLibrary/issues/1967
.. _#1963: https://github.com/robotframework/SeleniumLibrary/issues/1963
.. _#1956: https://github.com/robotframework/SeleniumLibrary/issues/1956
.. _#1971: https://github.com/robotframework/SeleniumLibrary/issues/1971
