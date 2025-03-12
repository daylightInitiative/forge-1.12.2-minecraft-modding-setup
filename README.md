# Preface
These instructions tell you how to setup a legacy forge environment, this is for people who wish to create and or modify an existing mod for 1.12.2 with hotswapping. Hotswapping is the ability to reload classes while the game is running without the need for restart.
#### This tutorial uses intellij, if you have a reproducable method for eclipse, submit a pull request

# Setting up the environment
First install java 1.8.0_181, I reccomend the one from oracle. 
* https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html (Requires an account)
* https://www.azul.com/downloads/?package=jdk#zulu
* https://docs.aws.amazon.com/corretto/latest/corretto-8-ug/downloads-list.html


#### Warning: Hotswapping may be incompatible with other jdk distributions besides oracle's offical one, currently it is the only tested one that works.

## Intellij 2021.1.3
I have no idea why, but this is the only version of intellij I have found to work. Make sure you install 2021.1.3 of the community edition.
https://www.jetbrains.com/idea/download/other.html

![image](https://github.com/user-attachments/assets/a218c37a-c656-4f92-b613-8f7f176012e5)


## Downloading the template empty project
For fast setup, I have pre-packaged the 1.12.2 mdk and an empty intelliJ project into a zip file.
Download and unzip: https://github.com/daylightInitiative/forge-1.12.2-minecraft-modding-setup/blob/master/Forge1.12_template.zip

Drag the folder outside of the zip file and rename it to your project name, it should look something like this:
![image](https://github.com/user-attachments/assets/80a4b3cb-00ca-43c5-919e-111e586cc6a9)

In intellij change, File->Project Structure->Project SDK to the java 8 you installed version (1.8.0_181)

Now, Open up the project in IntelliJ and in the terminal run the following commands for setup:

```
gradlew.bat
gradlew.bat build
gradlew.bat genIntellijRuns
```

