Probabilistic load flow analysis using Halton sequences in power systems with renewable resources

Filip Mišurović
*Faculty of Electrical Engineering*
*University of Montenegro*Podgorica, Montenegro
filip.misurovic@gmail.com

Saša Mujović
*Faculty of Electrical Engineering*
*University of Montenegro*Podgorica, Montenegro
sasam@ucg.ac.me

*Abstract*—Rising penetration of renewable resources in power systems through integration of distributed generation (DG) confronts traditional deterministic load flow (DLF) analysis with serious uncertainties and challenges. This claim is a direct consequence of variable energy production capability of the DGs whose operation strongly depends on weather conditions. The DLF approach gives only a snapshot of the state of the system at certain moment neglecting the all uncertainties arising from variable generation capabilities of DGs and volatility of consumption. Therefore, for the sake of such analyses another approach, namely, probabilistic load flow (PLF) should be adopted. The main issue regarding the application of PLF is the balance between method accuracy and efficiency. This paper is aimed to confirm the applicability of PLF method combining Monte Carlo simulations with Halton sequences for the modern power systems with integrated renewable generation. To that end, modified IEEE 30 bus test system was taken as a base for analysis and simulations, as well as deriving of key findings. Results have shown significant reduction of calculation time in comparison to basic Monte Carlo method, while keeping the precision of similar quasi-random techniques.

Keywords—Distributed generation, Halton sequence, Load flow, Monte Carlo methods, Probabilistic logic, Uncertainty.

# Introduction

Reliable supply of consumers with electrical energy of the prescribed quality is one of the basic goals of all power systems. Segmentation of vertically integrated electric power companies, as well as introducing of the electricity markets have additionally emphasized the importance of power quality and maintaining of voltage quality parameters within the requested range [1].

Modern trends in the development of electric power systems bring an increasing use of distributed generation (DG) based on renewable energy resources, conditioned by the requirements for reducing greenhouse gas emission and replacing of outdated conventional thermal power plants. Among renewable DGs, wind farms and solar power plants have the largest share in the energy mix [2]. The energy production capability of these sources is highly variable and depends on meteorological conditions, making them non-dispatchable units [3].

Bearing all previously listed in mind, it is pretty clear that with every new day modern power systems have less and less in common with the traditional power systems. In this regard, traditional, deterministic concept of power flow analysis (DLF), based on fixed values, can non yield an adequate accuracy of obtained results if applied on modern power systems. Simply, DLF does not take into account the uncertainties in electricity generation and consumption typical for the modern power systems with significant share of non-dispatchable units. In other words, the DLF can provide results which are valid only for a certain moment [4]. The application of a probabilistic load flow approach (PLF) could resolve this issue. Including uncertainties into calculation, the PLF application provides stochastic ranges of variables (e.g. bus voltages), what is opposed to the ranges of fixed values [5].

This paper deals with numerical PLF approach combining Monte Carlo simulations and Halton quasi-random numbers applied on modern power systems with renewable generators with clear intention to show its value considering fairly reduced number of simulations necessary for calculation in comparison to basic Monte Carlo PLF performed with simple random sampling (SRS) as well as sufficient accuracy compared to similar quasi-random methods, e.g. Latin Hypercube sampling (LHS). All analyses are performed in MATLAB, taking as a base IEEE 30 bus test system. This system is modified, i.e. supplemented with wind and solar generators, creating conditions which are distinctive for the modern power systems. The obtained results were compared and main conclusions were derived.

This work was supported through European Union’s Horizon 2020 research and innovation program under project CROSSBOW—CROSS BOrder management of variable renewable energies and storage units enabling a transnational Wholesale market (Grant No. 773430).

# Probabilistic load flow

Load flow analysis is very important for the purpose of planning, control and operation of existing, as well as planning the development of new parts of the power systems. Accordingly, the load flow analysis represents one of the most important calculations in the entire power engineering. The analysis includes determination of the modules and phase angles of the bus voltages, as well as calculation of active and reactive power in the transmission (distribution) lines. The requested input data are network configuration and related parameters, power consumption and rated power and characteristics of generators.

