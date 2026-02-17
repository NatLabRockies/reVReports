Installing reVReports
=====================

.. inclusion-install

Installing from PyPI
--------------------

reVReports can be installed via pip from
`PyPI <https://pypi.org/project/reVReports/>`__.

.. code-block:: shell

    pip install reVReports

.. note::

    It is recommended to install and run reVReports from an isolated
    environment (``pixi`` or ``conda``) rather than a system Python.


Handling ImportErrors
---------------------

If you encounter an ``ImportError``, it usually means that Python could not
find reVReports in your active environment. You can inspect the search path
with:

.. code-block:: python

    import sys
    sys.path

If multiple Python installations are present, ensure reVReports is installed
in the interpreter you are using (for example, avoid ``/usr/bin/python``).
Using a dedicated environment helps avoid these conflicts.


Installing from source (recommended for development)
----------------------------------------------------

We keep a version-controlled ``pixi.lock`` so contributors share the same
dependencies. To work from source:

1. Install `pixi <https://pixi.sh/latest/#installation>`__.
2. Clone the repository:

   - SSH: ``git clone git@github.com:NatLabRockies/reVReports.git``
   - HTTPS: ``git clone https://github.com/NatLabRockies/reVReports.git``

3. Sync and enter the development environment:

   .. code-block:: shell

       pixi install --frozen -e dev
       pixi shell -e dev

4. Verify the CLI:

   .. code-block:: shell

       pixi run -e dev reVReports --help

Common environments
~~~~~~~~~~~~~~~~~~~

- ``default``: runtime dependencies for the CLI and library
- ``dev``: adds linting/formatting tools (Ruff)
- ``test``: adds pytest and coverage extras
- ``doc``: adds Sphinx and doc build extras
- ``build``: packaging helpers

You may use other environment managers (``conda``, ``mamba``), but we only
support Pixi-managed setups when diagnosing environment issues.
