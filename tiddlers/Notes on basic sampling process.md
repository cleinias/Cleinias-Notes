# Notes on sampling overall process

A collection of notes on how to proceed to produce playable 
samples, partially relevant to field recording as well.

  The general procedure

1. Plan 
2. Record –> REAPER plus mics
3. Denoise –> RX (Spectral De-noise filter)
4. Name, split, and save to individual files –> REAPER
5. Map to keys, fill blanks, tune, balance volumes, add round 
  robins and effects –> KONTAKT 
	
## Details

1. **Plan** 
  	1. Write description of the basic concept or goal
  	2. Figure out what to record (objects, instruments, etc.)
	  3. Figure out how many samples are needed, counting 
    round-robins, velocity layers, number of notes (e.g. may be 
    go for stacked major or minor thirds (= 3, resp. 4, notes per 
    octave), or just by stacked major fifths).
	  4. Use a matrix of this kind, for instance:
		
	|  Object    |   Method    | Range  | No. Samples  | Velocity Layers  | Round Robins  | Total |
	|------------|-------------|--------|--------------|------------------|---------------|--------|
	| Bass rec.  | Minor 3rds  | F3-G5  |      9       |        1         |      4        |  36   |
	||||||                                                                             Total:  |  36   |
2 **Record (REAPER)**

  1. All samples go into one file, if recorded in the same 
    sonically stable environment (to ease later cleanup)
  2. Always record a “silence” patch for later de-noising
  3. Use more than one mic, if possible
  4. Record into Reaper tracks
  5. Save each mic's track to a separate file
	
3 **Denoise (RX 11)**
  1. Duplicate tracks as backup
  2. Import tracks into RX11
  3. Choose SPECTRAL DE-NOISE filter
  4. Let the filter learn the noise to eliminate from the 
    silence patches at the end of the tracks
  5. Remove noise and save

4 **Name, split, and save to individual files (REAPER)**
  1. Reimport de-noised tracks into Reaper
	2. Group tracks
	3. SPLIT: find next transient with tab, then split with “s”
	4. SHORTEN clips, both at the tail and at the head (to allow 
    for the envelope's attack): 
	5. CREATE FADE OUTS: check out D Hilowitz video  <https://www.youtube.com/watch?v=B2iEhJcrHxI> at 6:17 in.
	6. NAME THE CLIPS: 
		1. create regions for each clips: reaper action command: “
      Insert separate region for each selected item”
		2. Pull up the region manager and name each region with the 
      note it represent, plus a serial # for round robins (Db.1, 
      Db.2, etc). 
	7. EXPORT the clips:
		1. Pull up Reaper's render matrix, select what to render
		2. Name the folder by tracks' name, choose a convenient 
      filename pattern
			
5 **Map to keys, fill blanks (KONTAKT)**
1. CREATE a new instrument in Kontakt
2. Open Kontakt's “MAPPING EDITOR” in the new instrument just 
    created
3. NAVIGATE to the saved folders/files
4. IF you have round robins, CREATE DUPLICATE GROUPS for how 
    many round robins you have (4, 5, etc)
5. IMPORT the clips into the appropriate groups (all 1's to 
    group 1, etc.) by:
	1. selecting the relevant files and,
	2. dragging them into the mapping area (in a random 
      location)
6. AUTOMAP the sample by using the relevant part of the 
    filename to be the key, e.g “My_instrument_D#_1” gets mapped 
    to D# and choosing “Set to Single key”
7. change the ROOT KEY of all zone to center in Batch tools >> 
    Move root key to center
8.  FILL THE GAPS for the missing notes, by selecting all zones 
    and then “Automap functions >> Auto-spread key ranges by root 
    key”
	1. the edit the ranges appropriately and perhaps fill in the 
      gaps
9. REMOVE STARTING GAP, by selecting all zones, then opening 
    the Wave editor and shortening the initial gap
	1. The apply to all samples by –> Cog wheel >> to all 
      selected zones >> copy current sample - start setting
10. SET ROUND ROBINS
	1. Turn on round robins for all the samples
	2. The give a position to each group in the round robin 
      chain
11. TUNE the samples by starting a tuner plugin on a basic 
    one-note MIDI loop in REAPER, then adjust both volume and 
    pitch for each sample
12. set the ENVELOPE, by going to the ADSR section of the 
    instrument and lengthening the tail of very group to match 
    the the instrument being sampled (or to whatever effect is 
    desired)
13. DONE!


This is the basic structure, then you would have to think in 
terms of GUI, and perhaps controls for some parameters, if 
effects are desired, for instance. And so on. But this is the 
basic procedure.

