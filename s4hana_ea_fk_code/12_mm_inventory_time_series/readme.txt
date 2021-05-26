Following layered structure of CDS-views needs to be activated:

ZQ_MM_INV_STOCK_TS/TURNOVER                      - Query-views
|- ZC_MM_INV_STOCK_TS                            - Cube-view
   |- ZP_MM_INV_STOCK_TS                         - Aggregation, enrichment
      |- ZP_P_MaterialStockTimeSeries1 (union)   - Link stock to time series
         |- ZP_I_MaterialStockPeriodsSingl (4x)  - Period type as parameter
         |  |- ZP_P_MaterialStockPeriods (union) - Periods (F,Y,Q,M,W,D,P) based on parameters start/end date
         |     |- I_FiscalCalendarDate (1x:F)
         |     |- P_MaterialStockFYVariant
         |     |- I_SAPClient (dummy,6x)
         |     |- I_CalendarDate (5x:Y,Q,M,W,D)
         |     |- ZP_CA_DATE_PLFWIM (P)
         |- ZP_I_MaterialStock_Aggr (3x)         - Stock increase since start of 1st period
         |  |- ZB_I_MaterialDocumentRecord       - Basic view with mapping of field names
         |     |- matdoc                         - Source table Material Documents
         |- ZP_P_MaterialStockByKeyDate1         - Stock level at start of 1st period
            |- ZP_I_MaterialStock_Aggr
               |- ...

Below, CDS-views of which first name and then description are given.

Steps for each CDS-view:
a. in IDE start "New Data Definition",
b. enter name and description,
c. copy text from file [name].txt,
d. paste into editor of IDE,
e. activate.

CDS-views (in order):
 1. ZB_I_MaterialDocumentRecord, 'MM: I_MaterialDocumentRecord (enh.)'
 2. ZP_I_MaterialStock_Aggr, 'MM: I_MaterialStock_Aggr (enhanced)'
 3. ZP_P_MaterialStockByKeyDate1, 'MM: ZP_P_MaterialStockByKeyDate1 (copy)'
 4. ZP_CA_DATE_PLFWIM -> files and instructions in folder "08_complex_logic_exercise"
 5. ZP_P_MaterialStockPeriods, 'MM: P_MaterialStockPeriods (enhanced)'
 6. ZP_I_MaterialStockPeriodsSingl, 'MM: I_MaterialStockPeriodsSingle (copy)' (**)
 7. ZP_P_MaterialStockTimeSeries1, 'MM: P_MaterialStockTimeSeries1 (enh.)' (**)
 8. ZP_MM_INV_STOCK_TS, 'MM: Stock Time Series' (**)
 9. ZC_MM_INV_STOCK_TS, 'MM: Stock Time Series' (**)
10. ZQ_MM_INV_STOCK_TS, 'MM: Stock Time Series - Data' (**)
11. ZQ_MM_INV_STOCK_TURNOVER, 'MM: Stock - Turnover' (**)

Run ZQ-views in app "Query Browser".

(**) "P_PeriodType : nsdm_period_type" provides search help for all period types except the new one: 'P'.
     Copy and modify "nsdm_period_type" to obtain search help also for 'P'.


