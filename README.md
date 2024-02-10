## Plan what here should be:

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

