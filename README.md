XSLT crosswalk from internal metadata format for Papyrus (Dspace 5.8 : https://papyrus.bib.umontreal.ca) into :

- OpenAIRE Guidelines for Literature Repository Managers v4 (https://www.openaire.eu/schema/repo-lit/4.0/openaire.xsd)

This code is based on the crosswalk developped by 4science for CARL-ABRC : https://www.carl-abrc.ca/news/release-of-dspace-5-6-extension-openaire/
(itself mostly a backport from the DSpace 7 version available at https://github.com/DSpace/DSpace/blob/master/dspace/config/crosswalks/oai/metadataFormats/oai_openaire.xsl
          adapted to work with the limitation of the flat data model of DSpace pre version 7)

In addition to the XSLT crosswalk file, you will also need to provide an additional entry for the oaire format in the xoai.xml within
<Context baseurl="request" name="Default Context">.

Please note that certain parts of this code that were originally taken from 4science are not used/called and haven't been cleaned yet.

Context info: We are running Dspace XMLUI 5.8.
Internal metadataformat is mainly DC (both dc and dcterms), ETDMS, OAIRE (citation* elements), as well as a few local elements (prefix: UdeM). Of those local element one is aligned on Rioxx definitions for Version Control.

