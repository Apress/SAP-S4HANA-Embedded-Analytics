Below, CDS-views of which first name and then description are given.

Steps for each CDS-view:
a. in IDE start "New Data Definition",
b. enter name and description,
c. copy text from file [name].txt,
d. paste into editor of IDE,
e. activate.

CDS-views (in order):
1. ZB_LOG_AUFK_JEST, 'LOG: Data for UserStatus Order' - adapt data restriction on "Status Profile" to your situation
2. ZP_LOG_AUFK_JEST, 'LOG: Data for UserStatus Order'
3. ZP_LOG_AUFK_JEST_Ag, 'LOG: Data for User Status Order, aggr.'
4. ZP_LOG_AUFK_JEST_Str, 'LOG: Data for User Status Order, string'
5. ZP_LOG_AUFNR_UserStat, 'LOG: User Status of Order'
6. ZC_MM_RetList, 'MM: Return List (cube)' - or modify the version you already have
7. ZQ_MM_RetList, 'MM: Return List'        - or modify the version you already have

Run ZQ-view in app "Query Browser".