The traditional calculation of load flow is based on a deterministic approach. This approach takes as input variables the specific values of generation and consumption (most often the average expected values), while specific values of buses voltages provides as output. Based on the researchers' experience [6], input data values for some critical regimes may be analysed as well. The deterministic approach gives only a snapshot of the state of the system, ignoring the uncertainties arising from variable consumption or generation from renewable resources. This has imposed the need for a different approach in the load flow analysis and voltage quality analysis what is highlighted by the European standard EN-50160 [7]. The standard promotes and requires from distribution systems certain stochastic ranges of voltages, as opposed to the ranges of fixed values.

As a possible solution some authors have proposed the so-called stochastic calculation of load flow based on the assumption that the distributions of probabilities of the system states and the results of the load flow analysis are normally distributed. This assumption greatly simplifies the calculation, but it has been dismissed over years as very unreliable [8].

On the other hand, a PLF analysis can take into account uncertainties regarding network configuration, consumption, weather data related to generation capability of renewable resources, equipment failure rates etc. by the calculation based on the probability distribution of mentioned variables obtained through statistical analysis of their historical data. As a result, the states of the system (e.g. voltages) will be stochastically described too. The probabilistic approach to the calculation of load flow was first proposed in the mid-1970s [9], but has become especially popular after the growing penetration of renewable resources [10].

There are two groups of methods of probabilistic approach to the load flow calculation. Analytical methods based on the convolution of probability density functions and numerical methods performing a large number of DLF calculations using the Monte Carlo method.

Figure 1 presents the division of approaches to load flow calculation.



1. Load flow analysis approaches.

## Analytical methods

The basic idea of analytical methods is purely mathematical - to convolute the known probability density distribution functions of generated and consumed power and as a result to obtain the probability density distribution functions of the corresponding stochastic variable states of the system [11]. However, the load flow equations are nonlinear, and the input variables in different nodes of the network are often not completely independent, so the application of the convolution of probability functions implies certain approximations.

Thus, for the purposes of applying analytical techniques of PLF calculation, the following approximations are made: load flow equations are linearized, complete independence or linear dependence of input variables is assumed, normal and discrete distribution for generation and load is predicted and network configuration and parameters are assumed to be constant.

Linearization of load flow equations by developing equations in the Taylor series is basically performed for the average values of the input variables. It is clear that the accuracy of the results is worse for the values of the input variables that are far from the corresponding average values. These errors are especially problematic at the ends of the voltage distribution curve, which can lead to erroneous conclusions about the voltage quality in the network and consequently poor decisions regarding the system planning.

In order to mitigate the effects of linearization, numerous methods are used, among which is multilinearization, i.e. linearization of equations not only around the average value, but also around several other values. Slightly more efficient methods are point estimation methods [12], [13], cumulant methods [14], Gram-Charlie [15] and Cornish-Fischer distribution [16].

## Numerical methods

Numerical methods of PLF calculation represent the application of the Monte Carlo method. It is a procedure which consists of a stochastic simulation using random variables. Based on the calculated probability density functions of input variables, in this case the power consumption and generation from renewable resources, their values are randomly selected and then the DLF calculation is performed in accordance with values selected in this manner. The simulation needs to be repeated a sufficient number of times so that the obtained values (bus voltages) can be statistically processed and presented in the form of their probability density functions.

For DLF calculations, classical load flow methods like Newton-Raphson are usually used. There are applications of forward-backward sweep approach too [17], [18].

The main advantage of applying numerical methods is their precision which is a direct consequence of their ability to apply nonlinear equations to analyse the load flow in each iteration. The following system of equations applies [19]:

 

 

where *Pi* and *Qi* are the active and reactive power injected into node *i*, *Ui* and *Uk* voltage amplitudes at nodes *i* and *k*, θ*ik* the phase difference of the voltages at nodes *i* and *k*, *Gik* and *Bik* the real and imaginary part of the corresponding branch admittance matrix.

