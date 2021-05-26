I_CalendarDate is a standard SAP CDS-view already existing in your S/4HANA system.

Below, CDS-views of which first name and then description are given.

Steps for each CDS-view:
a. in IDE start "New Data Definition",
b. enter name and description,
c. copy text from file [name].txt,
d. paste into editor of IDE,
e. activate.

CDS-views (in order):
1. ZB_CA_DATE_PLFWIM, 'CA: Data for Date PerLtstVolWkInMnd'
2. ZP_CA_DATE_PLFWIM_MO, 'CA: PerLtstVolWkInMnd for Mnth'
3. ZP_CA_DATE_PLFWIM, 'CA: PerLtstVolWkInMnd for Date'

Run view ZP_CA_DATE_PLFWIM as data preview in IDE and check results.
You can also check contents of SQL-view ZPCADATEPLFWIM via SE11 or SE16(N).
