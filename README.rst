DOCKER PHP
===========

docker for php

|Build Status| |Docker Stars| |Docker Pulls| |Code Climate| |GitHub stars| |Issue Count| |license| |Test Coverage|

:Version: 0.0.0
:Web: https://github.com/hadenlabs/docker-php
:Download: https://github.com/hadenlabs/docker-php
:Source: https://github.com/hadenlabs/docker-php
:Keywords: docker-php

Download size of this image is only:

|MicroBadger|

.. contents:: Table of Contents:
    :local:

Requirements
------------

.. code-block:: bash

  make setup

Actions Makefile
----------------

.. code-block:: bash

  λ make
      ༼ つ ◕_◕ ༽つ Makefile for Cookiecutter docker

      Usage:
          make environment               create environment with pyenv
          make install                   install dependences python by env
          make clean                     remove files of build
          make setup                     install requirements

          Docker:

              make docker.build         build all services with docker-compose
              make docker.down          down services docker-compose
              make docker.ssh           connect by ssh to container
              make docker.stop          stop services by env
              make docker.verify_network           verify network
              make docker.up             up services of docker-compose
              make docker.list           list services of docker

          Tests:

              test.lint                  Run all pre-commit
              test.syntax                Run all syntax in code

Changelog
---------

Please see `CHANGELOG <CHANGELOG.md>`__ for more information what has
changed recently.

Contributing
------------

Please see `CONTRIBUTING <CONTRIBUTING.md>`__ for details.

Credits
-------

Made with :heart: :coffee: and :pizza: by `hadenlabs <https://github.com/hadenlabs>`__

-  `All Contributors <AUTHORS>`__

.. |Code Climate| image:: https://codeclimate.com/github/hadenlabs/docker-php/badges/gpa.svg
   :target: https://codeclimate.com/github/hadenlabs/docker-php
.. |GitHub issues| image:: https://img.shields.io/github/issues/hadenlabs/docker-php.svg
   :target: https://github.com/hadenlabs/docker-php/issues
.. |GitHub forks| image:: https://img.shields.io/github/forks/hadenlabs/docker-php.svg
   :target: https://github.com/hadenlabs/docker-php
.. |GitHub stars| image:: https://img.shields.io/github/stars/hadenlabs/docker-php.svg
   :target: https://github.com/hadenlabs/docker-php
.. |Issue Count| image:: https://codeclimate.com/github/hadenlabs/docker-php/badges/issue_count.svg
   :target: https://codeclimate.com/github/hadenlabs/docker-php
.. |license| image:: https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square
   :target: LICENSE
.. |Test Coverage| image:: https://codeclimate.com/github/hadenlabs/docker-php/badges/coverage.svg
   :target: https://codeclimate.com/github/hadenlabs/docker-php/coverage

.. |MicroBadger| image:: https://images.microbadger.com/badges/image/hadenlabs/docker-php.svg
   :target: http://microbadger.com/images/hadenlabs/docker-php
.. |Docker Stars| image:: https://img.shields.io/docker/stars/hadenlabs/docker-php.svg?style=flat-square
   :target: https://hub.docker.com/r/hadenlabs/docker-php
.. |Docker Pulls| image:: https://img.shields.io/docker/pulls/hadenlabs/docker-php.svg?style=flat-square
   :target: https://hub.docker.com/r/hadenlabs/docker-php

.. |Build Status| image:: https://travis-ci.org/hadenlabs/docker-php.svg
   :target: https://travis-ci.org/hadenlabs/docker-php