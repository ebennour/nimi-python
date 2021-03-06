niscope.Session
===============

.. py:module:: niscope

.. py:class:: Session

   An NI-SCOPE session to a National Instruments Digitizer.

   **Properties**

   +-----------------------------------------------------+----------------------------------------+
   | Property                                            | Datatype                               |
   +=====================================================+========================================+
   | :py:attr:`absolute_sample_clock_offset`             | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`accessory_gain`                           | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`accessory_offset`                         | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`acquisition_start_time`                   | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`acquisition_type`                         | :py:data:`AcquisitionType`             |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`acq_arm_source`                           | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`adv_trig_src`                             | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`allow_more_records_than_memory`           | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`arm_ref_trig_src`                         | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`backlog`                                  | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`bandpass_filter_enabled`                  | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`binary_sample_width`                      | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`channel_count`                            | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`channel_enabled`                          | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`channel_terminal_configuration`           | :py:data:`TerminalConfiguration`       |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`data_transfer_block_size`                 | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`data_transfer_maximum_bandwidth`          | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`data_transfer_preferred_packet_size`      | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`device_temperature`                       | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`driver_setup`                             | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`enable_dc_restore`                        | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`enable_time_interleaved_sampling`         | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`end_of_acquisition_event_output_terminal` | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`end_of_record_event_output_terminal`      | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`end_of_record_to_advance_trigger_holdoff` | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`equalization_filter_enabled`              | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`equalization_num_coefficients`            | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`exported_advance_trigger_output_terminal` | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`exported_ref_trigger_output_terminal`     | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`exported_start_trigger_output_terminal`   | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`flex_fir_antialias_filter_type`           | :py:data:`FlexFIRAntialiasFilterType`  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`fpga_bitfile_path`                        | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`high_pass_filter_frequency`               | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_enforce_realtime`                    | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_min_num_pts`                         | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_num_records`                         | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_record_length`                       | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_record_ref_position`                 | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_sample_rate`                         | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`horz_time_per_record`                     | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`input_clock_source`                       | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`input_impedance`                          | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`instrument_firmware_revision`             | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`instrument_manufacturer`                  | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`instrument_model`                         | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`interleaving_offset_correction_enabled`   | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`io_resource_descriptor`                   | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`logical_name`                             | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`master_enable`                            | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`max_input_frequency`                      | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`max_real_time_sampling_rate`              | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`max_ris_rate`                             | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`min_sample_rate`                          | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`onboard_memory_size`                      | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`output_clock_source`                      | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`pll_lock_status`                          | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`points_done`                              | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`poll_interval`                            | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`probe_attenuation`                        | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ready_for_advance_event_output_terminal`  | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ready_for_ref_event_output_terminal`      | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ready_for_start_event_output_terminal`    | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`records_done`                             | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`record_arm_source`                        | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ref_clk_rate`                             | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ref_trigger_detector_location`            | :py:data:`RefTriggerDetectorLocation`  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ref_trigger_minimum_quiet_time`           | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ref_trig_tdc_enable`                      | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`resolution`                               | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ris_in_auto_setup_enable`                 | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ris_method`                               | :py:data:`RISMethod`                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`ris_num_averages`                         | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`sample_clock_timebase_multiplier`         | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`sample_mode`                              | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`samp_clk_timebase_div`                    | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`samp_clk_timebase_rate`                   | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`samp_clk_timebase_src`                    | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`serial_number`                            | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`simulate`                                 | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`specific_driver_description`              | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`specific_driver_revision`                 | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`specific_driver_vendor`                   | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`start_to_ref_trigger_holdoff`             | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`supported_instrument_models`              | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_auto_triggered`                   | bool                                   |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_coupling`                         | :py:data:`TriggerCoupling`             |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_delay_time`                       | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_holdoff`                          | float in seconds or datetime.timedelta |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_hysteresis`                       | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_impedance`                        | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_level`                            | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_modifier`                         | :py:data:`TriggerModifier`             |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_slope`                            | :py:data:`TriggerSlope`                |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_source`                           | str                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_type`                             | :py:data:`TriggerType`                 |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_window_high_level`                | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_window_low_level`                 | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`trigger_window_mode`                      | :py:data:`TriggerWindowMode`           |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`tv_trigger_event`                         | :py:data:`VideoTriggerEvent`           |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`tv_trigger_line_number`                   | int                                    |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`tv_trigger_polarity`                      | :py:data:`VideoPolarity`               |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`tv_trigger_signal_format`                 | :py:data:`VideoSignalFormat`           |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`vertical_coupling`                        | :py:data:`VerticalCoupling`            |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`vertical_offset`                          | float                                  |
   +-----------------------------------------------------+----------------------------------------+
   | :py:attr:`vertical_range`                           | float                                  |
   +-----------------------------------------------------+----------------------------------------+

   **Public methods**

   +-------------------------------------------------------+
   | Method name                                           |
   +=======================================================+
   | :py:func:`abort`                                      |
   +-------------------------------------------------------+
   | :py:func:`acquisition_status`                         |
   +-------------------------------------------------------+
   | :py:func:`auto_setup`                                 |
   +-------------------------------------------------------+
   | :py:func:`commit`                                     |
   +-------------------------------------------------------+
   | :py:func:`configure_chan_characteristics`             |
   +-------------------------------------------------------+
   | :py:func:`configure_equalization_filter_coefficients` |
   +-------------------------------------------------------+
   | :py:func:`configure_horizontal_timing`                |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_digital`                  |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_edge`                     |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_hysteresis`               |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_immediate`                |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_software`                 |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_video`                    |
   +-------------------------------------------------------+
   | :py:func:`configure_trigger_window`                   |
   +-------------------------------------------------------+
   | :py:func:`configure_vertical`                         |
   +-------------------------------------------------------+
   | :py:func:`disable`                                    |
   +-------------------------------------------------------+
   | :py:func:`export_signal`                              |
   +-------------------------------------------------------+
   | :py:func:`fetch`                                      |
   +-------------------------------------------------------+
   | :py:func:`fetch_into`                                 |
   +-------------------------------------------------------+
   | :py:func:`get_equalization_filter_coefficients`       |
   +-------------------------------------------------------+
   | :py:func:`probe_compensation_signal_start`            |
   +-------------------------------------------------------+
   | :py:func:`probe_compensation_signal_stop`             |
   +-------------------------------------------------------+
   | :py:func:`read`                                       |
   +-------------------------------------------------------+
   | :py:func:`reset`                                      |
   +-------------------------------------------------------+
   | :py:func:`reset_device`                               |
   +-------------------------------------------------------+
   | :py:func:`reset_with_defaults`                        |
   +-------------------------------------------------------+
   | :py:func:`self_cal`                                   |
   +-------------------------------------------------------+
   | :py:func:`self_test`                                  |
   +-------------------------------------------------------+
   | :py:func:`send_software_trigger_edge`                 |
   +-------------------------------------------------------+


