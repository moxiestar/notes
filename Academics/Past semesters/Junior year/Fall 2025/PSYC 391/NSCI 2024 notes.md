# **Lesson 1: ERP basics**

***Measuring ERPs:***
- ERPs - potentiation reaction to a specific event measured by a single electrode
	- Can be used to visualize cognitive processing moment by moment
- Amplitude (size of deflection)
- Latency (when does deflection peak)
- Initial depolarization is recorded by the same electrodes (near occipital lobe) but the deflection is recorded on another electrode (near sagittal plane)

***Computer stuff:***
- /proj/courses/NSCI273
- Longleaf bookmarked [here](https://ondemand.rc.unc.edu/pun/sys/dashboard)
- In **MATLAB**, open ERPLAB Studio by typing **eeglab**, then typing **estudio** in the command


-------------------------------------------------------------------

# **Lesson 2: Advantages of EEGs**

***Learning goals: uses, advantages, and limitations of ERPs; other imaging methods***
- Oddball paradigm - one stimulus is shown, which you don't have to respond to, and then occasionally an "oddball" stimulus is shown, which you do have to respond to
	- Difference in P3 amplitude indicates that different event
- ERPs can be used to measure deception and unconscious processes

***Advantages and limitations of EEGs***
- fMRI and PET are better for linking cognition to brain activity
- EEGs are better for timing of different processes
- Advantages of EEGs over behavioral studies:
	- Observation of covert mental states
	- Timing of cognitive processes
	- Organization of cognitive processes
	- No response is required 
	- Direct measure of brain activity (not blood flow)
	- Not invasive or expensive
- Limits of EEG:
	- Poor spatial resolution (not much more local than lobe)
	- Does not measure deep brain activity
	- Signals can cancel each other out
	- Analyzing the data is complex

***Overview of methods:***
- Neuropsychology: patients with focal brain damage, studying how cognition breaks down
- PET (positron emission topography) scan: tagging blood with radioactive isotope; blood flows to where brain is more active
	- Dangerous because of radiation injections?
	- Delayed because of lag in blood flow
- fMRI (functional magnetic resonance imaging): uses magnetic fields and radiowaves to observe changes in blood oxygenation related to brain activity
	- Delayed because of lag in blood flow
- TMS (transcranial magnetic stimulation): creates small magnetic field that causes neurons to fire, putting that part of the brain out of commission (a temporary "lesion")
- tDCS/tACS (transcranial direct/alternate current stimulation): uses a weak current to inhibit or excite activity within the brain (biasing the brain)
- fNIRS (functional near-infrared spectroscopy): measures blood-flow related changes in reflectance from light
	- Light reflects onto detectors on scalp, showing changes in blood flow beneath detectors (somehow)
- MEG (magnetoencephalography): uses magnetic field to measure potentials
	- High spatial and temporal accuracy

***Electrical potential:***
- Difference in charge between dendrites and cell body in neuron -> PSP 

***Number of electrodes:***
- Active electrode, ground (reference 1) electrode, and reference (reference 2) electrode are all needed
- Having the second reference electrode limits the extraneous noise being recorded
- Caps are orientated in terms of lobes
- Electrodes on the left have odd numbers; on the right, even
- Central electrodes are labelled Cz or Fz etc
- Electro-oculogram electrodes measure the movement of eyes


-------------------------------------------------------------------

# **Lesson 3: Measuring potentials**

***Key takeaways:***
- Electrodes: (active - ground) - (reference - ground) = active - reference
- Location, distance, and orientation of electrodes influence the measured EEG signal
- Averaging trial data helps to reduce noise and see the true patterns of the components (typically requires at least 25 trials)
- Things to consider in components:
	- Amplitude: size of component
	- Latency: timing of component
	- Scalp topography: location of component
- You cannot calculate the change in neural sources from the change in components
- You cannot know the neural sources from the EEG, but you can guess
- Different components have different subtypes based on cognitive associations (ie visual P1 is very different from auditory P1)
- P3 has two subtypes: P3a (reaction to novelty stimulus) and P3b (reaction to target stimulus)
- Larger N1 occurs when discrimination between stimuli is required
- Difference waves - plotting the difference between various neural sources


-------------------------------------------------------------------

# **Lesson 4: ERP components 1**

***N170:***
- Negativity peaking around 170ms in response to human faces
- Topography shows peak over posterior sites, esp. right hemisphere

***N400:***
- Negativity peaking around 400ms in response to semantically unrelated content (nonsensical phrases)

***ERN (Error-related negativity):***
- Negativity peaking around 100ms after an incorrect response
- Calculated by subtracting waveform from incorrect trials minus correct trials
- Distributed across the frontal scalp

***MMN (Mismatch negativity):***
- Negativity evoked by a stimulus between current stimulus and recent stimuli
- Often studied with auditory stimuli
- Can be evoked even when not attending to the stimuli
- Sources in the auditory cortex and frontal lobe

***N2pc:***
- Negativity peaking around 200ms 
- Sources are posterior and contralateral on the scalp
- N1 associated with visual discrimination

***Purpose of ERP studies:***
- Visual discrimination
	- Does mindfulness improve visual discrimination (subjects reacts to stimuli)? Yes, the N1 response increases the more mindfulness training the subject has done
	- Can the N1 be used as a marker of anxiety? Anterior N1 is associated with early attention to emotionally salient visual stimuli - enhanced N1 seen in subjects with anxiety in response to unpleasant critical stimuli
	- Can the N1 predict response to antidepressants? Anterior N1 is sensitive to serotonin - this response is measured to judge whether a subject would respond well to stimuli. The N1 amplitude was correlated positively with how well subjects responded to citalopram

***Notes***
- Each component can have multiple subcomponents
- P300 has P3a and P3b


-------------------------------------------------------------------

# **Lesson 5: ERP components 2**

***Measurement notes:***
- Change in amplitude (intensity) indicates a difference in neural response
	- Increased amplitudes can be positive or negative (as people get more used to a task, they expend less effort - so decreased amplitudes can also be positive)
	- Difference waves can be informative, but raw waveforms are more indicative
		- Compare task conditions and correlations with subject behavior
	- Scalp distributions can also be helpful
- Change in latency (time) 
	- Increased latency indicates a delay in processing (or a confounded process)
	- Careful experimental design can help especially when dealing with components before 200ms

***Notes on N170:***
- N170 has greater amplitude and longer latency for inverted faces compared to upright faces (but scalp distributions are the same - it’s the same neural process, just delayed)
	- Delay of 10ms - significant in neural processing
- N2pc is faster and more intense when reacting to more dramatic stimuli
	- Timing can correlate to attention shift
- Scalp distribution differences typically correlate to different neural sources
- Study examined when the N170 first emerges 
	- N170 is displayed at young ages (4 yrs) but isn't displayed as much during adolescence
	- Researchers then tested scrambled faces - when comparing between scrambled faces and normal faces, the N170 was consistent from age 4 (maybe younger?)
	- Conclusion: subtle changes in visual system occur during first decades of life, but the N170 is present and accurate from a young age
	- Difference occurs in visual processing, not in the actual N170 component
- Best to look at amplitude, latency, and scalp distribution

***Tanaka & Curran article:***
- N170 could be elicited specifically by human faces, or it could be elicited by stimuli that we have expertise in (and everyone has expertise in human faces)
- Stimuli are presented for a short time to avoid subjects' eyes moving around, which gives rise to extra noise in the EEG
- Exclusion criteria: subjects had normal or corrected-to-normal vision
- Recorded from all 128 electrodes on cap, focusing on N170 electrodes (51-98) and averaged electrodes to reduce noise across the cap
- Could be correlated with facial recognition (bird and dog faces) but could be unrelated - researchers also tested with plants, and the pictures of the birds and dogs may not have focused on the faces
- N170 localized to fusiform facial area in brain (ventral temporal lobe)


-------------------------------------------------------------------

# **Lesson 6: Data analysis**

***Amplitude & latency:***
- Check notes for amplitude measures
- Mean and peak are most common measures of amplitude
	- Means are less affected by
		- Noise in data
		- Outliers
		- Number of trials
		- Variation from trial to trial
	- Mean can better capture the strength of the response when the component is more broad
	- Peaks is often better for quantifying sharp peaks
- How to quantify latency?
	- Onset: when component begins
	- Peak latency
	- Offset ?
- Fractional area latency
	- Defining window around peak
	- Integrating to find area under curve
	- Measuring when you get to the halfway point of the area under the curve
- Better to measure latency or amplitude?
	- Both are typically measured
	- Focus depends on experiment
- How to choose the right timing window?
	- Rely on prior research 
	- Rely on specific component
	- Rely on grand average
- How to choose the right electrodes?
	- Rely on literature
	- Rely on scalp distribution
	- Rely on mean amplitudes
	- Also depends on cap (10-10, 10-20)
- Difference waves allow you to focus on a particular component without noise
	- Condition B waveform - Condition A waveform
	- Must look at source waveforms
	- Doesn't allow isolation of effect to a particular condition (?)
- Report unpredicted effects, but don't hypothesize on why they might be there
	- Don't hypothesize after results are known (HARKing)
- Experiments must be reproducible
- Stats for EEG experiments:
	- Predictions about neural responses (amplitudes, latencies, oscillation, behavior)
	- Different results can have the same mean but different variabilities (standard distributions)
	- ANOVA: Analyses of variance
		- These help to explain the variance and the complex relationship between components
		- Identify IV(s) and DV
			- Example: within-subjects: IV factors: Electrode site + stimulus type
			- The more specifics you add to the IV factors, the greater the factorial design becomes
			- Example: Electrode site (PO7, PO8) + stimulus type (faces, cars) = 2x2 factorial design
			- Example: Electrode site (PO7, PO8) + stimulus type (faces, cars, fruit) = 2x3 factorial design
			- Example: Electrode site (PO7, PO8) + stimulus type (faces, cars, fruit) + color (greyscale, full color) = 2x3x2 factorial design
			- Adding a between-subjects factor: Electrode site (PO7, PO8) + stimulus type (faces, cars) + age group (old, young) = 2x2x2 mixed factorial design
- Main effect: the primary effect of a given variable
- Interaction effect: overlapping effect between different variables
- As your factors increase, the possible interactions increase (combinatorics) - these are harder to find and interpret
- F value: how different the means are relative to the variability within each sample
	- If variance is high within the groups, the means of the groups are more likely to be different by accident
- Larger sample size reduces the chance of having outliers
	- Degree of freedom: sample size - 1 ?
- Be sure to compare means to waveforms to check accuracy of data
- Match components to behavior - more meaningful
- **Programming experiments - important for homework**
	- Strategies
		- Find previous studies - contact researchers to see if you can use their program for replication
		- Always test and check
		- Check slides for more strategies with links


-------------------------------------------------------------------

# **Lesson 7: N170 experiment**

***Original N170 experiment:***
- Trial conditions: three sets of stimuli - faces, cars, and textural abstract images - were shown with a fixation cross. Subjects were asked to respond based on which type of stimulus was shown
- Timing: stimuli appeared for less than a second and were followed by a fixation cross
- Tasks: subjects were asked to press A when an object (face or car) was shown and press L when a textural image was shown
- Stimuli: human faces, frontal images of cars, textural abstract images

***Our experiment:***
- N170 response to different expressions
- 40 stimuli: 3 expressions (neutral, scared, happy) x5 plus a scrambled face
- Control: scrambled face (does not elicit N170)
- Different responses for different expressions?
- Hypothesis: the greatest amplitude of the N170 component will be shown in response to scared faces

***Midterm:***
- Paper, including diagrams
- 25-35 multiple choice, 3-6 short answer
- Time: 75 minutes
- Topics:
	- **Lectures (main focus) - review** 
	- Readings: chapters 1, 2, 3, and 9
	- Tanaka and Curran article

***Project:***
- Introduction to component
- Methods
	- Description of original experiment & modification for your own experiment
	- Details of EEG recording specifications and analysis steps
- Results
	- Analysis of full core dataset
		- 2 people: original dataset analysis
		- 1-2 people: alternatives to original dataset analysis
	- Analysis of your own experiment (1 subject)
- Discussion 
	- Original experiment vs new experiment
	- Original dataset vs new dataset
- References
- Create poster and powerpoint

***Data collection:***
- **Averaging and inspecting data:**
	- Grand average: average of all individual subjects' ERP components to create an overall average - displays shared outputs within the EEG data
	- Due to dipole shifts, one subject can show a negative component while others show positive
	- Grand average helps to understand how to quantify data: time windows, amplitudes, latencies, etc
	- Check that grand average correctly represents individual datasets (and is not being overly influenced by a few outliers)
	- Average over given time window
- **Reading data:**
	- Analog to digital converter - allows you to read the EEG signals on a computer
	- Sampling rate should be at least twice the highest frequency you need - this allows you to cover all the necessary data (Nyquist theorem)
		- If you sample too slowly, you get a "fake" frequency appearing in your data
	- Amplifier settings:
		- Gain: may need to be reduced if input is saturating the amps
		- Filters: can be set up when collecting data, especially if collecting AC vs DC
	- Interpolating data - filling in gaps between datapoints on scalp
		- Best for larger, broader components


-------------------------------------------------------------------

# **Lesson 8: ERPLAB guide**

***EEG -> ERP steps:***
- The following steps should be done once MATLAB and ERPLAB have been installed - recommend doing so on your computer if possible (as opposed to accessing it remotely online)
- Step 1: Filter the data
	- DC offset - center the data at 0
	- Localizes all the data within the desired range
	- Low pass filter - only frequencies lower than the threshold can pass through (we lose higher frequencies - removing high frequencies, passing low frequencies)
	- High pass filter - only frequencies higher than the threshold can pass through (we lose lower frequencies - mostly reducing lower background noise or skin potentials)
	- Band pass filter - removes low and high frequencies
	- Notch filters - removes a narrow band of frequencies (used to reduce electrical line noise)
	- Frequency response function - tells you what to amplify and what to diminish
		- Half-amplitude cutoff - reducing EEG by half
		- Sharp cutoff skews the data
- Step 2: Deal with any faulty channels
- Step 3: Re-reference the data
- Step 4: Epoch the data
- Step 5: Baseline correct the data
- Step 6: Artifact rejection
- Step 7: Average the data