The basic Monte Carlo method is based on SRS. Its main drawback is the possibility of sampling a value very similar to the values in the previous iterations. This is the reason of extremely big number of iterations needed to cover the analysed set of numbers correctly. In order to improve the efficiency of calculations, quasi-random sampling methods based on low discrepancy sequences have been introduced.

One of them is LHS technique which samples one value from the specific interval and then removes that whole interval from further analysis. However, the usage of this sampling technique generates unwanted dependencies between sampled values. This is solved by various permutation methods, e.g. Cholesky decomposition [20]. In [21], LHS is combined with copula method which offers predefining the dependencies between random variables. Additionally, [22] analyses the application of correlation matrices which are not positively definite by combining Nataf transformation, LHS sampling and matrices decomposition to singular values.

Another quasi-random method is Latin Supercube sampling, presented in [23] that is the combination of LHS and digital nets. It has shown satisfactory accuracy [24].

Moreover, there are examples of application of Uniform Design sampling technique [25] and improved Sobol generator of quasi-random numbers [26]. Improvement of the efficiency of Monte Carlo method is also analysed through the application of non-parametric density estimations of load flow calculation results such as adaptive kernel [27] and Parzen Window density estimation [28]. Their advantage is the flexibility of modelling a certain set of data which cannot give analytical solution or the solution could be too complicated.

# Halton sequences

Halton sequence is one of the low-discrepancy sequences used for quasi-Monte Carlo simulations. It was first described in [29]. This sequence generalizes one-dimensional van der Corput sequence and is very easy to implement [30] because it is based on the radical inverse function:



where *p* is a prime number, and the *p*-ary expansion of *n* is given as *n* = *b*0 + *b*1*p* + ... + *bmpm*, with integers 0 ≤ *bj*< *p*.

The Halton sequence, *Xn*, in *s*-dimensions is then defined as:



where the dimensional bases *p*1, *p*2,...,*p*s are pairwise coprime. In real calculations, the first *s* primes are used as the bases.

# Case study

For the purpose of simulating the application of Monte Carlo PLF methods (SRS, LHS and Halton sequences), as well as for the comparison of obtained results, the IEEE test system of 30 nodes was considered [31]. The system has been modified by attaching additional wind and solar generators to specific bus loads. Two wind and one solar generator are modelled as negative load and attached to buses 5, 20 and 8 of the test system respectively.

## Modeling uncertainties

### Load model: The load was stochastically modeled by the normal distribution [32], taking the deterministic value of the load as the mean value and 5 percent of the assumed mean value as the value of the standard deviation. Therefore, the probability density function of load can be expressed as:

 

where *x* is the bus load, µ the mean value and σ the standard deviation of load.

### Wind speed and generator model: For purposes of this simulation, real hourly wind speed data were used. They had been taken from the online historical weather reports [33], for the period of two weeks, for the site Krnovo (meteorologically interesting area in Montenegro, altitude - 1500 m), at the height of 80 metres above the ground.

Firstly, the histogram representing wind speed was created using the Distribution Fitting Tool in the MATLAB software package. Secondly, the wind speed was stochastically modelled by the Weibull distribution [34] and the parameters of scale and shape of the probability distribution density function were obtained. The histogram with the modelled wind density probability distribution function obtained through MATLAB Distribution Fitting Tool is given in Figure 2.



1. Histogram and modeled wind speed probability density distribution function.

Rated power of wind generator is chosen considering voltage level and size of used IEEE test system. Appropriate characteristics of an average onshore wind generator are selected based on rated power. These characteristics are shown in Table 1.

The output power of wind generator *P* is determined by the formula (6):

 

where *v* is wind speed, *vin* cut-in speed, *vout* cut-out speed, *vr* rated wind generator speed, *Pr* rated wind generator power, *Cp* power coefficient, ρ air density and *A* surface affected by wind.

1. Wind generator characteristics

