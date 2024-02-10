## Lets mark down what should be done and for what physics.


## So we have muons, and they undergo several changes of state from the perspective of view of the scientist and gamma-ray observatory. 

- ### Muon and atmosphere - first of all they born as secondary particles from CR interactions, and are flying through the atmosphere:
   - they have pure physics characteristic (mass,energy,direction?, flux/rate, speed, cherenkov angle, production height, attenuation length, energy loss, time of arrival, etc)
   - geometrical things - shape and size of the cherenkov cone, that would be good to know, timespan of the sygnal for different muon initial params
   - they interact with :
      - magnetic field (bending trajectory)
      - other particles
      - light which they produce undergo extinction (by molecules and aerosol) and scattering?
      
     
- ### Muon and Detector - then muons reach our detector (or at least light from their cherenkov cone):

   - There are quite big physical and technical background on the case how photons are transferred to the digital counts which we later process in analysis:
      - Photons are reflected from the mirror and create ring shape on the camera formed by pixels which was affected by light. Then this pixels produce signal which is translated to the photo electrons through ADC converter. Therefore we receive R0 waveforms. Then we should perform initial calibration and obtain R1 waveforms. Then we are applying cleaning,noise rejection and charge distraction - here we go with dl1 images.
      - First we perfom fit of the ring (2 methods + possible Hough transform)
         - figure out this things with different camera telescope etc coordinate systems 
      - Then we perform likelihood fitting of muon ring parameters - impact_parameter, phi, width and optical efficiency
         - need to check different implementation of this fit and be sure what is done in ctapipe
- ### Muon and Camera - more specific case of detector, because we have different types of cameras (LST, NectarCam, FlashCam, Astri - for each of them should be different approach)
         - Interesting idea here is to perform cross checks between cameras and how they process muons
   - When muon crossing the shadowing mast of telescopes, it can lose big part of the light - this should be handled.
   - Optical abberation in the correspondence of camera coordinates to incident angles.
   - Camera sensitivity to different incident angles
   - Camera shadowing
   - Finite camera focuses for muon analysis
   - Non-sphericity of the reflectors

- ### Muons and User - now, when we had correctly processed muon events we can get some information from them:
   
   - Build histograms and distributions based on input simtel/hdf5 tables
   - Build distributions of muon ring radius, width, impact parameter
   - Go further and reconstruct energy? (for real/simulated data)
   - and so on so forth.
  
        
