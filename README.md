# Source installation information for modders

This code follows the Minecraft Forge installation methodology. It will apply
some small patches to the vanilla MCP source code, giving you and it access
to some of the data and functions you need to build a successful mod.

Note also that the patches are built against "unrenamed" MCP source code (aka
srgnames) - this means that you will not be able to read them directly against
normal code.

Source pack installation information:

## Standalone source installation

See [the Forge Documentation](http://mcforge.readthedocs.io/en/latest/gettingstarted/) online for more detailed instructions.

1. Open your command-line and browse to the folder where you extracted the zip file.

2. You're left with a choice.
   **Eclipse**

   1. Run the following command: "gradlew genEclipseRuns" (./gradlew genEclipseRuns if you are on Mac/Linux)

   2. Open Eclipse, Import > Existing Gradle Project > Select Folder
      or run "gradlew eclipse" to generate the project.
      (Current Issue)

   3. Open Project > Run/Debug Settings > Edit runClient and runServer > Environment

   4. Edit MOD_CLASSES to show [modid]%%[Path]; 2 times rather then the generated 4.

   **IntelliJ IDEA**

   1. Open IDEA, and import project.

   2. Select your build.gradle file and have it import.

   3. Run the following command: "gradlew genIntellijRuns" (./gradlew genIntellijRuns if you are on Mac/Linux)

   4. Refresh the Gradle Project in IDEA if required.

   **Visual Studio Code**

   1. Open project root in Code.

   2. Assuming you have [Gradle Tasks](https://marketplace.visualstudio.com/items?itemName=richardwillis.vscode-gradle), in the activity bar: Gradle > Gradle Tasks > [this project] > fg_runs > genVSCodeRuns

   3. Restart VS Code if required.

If at any point you are missing libraries in your IDE, or you've run into problems you can run "gradlew --refresh-dependencies" to refresh the local cache. "gradlew clean" to reset everything {this does not affect your code} and then start the process again.

Should it still not work,
Refer to #ForgeGradle on EsperNet for more information about the gradle environment.
or the [Forge Project Discord](discord.gg/UvedJ9m)

## Forge source installation

MinecraftForge ships with this code and installs it as part of the forge
installation process, no further action is required on your part.

For more details update more often refer to the [Forge Forums](http://www.minecraftforge.net/forum/index.php/topic,14048.0.html)