| Parameters | Values | Parameters | Values |
| --- | --- | --- | --- |
| Rated power | 2.8 MW | Blade length | 50 m |
| Rated speed | 12 m/s | Altitude | 1500 m |
| Cut-in speed | 2.5 m/s | Power coefficient | 0.4 |
| Cut-out speed | 25 m/s | Power factor | 0.95 |

### Solar generator model: For purposes of modelling solar irradiance and generator power output based on real data, online tool NREL’s PWVatts [35] has been used. Hourly values of irradiance, temperatures and eventually power output covering one year for the area in central Montenegro have been taken into consideration. Characteristics of the solar generator are shown in Table 2.

1. Solar generator characteristics

| Parameters | Values | Parameters | Values |
| --- | --- | --- | --- |
| DC System Size | 4 MW | System Losses | 14.08% |
| Temperature Coefficient of Power | -0.47 %/°C | DC to AC Size Ratio | 1.2 |
| Approximate Nominal Efficiency | 15% | Inverter Efficiency | 96% |

## Simulation algorythm

First, 100 000 values of consumption, wind and solar generation data are sampled by SRS and used for the same number of DLF calculations by applying the Newton-Raphson method in the MATPOWER simulation tool in MATLAB software package. The obtained results of the DLF calculation are stored after each iteration and eventually statistically modelled by the normal probability distribution based on the calculated mean values and the values of the standard deviation. They are considered to be reference values for further simulations.

Then, specified number of stochastic variable values *N* is sampled three times, by SRS, LHS and Halton quasi-random sampling method. All of these datasets are used for DLF calculation in each of iterations. Results are compared with reference values and relative error is calculated as follows:

 

where xref is reference value calculated after 100 000 iterations and is output value obtained after *N* iterations.

It is important to notice that LHS and Halton method, as quasi-random, always give the same result for the specific number of iterations, while SRS as random method, gives different values. Therefore, each SRS simulation is repeated for 100 times in order to get mean relative error.

Several simulation scenarios with datasets consisting of 50, 100, 250, 1 000 and 10 000 values were considered in order to assess the accuracy and calculation time of all three sampling techniques and eventually to examine methods’ applicability in real life system analysis.

Figure 3 shows the algorithm of the applied program.



1. Scheme of probabilistic load flow algorithm.

The simulations were performed on HP Pavilion device with Intel Core i-5, 2.5 GHz processor and 8 GB RAM, using the MATLAB software package, version 2016a.

# Results

To compare the results of application of PLF calculation performed with input values obtained by different sampling methods, three subtypes of simulations have been performed for five above-mentioned datasets/iteration sizes: the first based on SRS, the second on LHS and the third on Halton quasi-random numbers. Figure 4 shows mean relative errors of voltages at nodes 18 and 29 obtained after three subtype simulations – SRS, LHS and Halton respectively, for all proposed numbers of iterations.





1. Comparison of voltage value relative errors at nodes 18 and 29.

After adding wind and solar generators to certain buses of the analysed test system, a problem in the form of voltage increase is expected in nearby nodes, except in the buses connected to conventional generators and compensators.

If, based on the simulation results, we observe the values of relative errors of voltages obtained by calculation performed with SRS or quasi-random sampling, it is clear that the latter approach gives a more realistic picture of the state of the system after the reasonably small amount of iterations.

For example, let’s consider the voltage value at bus 18 of IEEE 30 bus system. At first the relative error of calculated voltage is almost 20 times bigger after applying SRS method in contrast to quasi-random sampling. Even after 1000 of iterations the error of SRS method is over 6 times bigger. It is worth mentioning that after the smallest number of simulated iterations – 50, quasi-random methods offer the values approximate to the reference ones. Similar conclusion can be drawn if we consider relative error of voltage at bus 29. The ratio of above mentioned results is 23:1 after 100 iterations and 6:1 in case of 1000 iterations. This indicates clear benefits of Halton-based sampling used for PLF approach to power systems with lots of renewable resources.

Moreover, it is worth mentioning that Halton-based sampling method is slightly less precise for the lowest number of iterations. For 100 iterations and above, both analysed quasi-random methods, LHS and Halton sampling give similarly accurate results.

