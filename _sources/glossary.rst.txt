.. _glossary:

Glossary
========

.. glossary::
   :sorted:

   reVReports
      CLI and Python package that generates publication-ready plots,
      maps, and characterization tables from reV supply-curve outputs.

   Pixi
      Environment manager used to install dependencies, run tasks, and
      maintain reproducible shells for reVReports.

   supply curve
      reV output CSV with scenario-level columns such as capacity,
      annual energy, area, and metadata for each supply-curve point.

   scenario
      Named supply-curve input defined in the configuration that maps to
      a source CSV on disk and optional scenario-specific styling.

   configuration file
      JSON document consumed by reVReports describing scenarios,
      output directories, palettes, DPI, and other plotting options.

   scenario palette
      Mapping of scenario names to colors used across plots and maps for
      consistent styling.

   plot bundle
      Collection of report figures produced by ``reVReports plots``
      including bar charts, box plots, histograms, and regional views.

   map bundle
      Geospatial images produced by ``reVReports maps`` that visualize
      scenario capacity, density, or other metrics over study regions.

   characterization map
      JSON that maps characterization names to column paths inside
      supply-curve rows used by ``unpack-characterizations``.

   bespoke wind supply curve
      reV output variant where characterization data is embedded as JSON
      strings that can be expanded into columns for analysis.

   output directory
      Destination folder for generated images and CSVs. It is created if
      it does not already exist.

   DPI
      Dots per inch for saved PNG figures. Defaults to the package-wide
      ``DPI`` constant from ``reVReports.utilities.plots``.

   prefix outputs
      Optional configuration toggle that prepends ``"plot_"`` to emitted
      filenames to avoid clobbering existing images.
