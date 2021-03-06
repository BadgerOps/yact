============
YACT - Yet Another Config tool
============
Simple configuration handling for Python applications.
------------------------------------------------------
.. image :: https://travis-ci.org/jesseops/yact.svg?branch=master
    :target: https://travis-ci.org/jesseops/yact

.. image :: https://coveralls.io/repos/github/jesseops/yact/badge.svg?branch=master
    :target: https://coveralls.io/github/jesseops/yact?branch=master

.. image:: https://badges.gitter.im/yact-py/Lobby.svg
   :alt: Join the chat at https://gitter.im/yact-py/Lobby
   :target: https://gitter.im/yact-py/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge

YACT is a simple, lightweight, and flexible configuration package for Python applications.
It's designed to be as easy as possible to setup configuration for your project without needing to
jump through hoops.

Examples
========

**Basic usage:**

::

    >>> import yact
    >>> config = yact.from_file('sample.yaml')
    >>> assert isinstance(config, yact.Config)
    True

**Modifying and saving:**

::

    >>> config.set('foo', 'bar')
    >>> print(config['foo'])
    'bar'
    >>> config.save()

**Dot notation for nested configs:**

::

    >>> config.set('this.is.nested', True)
    >>> print(config.get('this')['is']['nested'])
    True