Table 3 presents calculation time in seconds required for execution of analysed simulation scenarios.

1. Calculation time for different scenarios

| It. | SRS | LHS | Halton | It. | SRS | LHS | Halton |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 50 | 0,47 | 2,84 | 2,43 | 1000 | 4,52 | 10,11 | 6,48 |
| **100** | 3,13 | 3,18 | 2,58 | 10000 | 83 | 82 | 47,7 |
| **250** | 1,32 | 4,31 | 3,26 | 100000 | 1081 | - | - |

It can be observed that calculation time is generally similar between three analysed methods. However, for the duration below 10 seconds, methods with LHS and Halton sampling are more acceptable in terms of results precision.

# Conclusions

In this paper, three numerical methods for probabilistic load flow calculation, SRS, LHS and Halton quasi-random sampling, were compared when applied to modern power systems which contain various uncertainties regarding the generation from renewable resources. It was concluded that the SRS-based approach is pretty much unusable in terms of accuracy, when applied for quick probabilistic analysis performed by small number of iterations. As an example of the confirmation of this view, several simulations were performed on IEEE 30 bus test system to which additional wind and solar generators were attached. The results confirmed that the relative error of bus voltage is significantly less if the quasi-random sampling is applied, supporting the claim of its superiority over basic Monte Carlo approach based on SRS. On the other hand, Halton sampling has proven competitive enough in comparison to LHS and has validated the effectiveness of its usage for the load flow analysis, voltage quality assessment and planning of modern power system.

Furthermore, performed simulations imply that dominance of Halton sampling could be even more noticeable for bigger systems and systems with large number of DGs that would require more calculation time per iteration. This indicates its ability of mass practical use for real systems as an indispensable tool in power system development.

##### References

