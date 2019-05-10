# EE551-Final
BPSK Phase Recovery

This Python program is designed to transmit an image coded along a carrier waveform using BPSK modultation

An image is loaded in and flattened

The image then has its pixel values converted to bits

The flattened bit array is cut into pieces and a header, footer, and data length information are added to the slices

A PRN code is generated although it's not used in this current implementation

As a result of the prn code being generated, the data array is padded with zeros to match the prn code length

The padded array is then modulated on a selected frequency waveform

A phase shift is applied to the modulated waveform

Calculations are done in order to correct the phase of the waveform

The waveform is demodulated and a search is done for the header, footer, and data length values

A validation check is done in order to identify valid header, footer and datalength sets

If there are no valid sets identified, the phase correction is assumed to be off by pi

The data sequence is inverted if the phase correction is off and validation is done again

After validation works correctly the valid sets are used to get the image data back

The image bits are converted back to int8 values and then reshaped to the original image size

A little more work is done in order for the image to display correctly

The original image and reconstructed image are displayed side by side to compare
