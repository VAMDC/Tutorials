.. _build-a-node:

Teaching materials for node-building
====================================

Contents:

.. toctree::
   :maxdepth: 1

   introductory-talk
   infrastructure-check-list
   spectroscopic/index
   collisional/index
   virtual-machine
   node-faq


The node-building tutorial is intended to be given by a VAMDC person to a group of prospective data-providers. The materials presented here are for the presenter to assemble into an agenda. The materials might be shown either to a small group (< 5 persons) or to a larger audience, but the presenter would have to arrange them differently for these two cases.

The introductory talk is technical and has little about the scientific purpose of VAMDC. The presenter may wish to prefix the technical talk with some contextual slides.

In node-building tutorials, the ideal is that students build a node around the actual data they wish to publish. In practice, this never works. Either the students come to the tutorials without any data samples, or their real data present too many problems of detail for the presenter to fix in real time. [#]_ Therefore, two worked examples are provided, one for spectroscopy and one for collisional data.

The spectroscopic node uses some of the atomic data from Chianti, and the Chianti node-software from the 12.07 system. This node demonstrates how to create the database from ASCII files.

The collisional node uses data contributed by Johannes Postler from IDEADB with node-software written by Guy Rixon during a tutorial at Innsbruck in 2013.

Both example nodes use the Python/Django node-software, which in turn uses some FOSS infrastructure. Getting this infrastructure to run can be time-consuming, so presenters (and preferably students) should work through the check-list before the tutorial.

Any tutorial on node building should ultimately refer to the excellent `node-software manual <http://www.vamdc.org/documents/nodesoftware/index.html>`_, and follow the sequence therein.

The frequently-asked-question list covers points of detail arising from previous tutorials.




.. rubric:: Footnotes

.. [#] Trying to write the python parts of a node on a projector in front of an audience is a ghastly thing to do unless you know *exactly* what to write to make the thing work. 

