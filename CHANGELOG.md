# Changelog

* [Unreleased](#unreleased)
* [0.8.0](#080---2018-04-27)
* [0.7.0](#070---2018-02-20)
* [0.6.0](#060---2017-12-20)
* [0.5.0](#050---2017-11-27)
* [0.4.0](#040---2017-11-07)
* [0.3.0](#030---2017-10-13)
* [0.2.0](#020---2017-09-20)
* [0.1.0](#010---2017-09-01)

All notable changes to this project will be documented in this file.

## [Unreleased]
* ### ALL
    * #### Added
    * #### Changed
        * `SelfTestError` now inherits from `<driver>.Error` rather than `Exception` - [#830](https://github.com/ni/nimi-python/issues/830)
        * Warning class name changed to `<driver>.DriverWarning` for all drivers - [#658](https://github.com/ni/nimi-python/issues/658)
    * #### Removed
        * IVI properties as applicable - some where already removed from some drivers [#824](https://github.com/ni/nimi-python/issues/824)
            * `engine_major_version`
            * `engine_minor_version`
            * `engine_revision`
            * `primary_error`
            * `secondary_error`
            * `error_elaboration`
            * `io_session_type`
            * `io_session` / `visa_rm_session`
            * `group_capabilities`
            * `interchange_check`
            * `range_check`
            * `record_coercions`
            * `specific_driver_class_spec_major_version`
            * `specific_driver_class_spec_minor_version`
            * `query_instrument_status`
            * `cache`
            * `specific_driver_prefix`
* ### NI-DMM
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-ModInst
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-Switch
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-DCPower
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-FGEN
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-SCOPE
    * #### Added
    * #### Changed
    * #### Removed
        * Properties removed
            * `stream_relative_to` [#825](https://github.com/ni/nimi-python/issues/825)
            * `oscillator_phase_dac_value` [#825](https://github.com/ni/nimi-python/issues/825)
            * `mux_mode_register` [#825](https://github.com/ni/nimi-python/issues/825)
            * `ddc_center_frequency` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_data_processing_mode` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_enabled` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_frequency_translation_enabled` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_frequency_translation_phase_i` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_frequency_translation_phase_q` [#823](https://github.com/ni/nimi-python/issues/823)
            * `ddc_q_source` [#823](https://github.com/ni/nimi-python/issues/823)
            * `digital_gain` [#823](https://github.com/ni/nimi-python/issues/823)
            * `digital_offset` [#823](https://github.com/ni/nimi-python/issues/823)
            * `dither_enabled` [#823](https://github.com/ni/nimi-python/issues/823)
            * `fetch_interleaved_iq_data` [#823](https://github.com/ni/nimi-python/issues/823)
            * `fractional_resample_enabled` [#823](https://github.com/ni/nimi-python/issues/823)
            * `overflow_error_reporting` [#823](https://github.com/ni/nimi-python/issues/823)
            * `adjust_pretrigger_samples_5102` [#822](https://github.com/ni/nimi-python/issues/822)
            * `five_v_out_output_terminal` [#822](https://github.com/ni/nimi-python/issues/822)
            * `clock_sync_pulse_source` [#822](https://github.com/ni/nimi-python/issues/822)
            * `device_number` [#822](https://github.com/ni/nimi-python/issues/822)
            * `fetch_interleaved_data` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_from_pfi_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_from_rtsi_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_from_star_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_to_pfi_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_to_rtsi_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `trigger_to_star_delay` [#822](https://github.com/ni/nimi-python/issues/822)
            * `slave_trigger_delay` [#822](https://github.com/ni/nimi-python/issues/822)
        * Methods removed
            * `get_frequency_response()` [#823](https://github.com/ni/nimi-python/issues/823)

## 0.8.0 - 2018-04-27
* ### ALL
    * #### Changed
        * All exceptions raised by the Python bindings inherit from `<driver>.Error`
        * Exception type formerly known as `<driver>.Error` is now known as `<driver>.DriverError`
            * This encapsulates any error that is returned by the underlying driver
        * All timeout parameters can now also take a simple number in seconds. `timeout=datetime.timedelta(milliseconds=100)` and `timeout=0.1` are identical. [#796](https://github.com/ni/nimi-python/issues/796)
* ### NI-DMM
    * #### Changed
        * Enum values that start with an underscore + digit have been renamed
            * `Function._2_WIRE_RES` --> `Function.TWO_WIRE_RES`
            * `Function._4_WIRE_RES` --> `Function.FOUR_WIRE_RES`
            * `ThermistorType._44004` --> `ThermistorType.THERMISTOR_44004`
            * `ThermistorType._44006` --> `ThermistorType.THERMISTOR_44006`
            * `ThermistorType._44007` --> `ThermistorType.THERMISTOR_44007`
            * `TransducerType._2_WIRE_RTD` --> `TransducerType.TWO_WIRE_RTD`
            * `TransducerType._4_WIRE_RTD` --> `TransducerType.FOUR_WIRE_RTD`
        * `Session.get_ext_cal_recommended_interval()` now returns a `datetime.timedelta` for the interval [#794](https://github.com/ni/nimi-python/issues/794)
* ### NI-DCPower
    * #### Changed
        * `Session.fetch_multiple()` and `Session.measure_multiple()` now return list of named tuples instead of multiple arrays. See [fetch_multiple](http://nimi-python.readthedocs.io/en/master/nidcpower/functions.html#nidcpower.Session.fetch_multiple) and [measure_multiple](http://nimi-python.readthedocs.io/en/master/nidcpower/functions.html#nidcpower.Session.measure_multiple)
        * `Session.cal_self_calibration()` renamed to `Session.self_cal()` to match other drivers - issue [#615](https://github.com/ni/nimi-python/issues/615)
        * `Session.set_sequence()` values parameter no longer has a default value and must be passed in. Parameter order has changed as a result of this - issue [#797](https://github.com/ni/nimi-python/issues/797)
        * Session constructor channel parameter can now use any channel format that repeated capabilities can use [#807](https://github.com/ni/nimi-python/issues/807)
        * `Session.get_ext_cal_recommended_interval()` now returns a `datetime.timedelta` for the interval [#794](https://github.com/ni/nimi-python/issues/794)
    * #### Removed
        * Advanced Sequence functions - until [#504](https://github.com/ni/nimi-python/issues/504) can be fixed in a proper way
            * `create_advanced_sequence()`
            * `create_advanced_sequence_step()`
            * `delete_advanced_sequence()`
* ### NI-FGEN
    * #### Changed
        * `Session.export_signal()` signal_identifier now has a default of "". This moves it to the end of the parameter list [#801](https://github.com/ni/nimi-python/issues/801)
        * `Session.get_ext_cal_recommended_interval()` now returns a `datetime.timedelta` for the interval [#794](https://github.com/ni/nimi-python/issues/794)
    * #### Removed
        * `Session.cal_adc_input` attribute and `Session.enums.CalADCInput` enum - External Cal not supported in Python
        * Session constructor channel parameter can now use any channel format that repeated capabilities can use [#807](https://github.com/ni/nimi-python/issues/807)
* ### NI-SCOPE
    * #### Changed
        * `Session.fetch()`, `Session.read()` and `Session.fetch_into()` updated
            * Takes additional parameters that modify fetch behavior
            * Add resulting record as part of the waveform info
            * Channel name and record number added to waveform info
            * See documentation for [fetch](http://nimi-python.readthedocs.io/en/master/niscope/functions.html#niscope.Session.fetch), 
                [read](http://nimi-python.readthedocs.io/en/master/niscope/functions.html#niscope.Session.read), 
                and [fetch_into](http://nimi-python.readthedocs.io/en/master/niscope/functions.html#niscope.Session.fetch_into) for more details.
        * Rename `wfm` parameter to `waveform` in `fetch()` and `fetch_into()`
        * Enum values and attribute names that start with an underscore + digit have been renamed
            * `Session._5102_adjust_pretrigger_samples` --> `Session.adjust_pretrigger_samples_5102`
            * `Session._5v_out_output_terminal` --> `Session.five_v_out_output_terminal`
            * `ExportableSignals._5V_OUT` --> `ExportableSignals.FIVE_V_OUT`
            * `FlexFIRAntialiasFilterType._48_TAP_STANDARD` --> `FlexFIRAntialiasFilterType.FOURTYEIGHT_TAP_STANDARD`
            * `FlexFIRAntialiasFilterType._48_TAP_HANNING` --> `FlexFIRAntialiasFilterType.FOURTYEIGHT_TAP_HANNING`
            * `FlexFIRAntialiasFilterType._16_TAP_HANNING` --> `FlexFIRAntialiasFilterType.SIXTEEN_TAP_HANNING`
            * `FlexFIRAntialiasFilterType._8_TAP_HANNING` --> `FlexFIRAntialiasFilterType.EIGHT_TAP_HANNING`
            * `VideoSignalFormat._480I_59_94_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_480I_59_94_FIELDS_PER_SECOND`
            * `VideoSignalFormat._480I_60_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_480I_60_FIELDS_PER_SECOND`
            * `VideoSignalFormat._480P_59_94_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_480P_59_94_FRAMES_PER_SECOND`
            * `VideoSignalFormat._480P_60_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_480P_60_FRAMES_PER_SECOND`
            * `VideoSignalFormat._576I_50_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_576I_50_FIELDS_PER_SECOND`
            * `VideoSignalFormat._576P_50_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_576P_50_FRAMES_PER_SECOND`
            * `VideoSignalFormat._720P_50_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_720P_50_FRAMES_PER_SECOND`
            * `VideoSignalFormat._720P_59_94_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_720P_59_94_FRAMES_PER_SECOND`
            * `VideoSignalFormat._720P_60_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_720P_60_FRAMES_PER_SECOND`
            * `VideoSignalFormat._1080I_50_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_1080I_50_FIELDS_PER_SECOND`
            * `VideoSignalFormat._1080I_59_94_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_1080I_59_94_FIELDS_PER_SECOND`
            * `VideoSignalFormat._1080I_60_FIELDS_PER_SECOND` --> `VideoSignalFormat.VIDEO_1080I_60_FIELDS_PER_SECOND`
            * `VideoSignalFormat._1080P_24_FRAMES_PER_SECOND` --> `VideoSignalFormat.VIDEO_1080P_24_FRAMES_PER_SECOND`
        * `Session.cal_self_calibration()` renamed to `Session.self_cal()` to match other drivers - issue [#615](https://github.com/ni/nimi-python/issues/615)
    * #### Removed
        * Following properties are now removed (use parameters to fetch calls):
            * `fetch_relative_to`
            * `fetch_offset`
            * `fetch_record_number`
            * `fetch_num_records`
        * Removed `number_of_coefficients` parameter from `get_equalization_filter_coefficients()`
        * Removed Measurement Library waveform methods and properties - issue [#809](https://github.com/ni/nimi-python/issues/809)
            * `actual_meas_wfm_size()`
            * `add_waveform_processing()`
            * `clear_waveform_processing()`
            * `fetch_array_measurement()`
            * `clear_waveform_measurement_stats()`
            * `fetch_measurement()`
            * `fetch_measurement_stats()`
            * `read_measurement()`
            * `configure_ref_levels()`
            * `meas_ref_level_units`
            * `meas_other_channel`
            * `meas_hysteresis_percent`
            * `meas_last_acq_histogram_size`
            * `meas_voltage_histogram_size`
            * `meas_voltage_histogram_low_volts`
            * `meas_voltage_histogram_high_volts`
            * `meas_time_histogram_size`
            * `meas_time_histogram_low_volts`
            * `meas_time_histogram_high_volts`
            * `meas_time_histogram_low_time`
            * `meas_time_histogram_high_time`
            * `meas_polynomial_interpolation_order`
            * `meas_interpolation_sampling_factor`
            * `meas_filter_cutoff_freq`
            * `meas_filter_center_freq`
            * `meas_filter_ripple`
            * `meas_filter_transient_waveform_percent`
            * `meas_filter_type`
            * `meas_filter_order`
            * `meas_filter_taps`
            * `meas_chan_low_ref_level`
            * `meas_chan_mid_ref_level`
            * `meas_chan_high_ref_level`
            * `meas_filter_width`
            * `meas_fir_filter_window`
            * `meas_array_gain`
            * `meas_array_offset`
            * `meas_percentage_method`
            * `fetch_meas_num_samples`

## 0.7.0 - 2018-02-20
* ### ALL
    * #### Changed
        * Option string can now be a python dictionary instead of a string. (Fix [#661](https://github.com/ni/nimi-python/issues/661))
            * Key/Value pairs approporiate for desired behavior
                ``` python
                session = nidmm.Session('Dev1', False, {'simulate': True, 'driver_setup': {'Model': '4071', 'BoardType': 'PXI'}})
                ```
        * Repeated capabilities are handled differently. See [#737](https://github.com/ni/nimi-python/issues/737) for discussion
        * All function parameters or attributes that represent time now use `datetime.timedelta()`. See [#659](https://github.com/ni/nimi-python/issues/659) for discussion
        * All functions that return calibration dates now return `datetime.datetime()`. See [#659](https://github.com/ni/nimi-python/issues/659) for discussion
* ### NI-DMM
    * #### Changed
        * `nidmm.Session()` no longer takes id_query parameter (Fix [#670](https://github.com/ni/nimi-python/issues/670))
        * The following functions timeout or delay parameter now is required to be a `datetime.timedelta()` object:
            * `configure_multi_point()`
            * `configure_trigger()`
            * `fetch()`
            * `fetch_multi_point()`
            * `fetch_waveform()`
            * `read()`
            * `read_multi_point()`
            * `read_waveform()`
        * The following functions return a `datetime.datetime()` object representing the date and time
            * `get_cal_date_and_time()`
        * Metadata updated to NI-DMM 17.5
    * #### Removed
        * Removed these enums and disconnected them from the associated attribute (Fix [#666](https://github.com/ni/nimi-python/issues/666))
            * `DCBias` - `DC_BIAS`
            * `OffsetCompensatedOhms` - `OFFSET_COMP_OHMS`
* ### NI-Switch
    * #### Changed
        * The following functions timeout, delay or holdoff parameters now is required to be a `datetime.timedelta()` object:
            * `configure_scan_trigger()`
            * `wait_for_debounce()`
            * `wait_for_scan_complete()`
* ### NI-DCPower
    * #### Added
        * `channel` repeated capability - See [#737](https://github.com/ni/nimi-python/issues/737) for discussion
    * #### Changed
        * Metadata updated to NI-DCPower 17.6.1
        * The following functions timeout parameter now is required to be a `datetime.timedelta()` object:
            * `fetch_multiple()`
            * `wait_for_event()`
        * The following functions return a `datetime.datetime()` object representing the date and time
            * `get_ext_cal_last_date_and_time()`
            * `get_self_cal_last_date_and_time()`
    * #### Removed
        * Removed these enums and disconnected them from the associated attribute (Fix [#666](https://github.com/ni/nimi-python/issues/666))
            * `CurrentLimitAutorange` - `CURRENT_LIMIT_AUTORANGE`
            * `CurrentLevelAutorange` - `CURRENT_LEVEL_AUTORANGE`
            * `VoltageLevelAutorange` - `VOLTAGE_LEVEL_AUTORANGE`
            * `VoltageLimitAutorange` - `VOLTAGE_LIMIT_AUTORANGE`
* ### NI-FGEN
    * #### Changed
        * Repeated capablilites - See [#737](https://github.com/ni/nimi-python/issues/737) for discussion:
            * `channel` repeated capability
            * `markers` repeated capability
            * `script_triggers` repeated capability
        * The following functions timeout parameter now is required to be a `datetime.timedelta()` object:
            * `adjust_sample_clock_relative_delay()`
            * `wait_until_done()`
        * The following functions return a `datetime.datetime()` object representing the date and time
            * `get_ext_cal_last_date_and_time()`
            * `get_self_cal_last_date_and_time()`
* ### NI-SCOPE
    * #### Added
        * Repeated capablilites - See [#737](https://github.com/ni/nimi-python/issues/737) for discussion:
            * `channel` repeated capability
    * #### Changed
        * `niscope.Session()` no longer takes id_query parameter (Fix [#670](https://github.com/ni/nimi-python/issues/670))
        * The following functions timeout, delay or holdoff parameters now is required to be a `datetime.timedelta()` object:
            * `configure_trigger_digital()`
            * `configure_trigger_edge()`
            * `configure_trigger_hysteresis()`
            * `configure_trigger_software()`
            * `configure_trigger_video()`
            * `configure_trigger_window()`
            * `fetch()`
            * `fetch_measurement_stats()`
            * `read()`
    * #### Removed
        * Removed these enums and disconnected them from the associated attribute (Fix [#666](https://github.com/ni/nimi-python/issues/666))
            * `BoolEnableDisable` - `P2P_ENABLED`, `P2P_ADVANCED_ATTRIBUTES_ENABLED`, `P2P_ONBOARD_MEMORY_ENABLED`
            * `BoolEnableDisableChan` - `CHANNEL_ENABLED`
            * `BoolEnableDisableIQ` - `FETCH_INTERLEAVED_IQ_DATA`
            * `BoolEnableDisableRealtime` - `HORZ_ENFORCE_REALTIME`
            * `BoolEnableDisableTIS` - `ENABLE_TIME_INTERLEAVED_SAMPLING`

## 0.6.0 - 2017-12-20
* ### ALL
  * #### Added
    * `abort`. See [#660](https://github.com/ni/nimi-python/issues/655).
* ### NI-DMM
  * #### Added
    * `fetch_waveform_into` for high-performance fetch using numpy.array of float64.
  * #### Changed
    * Property powerline_freq no longer uses enum PowerlineFrequency.
    * Property current_source no longer uses enum CurrentSource.
    * Property input_resistance no longer uses enum InputResistance.
    * Removed `actual_number_of_points` from `fetch_waveform()` returned tuple
    * Removed `actual_number_of_points` from `fetch_multi_point()` returned tuple
    * Removed `actual_number_of_points` from `read_multi_point()` returned tuple
    * Removed `actual_number_of_points` from `read_waveform()` returned tuple
* ### NI-Switch
  * #### Removed
    * Removed `init_with_topology`. Clients should use `niswitch.Session` constructor. See [#660](https://github.com/ni/nimi-python/issues/660).
* ### NI-DCPower
  * #### Changed
    * Property power_line_frequency no longer uses enum PowerLineFrequency.
    * Removed `actual_count` from `fetch_multiple()` returned tuple
* ### NI-FGEN
  * #### Added
    * Support for calling `write_waveform` using list (float) or numpy.array (int16 or float64)
    * Support for calling `write_waveform` with a waveform handle (int) or a name (str).
    * Support for calling `create_waveform` using list (float) or numpy.array (int16 or float64)
  * #### Changed
    * Renamed `create_waveform_f64` -> `create_waveform`
  * #### Removed
    * `create_waveform_i16`
    * `write_binary16_waveform`: Use `write_waveform`
    * `write_named_waveform_i16`: Use `write_waveform`
    * `write_named_waveform_f64`: Use `write_waveform`
* ### NI-SCOPE
  * #### Added
    * `fetch_into` for high-performance fetch using numpy.array. Supported element types:
      * `numpy.float64`
      * `numpy.int8`
      * `numpy.int16`
      * `numpy.int32`
  * #### Changed
    * Added default values for timeout on all fetch and read functions.
    * Property input_impedance no longer uses enum InputImpedance.
  * #### Removed
    * `AddWaveformProcessing` - See #667 for rationale
    * `ClearWaveformProcessing` - See #667 for rationale
    * `FetchArrayMeasurement` - See #667 for rationale

## 0.5.0 - 2017-11-27
* ### ALL
  * #### Removed
    * enum definitions that are not referenced by a function and/or an attributes
* ### NI-DMM
  * #### Added
    * `get_ext_cal_recommended_interval`
* ### NI-DCPower
  * #### Added
    * `get_ext_cal_last_date_and_time`
    * `get_ext_cal_last_temp`
    * `get_ext_cal_recommended_interval`
    * `measure_multiple`
* ### NI-FGEN
  * #### Removed
    * `adjust_sample_clock_relative_delay`
* ### NI-SCOPE
  * #### Added
    * Initial release
  * #### Removed
    * Removed Peer to Peer attributes

## 0.4.0 - 2017-11-07
* ### ALL
  * #### Changed
    * Simplified examples by removing try/except
    * **SOURCE BREAKER:** Changed names of enum value names to correspond to C #defines
* ### NI-DMM
  * #### Changed
    * Removed incorrect leading underscore from some enum values:
      * `Function.AC_VOLTS_DC_COUPLED`
      * `Function.WAVEFORM_CURRENT`
      * `MeasurementCompleteDest.LBR_TRIG_0`
      * `OperationMode.IVIDMM_MODE`
      * `SampleTrigger.EXTERNAL`
      * `SampleTrigger.TTL_3`
      * `TriggerSource.TTL_0`
      * `TriggerSource.TTL_3`
      * `TriggerSource.TTL_7`
      * `TriggerSource.PXI_STAR`
* ### NI-SWITCH
  * #### Removed
    * Support for `is_debounced` and `is_scanning` functions. Instead use the attribute of the same name.
* ### NI-DCPower
  * #### Added
    * New example `nidcpower_advanced_sequence.py`
  * #### Changed
    * Fixed method signature for:
      * `wait_for_event`
      * `create_sequence`
      * `create_advanced_sequence`
  * #### Removed
    * Support for `measure_multiple` until issue #444 is addressed.
* ### NI-FGEN
  * #### Added
    * Initial release

## 0.3.0 - 2017-10-13
* ### ALL
  * #### Added
    * Support for ViInt64 (64-bit integers)
  * #### Changed
    * Modified how methods with repeated capabilities are invoked. There's no longer (for example) a `channel_name` input. Instead:
      ```python
      # Sets sequence on channels 0 through 3
      session['0-3'].set_sequence(values, source_delays)
      ```
    * Enum value documentation lists the fully qualified name - this is to allow easy copy/paste
* ### NI-DMM
  * #### Changed
    * Added default values to some parameters.
  * #### Removed
    * Removed methods that aren’t useful in the Python bindings.
* ### NI-SWITCH
  * #### Changed
    * Added default values to some parameters.
  * #### Removed
    * Removed methods that aren’t useful in the Python bindings.
* ### NI-DCPower
  * #### Added
    * Initial release

## 0.2.0 - 2017-09-20
* ### ALL
  * #### Added
    * Suport for channel-based properties
  * #### Changed
    * Warnings no longer raise an exception
      * Warnings are now added to warnings.warn()
* ### NI-DMM
  * #### Changed
    * Added support for enums with types other than ViInt32 (Fixes [#330](https://github.com/ni/nimi-python/issues/330))
* ### NI-ModInst
  * #### Changed
    * Device index is now on session not attribute. The correct way is now
      ```python
      i = 0
      with nimodinst.Session('nidmm') as session:
          name = session[i].device_name
      ```
* ### NI-SWITCH
  * #### Added
    * Initial release

## 0.1.0 - 2017-09-01
* ### NI-DMM
  * #### Added
    * Initial release
* ### NI-ModInst
  * #### Added
    * Initial release

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Python Versioning](http://legacy.python.org/dev/peps/pep-0396/).

<!--
## [Unreleased]
* ### ALL
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-DMM
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-ModInst
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-Switch
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-DCPower
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-FGEN
    * #### Added
    * #### Changed
    * #### Removed
* ### NI-SCOPE
    * #### Added
    * #### Changed
    * #### Removed
-->


