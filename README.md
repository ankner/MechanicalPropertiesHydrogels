# MechanicalPropertiesHydrogels
Excel sheets accompanying the publication "Controlling mechanical properties via architecture of poly(methacrylic acid) hydrogels"
Excel sheets implementing LbL Hydrogel fitting

The Excel sheets in this archive accompany the manuscript "Controlling mechanical properties via architecture of poly(methacrylic acid) hydrogels",Maksim Dolmat, John F. Ankner, and Eugenia Kharlampieva, which is currently in preparation (as of August 2022).

There are two sets of Excel sheets representing two samples: poly(methacrylic acid) (PMAA) crosslinked hydrogels deposited on silicon (Si) substrates using the hydrogen-bonded (HB) Layer-by-Layer (LbL) technique with poly(N-vinylpyrrolidone) (PVPON) serving as the binder, pre-crosslinking using: 1) 40 kDa PVPON and 2) 280 kDa 

40 kDa PVPON sheets:

layersWinParamMin_187282_UAB_0521_02_dry_final

layersWinParamMin_187303_UAB_0521_02_pH5.05_final

layersWinParamMin_187310_UAB_0521_02_pH6.55_final

layersWinParamMin_187387_UAB_0521_02_pH6.95_final

280 kDa PVPON sheets:

layersWinParamMin_187296_UAB_0521_04_dry_final

layersWinParamMin_187466_UAB_0521_04_pH5.05_final

layersWinParamMin_187473_UAB_0521_04_pH6.55_final

The Excel sheets use macros to calculate reflectivity, evaluate goodness-of-fit, and perform most other operations. They can therefore be viewed using open-source programs such as Gnumeric or LibreOffice, but they are only really functional when run in Excel with Macros enabled. Each sheet is independent of the others and contains all of the machinery needed to modify and optimize model fits. The sheets consist of a number of tabs, including:

Reflectivity tab:

This is the master sheet and contains the model parameters (columns B-H), data (columns I-K), model fit (column L), and fitted model scattering-length density (SLD) profile (columns M-S).  Data can be loaded from 3-column text files (the '#' symbol identifies commented lines not to be loaded) by typing two-fingered ctrl-l; reflectivity is evaluated by ctrl-r; and plotted data and fit display toggled between R and RQ^4 by ctrl-q. 

SLDs, absorptions, thicknesses and full-width-at-half-maximum (fwhm) interfacial widths are entered into or calculated in the labeled columns starting at row 3. Layers are added to the model and evaluated until the first blank row. We have primarily used column H for parameters used to calculate and populate the reflectivity columns, but these calculations can be done anywhere on the sheet. The calculations are described in detail in the Supplementary Information of the manuscript. The sheets are, however, not limited in function and the models can be modified or the sheets repurposed entirely to fit different data. Goodness-of-fit is given by chi-squared in cell A10.

Uncertainties tab:

The values and statistical uncertainties of model parameters shown on the Reflectivity tab and other relevant quantities are calculated and displayed here.

Uncertainties_DREAM tab:

The values and statistical uncertainties of model parameters fit using the DREAM algorithm available at ORNL.  Fitted models and data were ported from these sheets to take advantage of its more sophisticated treatment of parameter uncertainty.  All values result from independent fits to the data.

Fitted parameters tabs:

Each fitted parameter in the model has its own tab (e.g. density in layers_102384_SA_HB_Dry). Parameters are identified by which cell they occupy in the Reflectivity tab (cell A2 in the parameter tab) and can be varied through a range of values (Start, Stop, and Nsteps) in cells (B-D)2. Pressing ctrl-p evaluates the model over the desired range and fits a parabola to the chi-squared profile. Parameter minimum chi-squared and uncertainty are written in cells C4 and D4, respectively. For the sheets using incoherent smearing, ctrl-i carries out the parameter variation. New parameters can be added by copying, relabeling, and editing an existing parameter tab using standard Excel commands.

ScaledCombined tab:

A copy of the text file used to load in the data using the ctrl-l command in the Reflectivity tab. Data can also be cut and pasted into the relevant columns in the Reflectivity tab. Information on the ScaledCombined tab is purely documentary and does not affect the operation of the other features.

ScatteringParameters tab:

A neutron SLD calculator (using ActiveX so it won't work on Macs). Press the Compound Calculator button, enter values in the popup, and press Enter in the popup to add a line to the table. Cut and paste from columns D-F to appropriate columns C-E in the Reflectivity tab.

AtomicParameters tab:

The isotopic parameters used for the calculations in the ScatteringParameters tab (compiled by Varley Sears several decades ago).

This brief description is not in any way comprehensive, but feel free to contact the authors if questions or problems arise
