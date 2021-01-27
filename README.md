# Sensirion I2C SCD4x Arduino Library

This is the Sensirion SCD4x library for Arduino using the I2C interface.

[<center><img src="assets/SCD41_Development_Board.png" width="300px"></center>](https://sensirion.com/my-scd-ek)

Click [here](https://sensirion.com/my-scd-ek) to learn more about the SCD4x
sensor and the SCD41 Evaluation Kit Board.

# Installation

To install, download the latest release as .zip file and add it to your
[Arduino IDE](http://www.arduino.cc/en/main/software) via

	Sketch => Include Library => Add .ZIP Library...

Don't forget to **install the dependencies** listed below the same way via `Add
.ZIP Library`

Note: Installation via the Arduino Library Manager is coming soon.

# Dependencies

* [Sensirion Core Arduino Library](https://github.com/Sensirion/Sensirion_Core_Arduino_Library)


# Quick Start

1. Connect the SCDd4x sensor to your Arduino board's standard I2C bus. Check
   the pinout of your Arduino board to find the correct pins. The pinout of the
   SCD4x sensor board can be found [here](https://sensirion.com/my-scd-ek)

	* **VDD** of the SEK-SCD41 to the **3.3V** of your Arduino board (5V is also possible)
	* **GND** of the SEK-SCD41 to the **GND** of your Arduino board
	* **SCL** of the SEK-SCD41 to the **SCL** of your Arduino board
	* **SDA** of the SEK-SCD41 to the **SDA** of your Arduino board

2. Open the `exampleUsage` sample project within the Arduino IDE

		File => Examples => Sensirion I2C Scd4x => exampleUsage

3. Click the `Upload` button in the Arduino IDE or

		Sketch => Upload

4. When the upload process has finished, open the `Serial Monitor` or `Serial
   Plotter` via the `Tools` menu to observe the measured CO2, Temperature and
   Humidity values. Note that the `Baud Rate` in the corresponding window has
   to be set to `115200 baud`.

# Contributing

**Contributions are welcome!**

We develop and test this driver using our company internal tools (version
control, continuous integration, code review etc.) and automatically
synchronize the master branch with GitHub. But this doesn't mean that we don't
respond to issues or don't accept pull requests on GitHub. In fact, you're very
welcome to open issues or create pull requests :)

This Sensirion library uses
[`clang-format`](https://releases.llvm.org/download.html) to standardize the
formatting of all our `.cpp` and `.h` files. Make sure your contributions are
formatted accordingly:

The `-i` flag will apply the format changes to the files listed.

```bash
clang-format -i *.cpp *.h
```

Note that differences from this formatting will result in a failed build until
they are fixed.

# License

See [LICENSE](LICENSE).
