## TODO:

- Gather good papers/technical notes on muon physics in the IACT astronomy
- Build class Muon() that will have just overall physical information about this particle, together with some methods for calculating their main physical parameters.
- Add methods for interpolating atmosphere
- Add methods to calculate height of production in the simulations of muons for single CTA telescope
- Add file with constants (CTA Telescopes parameters, corsika/simtel main parametes, ...)


## Plan what code should looks like:

Create class Muon(), with all main muon parameters, constants and physical formulas.

-  Method to calculate muon flux/rate
-  Muon mass,
-  Cherenkov angle
-  Add method to interpolate atmosphere depthness

And subclasses: 

-  MuonDetector() - for describing how muon is interacting with iact detector

   - Use calibpipe to calculate optical efficiency
   - Methods to build different histograms, waveforms, show simulational parameters (realisation for one and many simtel files)
   - Distributions that can be found in Gaug file

-  MuonAtmosphere() - to describe how muon interacting in atmosphere

   - function for geomagnetic distortion of the muon
   - implement level-B requirements regarding muon fine physics


Interface should be done through simtel files.
