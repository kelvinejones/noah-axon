# noah-axon

Ia afferent collateral model used as Supplemental Figure S3 in GABA 
priming paper

HOW-TO RE-CREATE PANEL B
1) run "init.hoc" using nrngui
2) click "init&run" in the RunControl PANEL

HOW-TO RE-CREATE PANEL C (g_GABA = 0.6nS, 1.5nS, or 2.4nS)
1) run "init.hoc" using nrngui if not already done so
2) in the PointProcessGroupManager panel, ensure you are viewing the global
    specifications for the nodal GABA currents by clicking "PanelStyle" and
    then "Global Spec"
3) Adjust "gmax(µS)" to either 0.0006 (for 0.6µS), 0.0015 (for 1.5µS), or
    0.0024 (for 2.4 µS) and hit enter
4) click "init&run" in the RunControl PANEL
5) If desired, you can add recording traces to the graph for N4, N5, B1, and B2
    by right clicking and holding the graph whitespace, navigating to "Plot what?"
    with the cursor, and releasing the keypress. In the space provided write:
        FOR N4:
            Bout[18].v(0.5)+Bout[18].vext[0](0.5)
        FOR N5:
            Bout[30].v(0.5)+Bout[30].vext[0](0.5)
        FOR B1:
            Bout[35].v(0.5)+Bout[35].vext[0](0.5)
        FOR B2:
            Bout[23].v(0.5)+Bout[23].vext[0](0.5)
