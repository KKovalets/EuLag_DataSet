Here are presented measurements data collected for the latitude band of 20-30◦N in the Atlantic and Pacific Oceans and 50-60◦S of the Southern Ocean, which were used in the simulation process in EuLag model or verification of its modeling results. 

Following profiles are presented here:

1) The averaged profiles of temperature and oxygen for the Pacific, Atlantic and Southern Oceans, obtained using measurements data collected by (Boyer et al., 2018).
In corresponding files the first column is Z-coordinate measured in meters (m), and the second is temperature in ◦C or oxygen concentration in kg/m^3.
These profiles were used in calculations as input data. 
To perform the simulation for one specific ocean, user must take the corresponding temperature and oxygen files from this repository and place them into the project folder, where executable file and other input files are also present. Then filenames must be changed as "Temperature.dat" for file with the temperature profile and "O2 concentration.dat" for file with the oxygen profile. 
For correct performance user also must change n_data1 (the number of data rows in temperature profile) and n_data2 (the number of data rows in oxygen profile) in the Input.nml. These parameters should be set to the number of lines contained in the corresponding data-files. 
Parameters Z_measur and Sp_measur in the Input.nml must also be changed depending on which ocean data are used in modeling (see paragraph 2).

2) POM concentrations and fluxes profiles, which were given for the Atlantic Ocean in (Aumont et al., 2017) and (Lutz et al. , 2002), for the Pacific Ocean in (Martin et al., 1987) and (Druffel et al., 1992) and for the Southern Ocean in (Aumont et al., 2017) and (Lutz et al., 2002). 
In the corresponding files the first column is Z-coordinate measured in meters (m), and the second is POM concentration measured in kg/m^3 (Sp) or POM flux (Fd) in kg/m^2/s.
In our simulations measurements of POM concentrations (Sp) in the upper layer of euphotic zone were used as the input data, defined as Z_measur and Sp_measur variables in the Input.nml file. So, if the user wants to perform the same simulations for some specific ocean, he must open the corresponding file with POM concentration profile in this ocean and take the highest measurment from here. Then set the Z_measur as rounded to the nearest integer Z-coordinate and Sp_measur as corresponding POM concentration value. For example, the highest measurement in "Atlantic POM concentration (Sp).dat" file is Z = 94.10133, POM concentration = 5.59821E-06. To perform simulations for the Atlantic Ocean we set parameters as Z_measur=94., Sp_measur=5.59821E-06.
It should be noted that in general it's not necessary to round Z-coordinate, if user doesn't want to. But in our simulations we did so, as far as we found it convenient, and it need to be done to reproduce our results in the most correct way.
User can also use POM flux measurments as a parameter instead of concentration. To do this, set the Sp_measur=0. and assign the Z_measur and Fd_measur parameters the corresponding values of the highest measurement from POM flux file. We didn't do it in our calculations, but we gave the user an opportunity to do it.
We also used POM fluxes and concentrations to compare them with our calculations and make the sensitivity study.
 
Data references:
1. Aumont, O., van Hulten, M., Roy-Barman, M., Dutay, J.-C., Éthé, C., and Gehlen, M.: Variable reactivity of particulate organic matter in a global ocean biogeochemical model, Biogeosciences, 14, 2321–2341, https://doi.org/10.5194/bg-14-2321-2017, 2017.

2. Boyer, T.P., Baranova,O.K., Coleman, C. , Garcia, H.E., Grodsky, A., Locarnini, R.A., Mishonov, A.V. , Paver, C.R., Reagan, J.R., Seidov, D., Smolyar, I.V., Weathers, K., and Zweng,M.M.: World Ocean Database 2018. A.V. Mishonov, Technical Ed., NOAA Atlas NESDIS 87. https://www.ncei.noaa.gov/sites/default/files/2020-04/wod_intro_0.pdf, 2018.

3. Druffel, E., Williams, P., Bauer, J., and Ertel, J.: Cycling of dissolved and particulate organic matter in the open ocean, J. Geophys. Res., 97, 15639–15659, https://doi.org/10.1029/92JC01511, 1992.

4. Lutz, M. J., Dunbar, R. B., and Caldeira, K.: Regional variability in the vertical flux of particulate organic carbon in the ocean interior, Global Biogeochem. Cycles, 16, 1037, https://doi.org/10.1029/2000GB001383, 2002.

5. Martin, J., Knauer, G., K., D., and Broenkow, W.: VERTEX: carbon cycling in the northeast Pacific, Deep-Sea Res., 34, 267–285, 1987.
