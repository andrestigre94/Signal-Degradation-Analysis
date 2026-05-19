# Signal Degradation Analysis

This will be the repository with the data and analysis for the Final Project of DS4EEB class with Malin Pinsky

**Authors: Andrés Felipe Tigreros Andrade**

## Background and rationale

Acoustic signals are a major channel of information transfer in birds, mediating decisions related to foraging, reproduction, and predator avoidance (Danchin et al. 2004; Seppänen et al. 2007; Goodale et al. 2010). In mixed-species flocks (MSFs), individuals routinely attend to heterospecific cues, and vocal communication can contribute to cohesion and collective anti-predator behavior (Sridhar et al. 2009; Goodale et al. 2010).

However, the transfer of acoustic information is constrained by physical degradation during propagation through space. As calls travel, attenuation, scattering, and reverberation reduce detectability and can distort temporal and spectral structure (Wiley & Richards 1978; Richards & Wiley 1980). These effects can be especially strong in forests, where vegetation and atmospheric conditions influence reverberation and attenuation in frequency-dependent ways (Morton 1975; Marten et al. 1977). As distance increases, receivers experience increasing uncertainty about signal structure and source location, so the reliability and value of social information decreases with distance, with implications for ranging, eavesdropping, and community-wide information flow (McGregor 1993; Seppänen et al. 2007).

While distance-related degradation has been studied extensively in territorial contexts (Morton 1975; McGregor 1993; Naguib 2003), fewer studies have tested how degradation shapes responses to alarm calls, despite their central role in survival and predator avoidance (Lima & Dill 1990; Magrath et al. 2015). Alarm calls can encode predator information that is usable by heterospecifics, making them key social-information signals in avian communities (Magrath et al. 2009; Magrath et al. 2015). Yet empirical tests remain limited regarding how quickly alarm-call effectiveness decays with distance in natural flock systems, and whether decay differs among species that vary in signalling roles or call structure.

Species differences in vocal amplitude, acoustic structure, and signalling function can affect transmission and detection (Morton 1975). In Amazonian understory MSFs, sentinel-like “information hub” species may disproportionately shape flock behavior and cohesion (Goodale & Kotagama 2005; Sridhar et al. 2009). In particular, Thamnomanes antshrikes often serve as sentinels and key sources of alarm information (Munn & Terborgh 1979; Martínez et al. 2018). Playback work also suggests that reliance on heterospecific alarms varies among species and ecological roles (Martínez & Zenil 2012). Understanding how alarm-call information degrades with distance and differs among callers is therefore important for quantifying the spatial footprint of information available to flocks and nearby community members (Magrath et al. 2015).

### **Study system and experimental design**

This dataset contains behavioral responses of the Long-winged Antwren (Myrmotherula longipennis), a common understory flock participant, to standardized alarm-call playbacks produced by three flocking species:

1.  Dusky-throated Antshrike (THAARD)

2.  Bluish-slate Antshrike (THASCH)

3.  White-flanked Antwren (MYRAXI)

Playbacks were broadcast at four distance treatments: 10, 20, 30, and 40 m from the focal individual. Some trials used a control playback (CONTRL).

### Study site

Fieldwork was conducted at Cocha Cashu Biological Station, Manu National Park, southeastern Peru (Madre de Dios; \~11.9° S, 71.4° W). Trials occurred across a heterogeneous mosaic including seasonally flooded floodplain (várzea) forest and adjacent terra firme habitat, within the station’s trail network.

### Playback preparation

Playback stimuli were constructed from alarm-call recordings previously obtained and processed in RStudio (R Core Team, 2025) using tuneR (Ligges et al. 2023), seewave (Sueur et al. 2008), and warbleR (Araya-Salas & Smith-Vidaurre 2017). Files were band-pass filtered (FIR) between 1.5–10 kHz, amplitude-normalized, exported at 24-bit resolution, and standardized to comparable note-call lengths.

### Playback trials (field protocol)

Experiments were conducted Aug 17 – Sept 18, 2025. Flocks were located by typical movement vocalizations. After confirming M. longipennis presence, flock composition was recorded for 10 minutes. Each trial included:

1.  5 min pre-trial baseline observation,

2.  30 s narrated pre-playback behavior recording,

3.  playback broadcast, and

4.  5 min post-trial observation.

A two-observer protocol was used: observer 1 tracked the focal bird and recorded behavior; observer 2 (aware of treatment) positioned the speaker (JBL Charge 5) at the assigned distance using a rangefinder.

### Behavioral response coding

The outcome variable captures the immediate response of the focal individual at the start of the post-trial window, coded as a categorical response class:

- Dive (rapid downward movement into cover)

- Freeze (sudden immobility)

- Look around (increased vigilance/scanning)

- Call back (immediate vocal response interpreted as alarm calling)

- No response (no observable change relative to baseline)

In this dataset, the “true” response is stored as an integer code (see RPTA(true) below), and a binary indicator (RPTA(bin)) flags whether any response occurred versus no response.

## File: finalized_playbacks.csv

**Dataset** description for `finalized_playbacks.csv`

**Authors:** Andrés Felipe Tigreros-Andrade, Jorge Novoa, Daniel T. Blumstein, Ari E. Martínez

### Unit of observation

One row = one playback trial conducted on a focal Myrmotherula longipennis individual within an MSF, with an associated playback treatment (caller identity × distance) and an immediate behavioral response.

### Target audience of this project:

The targeted audience foreseen for this project is the academic community. This in order to prepare the analysis of this dataset to be published in a peer-reviewed journal, maybe Animal Behavior.
