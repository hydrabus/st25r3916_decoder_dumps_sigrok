# st25r3916_decoder_dumps_sigrok
HydraNFC Shield v2 st25r3916 decoder/dumps for sigrok nightly build

st25r3916_spi decoder limitations/TODO:
* This decoder shall be compatible with all ST25R39xx ICs(except ST25R3911B which have different registers ...) and is validated with ST25R3916
* Does not provide details for register value with Bit Fields (contribution is welcome to add Bit Fields for each register...)
* Chaining Direct Commands is not supported and will display some errors 
  * Note: https://www.st.com/en/embedded-software/stsw-st25rfal002.html ST25R3916 RFAL does not use Chaining Direct Commands so far (checked on STSW-ST25RFAL002 v2.4.0 or before)
* Write or Read registers with auto-incrementing address is not supported and will display errors
    * Note: https://www.st.com/en/embedded-software/stsw-st25rfal002.html ST25R3916 RFAL does not use auto-incrementing address so far (checked on STSW-ST25RFAL002 v2.4.0 or before)

Update 30 July 2020: 
* st25r39xx Decoder available in official sigrokproject repository see https://github.com/sigrokproject/libsigrokdecode/tree/master/decoders/st25r39xx_spi
* st25r39xx Dumps available in official sigrokproject repository see https://github.com/sigrokproject/sigrok-dumps/tree/master/nfc/st25r39xx

Update 10 August 2021: 
* Fix decoders/st25r39xx_spi FIFOR/FIFOW issues with Pulseview (with "Tabular Output View" crash when refresh...) because of FIFO Read/FIFO Write commands, was not returning the annotations short name FIFOR/FIFOW
