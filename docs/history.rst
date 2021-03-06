=======
History
=======

0.0.7 (2018-10-09)
------------------

* First release on PyPI.

0.0.8 (2018-11-26)
------------------

* First major update. Added wfmBuilder.iq_correction(), which utilizes Keysight's VSA software and a Keysight receiver (either an oscilloscope or signal analyzer) and applies a digital predistortion filter to a waveform to flatten amplitude and phase response.

0.0.9 (2018-11-26)
------------------

* Fixed a problem with UXG.csv_pdw_file_download() and UXG.csv_windex_file_download() that threw an error when trying to delete a file that didn't exist.

0.0.10 (2018-12-10)
-------------------

* Added multitone_generator generator. Added 128-QAM and 256-QAM. Streamlined UXG instrument class, split play()/stop into stream_play() and arb_play()/stream_stop() and arb_stop(). Updated index to include a better intro to the project.

0.0.11 (2019-01-23)
-------------------

* Fixed bugs with multitone_generator generator. Added AM modulator.

0.0.12 (2019-02-20)
-------------------

* Removed UXG class and replaced it with two classes, AnalogUXG and VectorUXG. Expanded VSG class to include M9381A and M9383A without changing public API.

0.0.13 (2019-04-19)
-------------------

* Added GUI. Adjusted several functions to streamline waveform creation and download between all instrument types.

0.0.14 (2019-11-12)
-------------------

* Fixed bug in UXG classes that emitted a long CW pulse prior to starting streaming. Added "pri" argument to pulse creation methods.

2020.04.0 (2020-04-29)
----------------------

* Removed communications.py and replaced it with external module ``socketscpi``. ``.configure()`` methods now use ``**kwargs`` to prevent the function from changing any settings not explicitly specified back to default values. Changed multitone_generator waveform creation method to frequency domain. Significant updates to documentation and in-code comments. Changed from semantic versioning to calendar versioning.

2020.05.0 (2020-05-13)
----------------------

* Changed name of digmod_prbs_generator() to digmod_generator(). Overhauled digitally modulated waveform creation function, fixing bugs and producing better signal fidelity. Added vsaControl.py, which allows the user to control an instance of Keysight 89600 VSA software for waveform analysis.

2020.06.0 (2020-06-01)
----------------------

* Added 16-, 32-, and 64-APSK modulation types to wfmBuilder.py. Moved PDW-building function definitions from instruments.py to pdwBuilder.py. Updated documentation.

2020.07.1 (2020-07-06)
----------------------

* BUGFIX: corrected a problem with the 16-QAM modulator in digmod_generator(). Fixed a math error in power level calculations in PDW functions.

2020.07.3 (2020-07-31)
----------------------

* Dramatically improved resampling and wraparound handling in digmod_generator().

2020.08.1 (2020-08-03)
----------------------

* BROKEN: Updated GUI to reflect changes to instrument configuration functions and improvements to wfmBuilder functions. You can now access pyarbtools.pdwBuilder directly. Improved version updating.

2020.08.2 (2020-08-06)
----------------------

* Fixed issue where the GUI icon was not included with the PyArbTools package, which prevented the GUI from running.

2020.09.1 (2020-09-03)
----------------------

* Added VXG instrument class for controlling the M9384B VXG signal generators.

2020.09.2 (2020-09-08)
----------------------

* Added import_mat() method to wfmBuilder.py that imports .mat files containing waveform data and optional metadata.

2021.01.1 (2021-01-20)
----------------------

* Added analog_uxg_lan_stream_pdw_example() analog uxg lan streaming example
