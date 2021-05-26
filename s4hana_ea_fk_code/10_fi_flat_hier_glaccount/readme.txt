Below, CDS-views of which first name and then description are given.

Steps for each CDS-view:
a. in IDE start "New Data Definition",
b. enter name and description,
c. copy text from file [name].txt,
d. paste into editor of IDE,
e. activate.

CDS-views (in order):
1. ZB_FI_RACCT_HIER_PAR, 'FI: Data for G/L Account Hierarchy' - Adapt "Controlling Area" (ska1.ktopl)
2. ZP_FI_RACCT_HIER_PAR, 'FI: Data for G/L Account Hierarchy'
3. ZA_FI_RACCT_HIER_PAR, 'FI: G/L Account Hierarchy'
4. ZT_FI_ERGSL_NS00, 'FI: Fin.Statement Version text NS00'    - Adapt "Financial Statement Version" (versn)

Run views ZA_FI_RACCT_HIER_PAR and ZT_FI_ERGSL_NS00 as data preview in IDE and check results.
See Chapter 6, section "Author-Delivered Content", subsection "Flattened Hierarchies"
for application of these codes.
Both views are used in the stack of CDS-views in folder "13_fi_act_plan_com"
and can be tested via the query-view in the same folder.

