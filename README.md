  
# How to create a executable .desktop file

## What is a .desktop file
A .desktop file is a simple text file that holds information about a program. It follows a specific format and contains several key fields. The three categories of lines in a desktop entry file are `[Desktop Entry]`, `Key=Value` pairs, and `Comments` . The `Type` and `Name` keys are required for every desktop entry file . The `Exec` key defines the command to execute when launching the application . The `Icon` key specifies the path to the icon file associated with the application . The `.desktop` file is usually placed in `~/.local/share/applications` or `/usr/share/applications/`, depending on whether you want the launcher to be accessible for your local account only or for everyone .
# Step by Step guide
1. Navigate to the directory where you want to create the file.
2. Create a new file with the .desktop extension.
3. Open the file in a text editor.
4. Add the necessary information to the file, such as the name of the application, the command to run it, and the icon to use.
5. Save the file and exit the text editor.
6. Make the file executable by running the command `chmod +x filename.desktop` or right click  it and add permission to execute.
7. Move the file to `/usr/share/applications` or `/home/"Username"/.local/share/applications`
  
## Code Example
````Bash
[Desktop Entry]
Version=1.0
Name=jMemorize
Type=Application
Comment=Flash card based learning tool
Exec=/opt/jmemorise
Icon=/usr/share/icons/
Terminal=false
StartupNotify=true
Categories=Education
````
### Tips
- You can specify the full path to the executable in the `Exec` key. For example, if your executable is located at `/home/user/programs/myprogram`, you can set the `Exec` key to `/home/user/programs/myprogram`
- Should appear in the Menu(Show Applications button) or make a copy and put it on the Desktop.
### Extra Attributes
- `GenericName`: This key provides a generic name for the application, which can be used by the desktop environment to display the application in menus and other places.
- `Comment`: This key provides a brief description or comment about the application.
- `Categories`: This key specifies the categories in which the application should be shown. The categories are separated by semicolons.
- `MimeType`: This key specifies the MIME types that the application is capable of handling.
- `Keywords`: This key specifies a list of keywords that can be used to search for the application. The keywords are separated by semicolons.
- `StartupNotify`: This key specifies whether the desktop environment should be notified when the application starts up.
- `StartupWMClass`: This key specifies the WM_CLASS property of the main window of the application, which can be used by the desktop environment to group windows together.

# Software to create a .desktop file

- here is a GUI based software [Arronax](https://www.florian-diesch.de/software/arronax/index.html) for making a `.desktop` file
- [alexkdeveloper/desktop-files-creator](https://github.com/alexkdeveloper/desktop-files-creator) here an other one


# Resources 
[Desktop Entry Specification (specifications.freedesktop.org)](https://specifications.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html#value-types)</br>
[How to Create a .Desktop File for Your Application in Linux - Make Tech Easier](https://www.maketecheasier.com/create-desktop-file-linux/)

---


