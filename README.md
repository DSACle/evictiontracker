# DSA Cleveland Evictions Tracker
The DSA Cleveland evictions tracker is a java command line tool designed to parse evictions data.

## Windows Instructions
### Getting Started
**First-time users only**, be sure to download and install the latest version of Java from https://java.com/en/download. If Java 8 is already installed on your computer you can skip this step, but there is no harm in re-installing over an existing version if you are unsure.

**Returning users**, check for any new [releases](https://github.com/DSACle/evictiontracker/releases) since your last visit:
- If needed, download the latest version by clicking "Assets" and then `evictionsparser.zip`. If prompted, save the file to your computer before trying to open it.
- Extract the ZIP file. This can be done with the default Windows tool (right-click, "Extract All...", click through the prompts) or dedicated software like 7-zip.

### Running The Application
- Open the `evictionstracker` folder so that you can see `parser.jar`, `parse.bat`, and `parse`. Leave this window aside for a moment.
- On your keyboard press *Windows key + R* and type `powershell` in the window that appears. This should open a blue window called "Microsoft PowerShell".
- Now we have to point PowerShell into the right folder. Type `cd` ("change directory") followed by a space. Return to the `evictionstracker` window you left aside earlier and click into the address bar (where it shows something like "This PC > Downloads > evictionstracker" -- clicking into this box should cause that text to change into something more like `C:\Users\yourname\Downloads\evictionstracker`). Copy this and paste it into PowerShell with *Ctrl+V*, then hit Enter.
- Nothing big will happen, but where it once read `PS C:\Users\yourname>` it should now read `PS {the path you pasted in}>`.
- Type `.\parse.bat` followed by a space. This text should be yellow.
- Locate on your computer the PDF file to be converted, then drag-and-drop it right into the PowerShell window. It should automatically fill in the path to the PDF file. This text should be white -- if it's not, make sure you have a space after `.\parse.bat`.
- Hit the spacebar again, then type what you would like to name the output file after conversion is complete. Make sure it ends in `.csv` or Windows won't know how to open it! If you forget, you can simply rename the output file once the conversion is complete (ignoring Windows' warning that you might break something by changing a file extension).
- Everything should be in place now; it's time to hit Enter and cross your fingers! The whole command should look something like this, noting the spaces: `.\parse.bat C:\Users\Yourname\Downloads\eviction_data.pdf output.csv`. If all goes well, you should get an output file in the `evictionstracker` folder with all of the data from the PDF. 
- Vet the CSV file for anything that might have gotten garbled during conversion; you may see some arcane error messages in PowerShell that mention "Java" if this happens.

## Linux Instructions
### Getting Started
This application uses Java 8 and Maven. If you do not have a local maven install, a maven wrapper is provided. The setup instructions will assume the use of the wrapper but feel free to use your own local install if you prefer.

### Prerequisites
- JDK 8

### Running The Application Locally
Clone the application and `cd` into the directory. Then run the following commands (the pkg script is a linux script, but is mostly optional):

```
./mvnw clean package
./pkg.sh
```

The ./mvnw clean package command will create a JAR file in the `target` directory. The `./pkg.sh` line will rename the JAR and bundle it with some utility scripts into `target/evictionsparser.zip` which is our distributable.

## Contributing
Contributions are welcome! If you wish to contribute we ask you please first contact either the repository owners or [DSA Cleveland](mailto:info@dsacleveland.org).

### Pull Request Process
1. Update the README.md to correct any information that has changed within the scope of your pull request.
2. Push your PR branch and request a PR with the github UI.
3. Inform a maintainer of your change request.

### Code of Conduct
This project is adherent to both the DSA Cleveland Code of Conduct and the [Contributor Covenant Code of Conduct](code_of_conduct.md). In places where the two contradict, the DSA Code of Conduct takes precedence.

# Authors
- [**Alvin Gao**](https://github.com/tehgao): Initial Work
- [**Koby Picker**](https://github.com/jkobyp): CSV construction

# License
This program is licensed under the terms of the GPLv3. See the [license](LICENSE.md) for more details.

# Acknowledgements
- DSA Cleveland Housing Justice Committee for providing guidance
