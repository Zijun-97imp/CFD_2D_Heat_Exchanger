# CFD_2D_Heat_Exchanger

## The heat-exchanger transferom through circular cylinder structure. Using Fortran language.

### The below content is presenting the questions:

+ Run a first simulaƟon with Re = 200 (line 646 of the 2D_compressible.f90 file) and nx × ny = 129 × 129 for
  nt = 10000 Ɵme steps with a second order Adams-Bashforth scheme (itemp=1) and a CFL equal to 0.25 (line 48 of
  the 2D_compressible.f90 file). Generate 4 visualisaƟons of the vorƟcity field for nt = 2500,5000,7500,10000.
  Briefly comment on the results in less than 100 words. (Note : The code should be configured for this question,
  no changes are needed).


+ We want to increase the CFL number in order to reduce the cost of the simulaƟon. Using the same second order
  Adams-Bashforth scheme (itemp=1), is it possible to run a simulaƟon with a CFL of 0.75? 
  If yes, generate 4 visualisaƟons of the vorƟcity field for nt = 2500,5000,7500,10000 and briefly comment on the 
  results in less than 100 words. If not, try to explain why in less than 100 words.


+ Complete the subrouƟne rkutta in which a third-order Runge-KuƩa scheme will be used for the Ɵme advancement 
  (use the skeleton provided in the code). The scheme is described in secƟon 4.3. Run a simulaƟon with the same 
  parameters as in the first simulaƟon but with a CFL=0.75 and the newly implemented third-order RungeKuƩa sche
  me (itemp=2, line 38 of the 2D_compressible.f90 file)). Generate 4 visualisaƟons of the vorƟcityfield for 
  nt = 2500,5000,7500,10000. Briefly comment on the results in less than 100 words and copy-paste the
  subrouƟne rkutta in your report.

+ We want to use centered fourth-order schemes for the first and second derivaƟves in the two spaƟal direcƟons.
  Write four new subrouƟnes, using the skeletons provided in the code : derix4, deriy4, derxx4 and deryy4.
  In the subrouƟne fluxx, replace the second-order first and second derivaƟves with the new fourth-order ones.
  Then run a simulaƟon with same parameters as the first simulaƟon (question 1) but with the new the fourthorder 
  schemes. Generate 4 visualisaƟons of the vorƟcity field for nt = 2500,5000,7500,10000. Briefly commenton the 
  results and discuss the differences (if any) with the first simulaƟon (quesƟon 1) in less than 100 words.
  Copy-paste the four new subrouƟnes in your report. 

+ 6. Modify the code in order to simulate a single cylinder on a domain Lx ×Ly = 20d ×12d, with nx ×ny = 513×257
  mesh nodes and with inflow/ouƞlow boundary condiƟons in the streamwise direcƟon. You will have to modify
  the derivaƟve subrouƟnes derix and derxx to account for the new inlet/outlet boundary condiƟons (periodic
  boundary condiƟons are not relevant anymore, the use of non-centered schemes for the first and last points can be
  an opƟon). You may want to create a new subrouƟne boundary to impose the inlet and outlet boundary condiƟons
  in the streamwise direcƟon. Inlet and oulet boundary condiƟons need to be imposed for rho, rou, rov, roe and
  scp. For the inlet boundary condiƟon, you can look at the subrouƟne initl and use the same profiles for i = 1.5
  For the outlet boundary condiƟon, you can use a simple 1D convection equation:

                                            * ∂ϕ/∂t + Uc(∂ϕ/∂x) = 0 *
                                           
  where ϕ is the quanƟty to be convected at a speed Uc = U0 outside of the computaƟonal domain. To solve this
  equaƟon, you can use an Euler scheme for the Ɵme derivaƟve and a first order scheme for the spaƟal derivaƟve.
  For this final simulaƟon, you can use the same parameters of the first quesƟon : Re = 200, CFL=0.25, second order
  Adams-Bashforth scheme for Ɵme advancement, same iniƟal condiƟon. The post-processing tools will have to
  be change in order to generate 2 visualisaƟons of the vorƟcity (see examples in figure 3). Copy-paste the new
  subrouƟnes derix and derxx as well as the new subrouƟne boundary. 













