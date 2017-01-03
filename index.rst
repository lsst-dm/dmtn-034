..
  Technote content.

  See https://developer.lsst.io/docs/rst_styleguide.html
  for a guide to reStructuredText writing.

  Do not put the title, authors or other metadata in this document;
  those are automatically added.

  Use the following syntax for sections:

  Sections
  ========

  and

  Subsections
  -----------

  and

  Subsubsections
  ^^^^^^^^^^^^^^

  To add images, add the image file (png, svg or jpeg preferred) to the
  _static/ directory. The reST syntax for adding the image is

  .. figure:: /_static/filename.ext
     :name: fig-label
     :target: http://target.link/url

     Caption text.

   Run: ``make html`` and ``open _build/html/index.html`` to preview your work.
   See the README at https://github.com/lsst-sqre/lsst-technote-bootstrap or
   this repo's README for more info.

   Feel free to delete this instructional comment.

:tocdepth: 1
.. Please do not modify tocdepth; will be fixed when a new Sphinx theme is shipped.

.. sectnum::

.. Add content below. Do not include the document title.

LSST Data Management has recently finished the Summer 2012 Data Challenge, our latest semi-annual development cycle.
Its goals were to prototype extended source photometry algorithms, image-coaddition pipelines, forced-photometry pipelines, and the associated middleware and user interfaces for LSST.
To assess our success and inform future work, we used the resulting code to reprocess and analyze a small subset (~5%) of SDSS Stripe 82.
We have released this data (and software) at the 2012 LSST All Hands Meeting to demonstrate the current capabilities of DM code, and in hope you may find the reprocessed data scientifically interesting.

For those who were not at the AHM, this document provides the links to the Summer 2012 software, data, and documentation.
They include a catalog measured from a subset of frames of SDSS Stripe 82, a deep r-band coadd of the same area, and a catalog of forced photometry at locations where sources were detected in the coadd.

Our preliminary analysis indicates the quality of this dataset is comparable to that of SDSS DR8, with the deep forced photometry catalog providing added value over DR8. Nevertheless, we caution you that this is prototype code.
It is still incomplete both in terms of features and quality, and the same will be true of the reprocessed data. If you do notice issues, or have questions, please don't hesitate to contact us at ``<dm-help --at-- lsstcorp.org>``.

Summer 2012 Data Challenge Outputs
----------------------------------

Below is a list of links to outputs of Summer 2012 data challenge.
A description of the challenge is available in the `Data Challenge Handbook`_.
You may also find useful the presentations on the Summer 2012 data release that were given at the `All Hands Meeting`_:

* `Summer 2012 Data Challenge Plenary <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13608>`_
* `Overview of Summer 2012 Data Release <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13657>`_
* `Summer 2012 co-adds and forced photometry <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13640>`_
* `Summer 2012 Extended Source Photometry <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13659>`_
* `Summer 2012 Database Schema <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13662>`_
* `Summer 2012 Data Access Tools <https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-13663>`_

.. _Data Challenge Handbook: https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-15286
.. _All Hands Meeting: https://www.lsstcorp.org/ahm2012/node/40

.. note::

   Some of these websites require the standard DM user name and password; if you don't know it already, it can be found in Section 2.2.1 of the `prior Data Challenge Handbook`_.

.. _prior Data Challenge Handbook: https://docushare.lsstcorp.org/docushare/dsweb/Get/Document-10762

.. note::

   The catalog and image access tools in use here are temporary solutions for data distribution graciously provided to us by IPAC: in particular, they are *NOT* representative of the Science User Interface the LSST will ultimately have.

* Summer 2012 `Data Challenge Handbook`_.
* `Catalogs access (Gator) <https://osiris.ipac.caltech.edu/>`_
* `Download of coadded images (Image Inventory Service) <https://osiris.ipac.caltech.edu/cgi-bin/LSST/nph-lsst>`_
* `Image/catalog visualization and analysis tool (Hydra) <https://osiris.ipac.caltech.edu/applications/lsst/>`_
* `Data Management Software Summer 2012 Release <https://dev.lsstcorp.org/trac/wiki/Installing/Summer2012>`_
* `Data Quality Assessment (pipeQA) <http://lsst1.ncsa.uiuc.edu/pipeQA/public/>`_
* `LSST Summer 2012 Database Schema <http://lsst-web.ncsa.illinois.edu/schema/index.php?sVer=S12_sdss>`_ (note: this is not the Gator schema, this is the internal MySQL database schema; let us know if you need to access it)

If you decide to make use of this data, feel free to inquire about the details at ``<dm-help --at-- lsst.org>``.
Note that the users of these data (though not the software), have to abide by the `LSST Publication Policy`_.

.. _LSST Publication Policy: http://ls.st/LPM-162

Known issues
------------

Examples on some data access tools are misleading (e.g., "search for M81", when M81 is not within the reprocessed footprint)
    We are aware of the issue and are working to resolve it. In the meantime, take a look at the footprints below to guide your searches.
Clicking Hydra tool's help ('?') button leads to a password-protected page
    We are aware of the issue and are working to resolve it.

Covered footprint
-----------------

A quick visualization of the footprint available in Summer 2012 data release, created by plotting all 250+ million forced sources:

.. image:: /_static/Summer2012-Footprint.png
   :alt: Summer2012 Footprint
   :target: _static/Summer2012-Footprint.png

.. image:: /_static/Summer2012-Footprint-Zoomed.png
   :alt: Summer2012 Footprint Zoomed
   :target: _static/Summer2012-Footprint-Zoomed.png

.. note::

   This document was originally published as an LSST TRAC page at https://dev.lsstcorp.org/trac/wiki/DC/Summer2012
