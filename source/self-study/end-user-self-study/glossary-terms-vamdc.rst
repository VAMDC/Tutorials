.. _glossary-terms-vamdc:

Glossary of terms for VAMDC 
===========================

If you cannot find the term you are looking for in this glossary, you may find it useful to look at http://www.ucl.ac.uk/~ucapch0/VAMDC/VAMDC_glossary.html .

.. _ivoa:

**I**

InChI
    International Chemical Identifier. Provides a human readable textual identifier for chemical substances. For example, the InChI for methane/CH4 is 1S/CH4/h1H4 . Please see http://www.iupac.org/inchi/ for further information. 

InChIKey
    A fixed length (25 characters) digital representation (non-human readable) of the InChI. For example, the InChiKey of methane/CH4 is inchikey VNWKTOKETHGBQD-UHFFFAOYSA-N. 

IVOA
    International Virtual Observatory Alliance. An alliance formed to develop the standards for the transmission and storage of astronomical data and encourage their use. http://www.ivoa.net/
    
**N**

Node
    A VAMDC node is a data service offering its data using the standards and protocols of VAMDC. Each node will provide the data for one or more atomic/molecular databases e.g. BASECOL, Chianti, HITRAN. 

**P**

Portal
    The `VAMDC portal <http://portal.vamdc.org/vamdc_portal/home.seam>`_ is a single web interface that can be used to send queries to all of the VAMDC nodes. The portal ensures that only those nodes that will understand a query will receive it. 

.. _registry:

**R**

Registry
    The VAMDC Registry can be considered as a database of databases; it stores information on each of the VAMDC databases (such as the description, where to access it and what keywords it supports in the search) which is then used by the portal when the user submits a query. The VAMDC registry was adapted from a similar service used by the :ref:`IVOA <ivoa>`; further information can be found http://standards.vamdc.org/registry/index.html

.. _sql:

**S**

Schema
    Is used to describe the content, structure and semantics of XML documents. See http://www.w3.org/XML/Schema 

SQL
    Structured Query Language. A programming language used in the querying and managment of data in relational databases such as MySQL or Postgres. VAMDC uses a modified form of SQL as it's query language - further information can be found at http://standards.vamdc.org/queryLanguage/index.html. 

**T**

TAPXSAMS
    See :ref:`VAMDC-TAP <vamdc-tap>` 

.. _vamdc-tap:

**V**

VAMDC
    Virtual Atomic and Molecular Data Centre. An EU project to build an interoperable e-Infrastructure for the exchange of atomic and molecular data. The home page of VAMDC is http://www.vamdc.org 

VAMDC-TAP
    VAMDC Table Access Protocol (also referred to as TAPXSAMS). The protocol used by VAMDC services for querying and returning data in th XSAMS format. Further information on the standard can be found at http://standards.vamdc.org/dataAccessProtocol/vamdctap.html 

.. _xsams:

**X**

XML
    Extensible Markup Language. A markup language, similar in appearance to HTML, designed to transport and store data. See http://www.w3schools.com/xml/xml_whatis.asp 

XSAMS
    XML Schema for Atoms, Molecules and Solids. XSAMS is the standard model used within VAMDC for the exchange of data. See http://standards.vamdc.org/dataModel/vamdcxsams/index.html#vamdcxsamslanguage-index for more details. 