1. M. Sencar, V. Pozeb and T. Krope, “Development of EU (European Union) energy market agenda and security of supply,” *Energy*, Volume 77, 2014, Pages 117-124, <https://doi.org/10.1016/j.energy.2014.05.031>.
2. REN21. 2020. Renewables 2020 Global Status Report (Paris: REN21 Secretariat). Available online: https://www.ren21.net/wp-content/uploads/2019/05/gsr\_2020\_full\_report\_en.pdf (accessed on 1 October 2020)
3. A.T.D. Perera, V. M. Nik, D. Mauree *et al*., “Electrical hubs: An effective way to integrate non-dispatchable renewable energy sources with minimum impact to the grid,” *Applied Energy*, Volume 190, 2017, Pages 232-248, <https://doi.org/10.1016/j.apenergy.2016.12.127>.
4. S. Conti and S. Raiti, “Probabilistic Load Flow for Distribution Networks with Photovoltaic Generators Part 1: Theoretical Concepts and Models,” 2007 International Conference on Clean Electrical Power, Capri, 2007, pp. 132-136, <https://doi.org/10.1109/ICCEP.2007.384199>.
5. A. Zakaria, Firas B. Ismail, M.S. Hossain Lipu *et al*., “Uncertainty models for stochastic optimization in renewable energy applications,” Renewable Energy, Volume 145, 2020, Pages 1543-1571, <https://doi.org/10.1016/j.renene.2019.07.081>.
6. J. M. Sexauer and S. Mohagheghi, “Voltage Quality Assessment in a Distribution System With Distributed Generation—A Probabilistic Load Flow Approach,” in IEEE Transactions on Power Delivery, vol. 28, no. 3, pp. 1652-1662, July 2013, <https://doi.org/10.1109/TPWRD.2013.2259599>.
7. Voltage characteristics of electricity supplied by public distribution systems, EN 50160, CENELEC
8. P. Chen, Z. Chen and B. Bak-Jensen, “Probabilistic load flow: A review,” 2008 Third International Conference on Electric Utility Deregulation and Restructuring and Power Technologies, Nanjing, 2008, pp. 1586-1591, <https://doi.org/10.1109/DRPT.2008.4523658>.
9. B. Borkowska, “Probabilistic Load Flow,” in IEEE Transactions on Power Apparatus and Systems, vol. PAS-93, no. 3, pp. 752-759, May 1974, <https://doi.org/10.1109/TPAS.1974.293973>.
10. B. R. Prusty and D. Jena, “A critical review on probabilistic load flow studies in uncertainty constrained power systems with photovoltaic generation and a new approach,” Renewable and Sustainable Energy Reviews, Volume 69, 2017, Pages 1286-1302, <https://doi.org/10.1016/j.rser.2016.12.044>.
11. R. N. Allan, B. Borkowska and C. H. Grigg, “Probabilistic analysis of power flows,“ *Proceedings of the Institution of Electrical Engineers*, Volume 121, no. 12, pp. 1551-1556, December 1974, <https://doi.org/10.1049/piee.1974.0320>
12. F. Diop and M. Hennebel, “Probabilistic load flow methods to estimate impacts of distributed generators on a LV unbalanced distribution grid,” *2017 IEEE Manchester PowerTech*, Manchester, 2017, pp. 1-6, <https://doi.org/10.1109/PTC.2017.7981107>.
13. Y. Che, X. Wang, X. Lv *et al*., “Probabilistic load flow using improved three point estimate method,” *International Journal of Electrical Power & Energy Systems*, Volume 117, 2020, 105618, <https://doi.org/10.1016/j.ijepes.2019.105618>.
14. X. Deng, P. Zhang, K. Jin, *et al*., “Probabilistic load flow method considering large-scale wind power integration”, *Journal of Modern Power Systems and Clean Energy*, 7, 813–825, 2019, <https://doi.org/10.1007/s40565-019-0502-0>
15. P. Zhang and S. T. Lee, “Probabilistic load flow computation using the method of combined cumulants and Gram-Charlier expansion,” in *IEEE Transactions on Power Systems*, vol. 19, no. 1, pp. 676-682, Feb. 2004, <https://doi.org/10.1109/TPWRS.2003.818743>
16. J. Usaola, “Probabilistic load flow with wind production uncertainty using cumulants and Cornish–Fisher expansion,” *International Journal of Electrical Power & Energy Systems*, Volume 31, Issue 9, 2009, Pages 474-481, <https://doi.org/10.1016/j.ijepes.2009.02.003>
17. W. Ahmed, S. Kamel and F. Jurado, “Probabilistic load flow analysis for large scale radial distribution systems,” *2016 Eighteenth International Middle East Power Systems Conference (MEPCON)*, Cairo, 2016, pp. 803-808, <https://doi.org/10.1109/MEPCON.2016.7836986>
18. F. Jabari, M. Shamizadeh and B. Mohammadi-Ivatloo (2020) “Probabilistic Power Flow Analysis of Distribution Systems Using Monte Carlo Simulations”. In: M. Pesaran Hajiabbas and B. Mohammadi-Ivatloo (eds) *Optimization of Power System Problems*. Studies in Systems, Decision and Control, vol 262. Springer, Cham. <https://doi.org/10.1007/978-3-030-34050-6_10>
19. A. G. Anastasiadis, E. Voreadi and N. D. Hatziargyriou, “Probabilistic Load Flow methods with high integration of Renewable Energy Sources and Electric Vehicles - case study of Greece,” *2011 IEEE Trondheim PowerTech*, Trondheim, 2011, pp. 1-8, <https://doi.org/10.1109/PTC.2011.6019380>
20. H. Yu, C. Y. Chung, K. P. Wong, *et al****.*,** “Probabilistic Load Flow Evaluation With Hybrid Latin Hypercube Sampling and Cholesky Decomposition,” *IEEE Transactions on Power Systems,* May 2009, Vol. 24, 2, pp. 661-667, <https://doi.org/10.1109/TPWRS.2009.2016589>
21. D. Cai, D. Shi and J. Chen, “Probabilistic load flow computation using Copula and Latin hypercube sampling,” *IET Generation, Transmission & Distribution.* September 2014, Vol. 8, 9, pp. 1539-1549, <https://doi.org/10.1049/iet-gtd.2013.0649>
22. J. Zhang, G. Xiong, K. Meng, *et al*., “An improved probabilistic load flow simulation method considering correlated stochastic variables,” *International Journal of Electrical Power & Energy Systems*, Volume 111, 2019, Pages 260-268, <https://doi.org/10.1016/j.ijepes.2019.04.007>
23. T. Cui and F. Franchetti, “A Quasi-Monte Carlo approach for radial distribution system probabilistic load flow,” *2013 IEEE PES Innovative Smart Grid Technologies Conference (ISGT)*, Washington, DC, 2013, pp. 1-6, <https://doi.org/10.1109/ISGT.2013.6497894>
24. M. Hajian, W. D. Rosehart and H. Zareipour, “Probabilistic Power Flow by Monte Carlo Simulation With Latin Supercube Sampling,” *IEEE Transactions on Power Systems.* May 2013, Vol. 28, 2, pp. 1550-1559, <https://doi.org/10.1109/TPWRS.2012.2214447>
25. D. Cai, D. Shi and J. Chen, “Probabilistic load flow with correlated input random variables using uniform design sampling,” International Journal of Electrical Power & Energy Systems. December 2014, Vol. 63, pp. 105-112, <https://doi.org/10.1016/j.ijepes.2014.05.027>
26. L. Zhang, H. Cheng, S. Zhang, P. Zeng, L. Yao “Probabilistic power flow calculation using the Johnson system and Sobol’s quasi-random numbers,” IET Gener. Transm. Distrib., 2016, vol. 10, iss. 12, pp. 3050–3059, <https://doi.org/10.1049/iet-gtd.2016.0181>
27. N. Soleimanpour and M. Mohammadi, “Probabilistic Load Flow by Using Nonparametric Density Estimators,” IEEE Transactions on Power Systems. November 2013, Vol. 28, 4, pp. 3747-3755, <https://doi.org/10.1109/TPWRS.2013.2258409>
28. M. Rouhani, M. Mohammadi and A. Kargarian, “Parzen Window Density Estimator-Based Probabilistic Power Flow With Correlated Uncertainties,” IEEE Transactions on Sustainable Energy. July 2016, Vol. 7, 3, pp. 1170-1181, <https://doi.org/10.1109/TSTE.2016.2530049>
29. J. H. Halton (1960) “On the efficiency of certain quasi-random sequences of points in evaluating multi-dimensional integrals,” in *Numerische Mathematik*, 2(1), pages 84–90, <https://doi.org/10.1007/bf01386213>
30. G. Weerasinghe, H. Chi, Y. Cao (2016) “Particle Swarm Optimization Simulation via Optimal Halton Sequences,” in *Procedia Computer Science*, 80, 772–781. <https://doi.org/10.1016/j.procs.2016.05.367>
31. Power Systems Test Case Archive, University of Washington. Available online: <http://labs.ece.uw.edu/pstca/> (accessed on 1 April 2021)
32. R. Billinton and D. Huang, “Effects of Load Forecast Uncertainty on Bulk Electric System Reliability Evaluation,” in *IEEE Transactions on Power System*s, vol. 23, no. 2, pp. 418-425, May 2008, <https://doi.org/10.1109/TPWRS.2008.920078>
33. Meteoblue. Available online: <http://www.meteoblue.com> (accessed on 10 May 2021)
34. G. E. Constante-Flores and M. Illindala, “Data-driven probabilistic power flow analysis for a distribution system with Renewable Energy sources using Monte Carlo Simulation,” *2017 IEEE/IAS 53rd Industrial and Commercial Power Systems Technical Conference (I&CPS)*, Niagara Falls, ON, 2017, pp. 1-8, <https://doi.org/10.1109/ICPS.2017.7945118>
35. PVWatts® Calculator, The National Renewable Energy Laboratory (NREL). Available online: <https://pvwatts.nrel.gov/index.php> (accessed on 10 May 2021)