# st25r3916_decoder_dumps_sigrok
HydraNFC Shield v2 st25r3916 decoder/dumps for sigrok nightly build

* Waiting st25r3916 spi decoder pull request to be integrated in official libsigrokdecode https://github.com/sigrokproject/libsigrokdecode/pull/37
* Waiting st25r3916 spi dumps pull request to be integrated in official sigrok-dumps https://github.com/sigrokproject/sigrok-dumps/pull/21

Note: You can add comments in those pull requests to speed up the process...

st25r3916_spi decoder limitations/TODO:
* This decoder shall be compatible with all ST25R39xx ICs(except ST25R3911B which have different registers ...) and is validated with ST25R3916
* Does not provide details for register value with Bit Fields (contribution is welcome to add Bit Fields for each register...)
* Chaining Direct Commands is not supported and will display some errors 
  * Note: https://www.st.com/en/embedded-software/stsw-st25rfal002.html ST25R3916 RFAL does not use Chaining Direct Commands so far (checked on STSW-ST25RFAL002 v2.2.0 or before)
* Write or Read registers with auto-incrementing address is not supported and will display errors
    * Note: https://www.st.com/en/embedded-software/stsw-st25rfal002.html ST25R3916 RFAL does not use auto-incrementing address so far (checked on STSW-ST25RFAL002 v2.2.0 or before)
