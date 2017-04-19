Changelog
=========


%%version%% (unreleased)
------------------------
- Changing tox tester to nose. [AlexV]
- Moving ctx_server back to pyros to keep dependencies one-way. [AlexV]
- Renaming test_pyros_mock for pytest to detect it. [AlexV]
- Removing the pkgutil way to only use one way to do namespace packages.
  [AlexV]
- Adding tox and travis files. adding dependency on pyros repo for
  tests... [AlexV]
- Setup.py publish command description change. [AlexV]
- Adding null logging handler by default. [AlexV]
- Keep using the same ros package name for now. [AlexV]
- Reorganizing to nest everything under pyros_interfaces namespace.
  [AlexV]
- Now relying on catkin_pip >0.2. [AlexV]
- Fix for cmakelists. added dependencies in package.xml. [alexv]
- Added git changelog configuration. some setup.py fixes. [alexv]


0.4.0 (2017-01-18)
------------------
- V0.4.0. [alexv]
- More fixes to get other tests to pass. [alexv]
- Restructuring pyros_common to simplify things. added cmakelists and
  package.xml temporarily, while we get everything working together from
  source... [alexv]
- Adding pyros protocol. [alexv]
- Fixed setup.py. [alexv]
- Moving code from pyros. [alexv]
- Initial commit. [AlexV]


