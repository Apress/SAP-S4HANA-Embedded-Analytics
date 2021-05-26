Following layered structure of CDS-views needs to be activated:
  ZQ_MM_INV_GDSMNV                     - Query-view
  |- ZC_MM_INV_GDSMNV                  - Cube-view
     |- ZP_MM_INV_GDSMNV               - Data-integration
        |- ZP_I_GoodsMovementDocument  - Data-integration
           |- I_MaterialDocumentRecord - Basic view with field mappings
              |- matdoc                - Source table Material Documents

Below, CDS-views of which first name and then description are given.

Steps for each CDS-view:
a. in IDE start "New Data Definition",
b. enter name and description,
c. copy text from file [name].txt,
d. paste into editor of IDE,
e. activate.

CDS-views (in order):
 1. ZP_I_GoodsMovementDocument, 'MM: Goods Movements & Stock'
 2. ZP_MM_INV_GDSMNV, 'MM: Goods Movements & Stock, enrichment'
 3. ZC_MM_INV_GDSMNV, 'MM: Goods Movements & Stock'
 4. ZQ_MM_INV_GDSMNV, 'MM: Goods Movements & Stock, 1 period'

Run ZQ-views in app "Query Browser".


