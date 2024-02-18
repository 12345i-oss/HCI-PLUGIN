# EA Plugin Setup Guide

This guide outlines the steps to create and set up an EA plugin using Visual Studio.

## Step 1: Create the Class Library Project

1. Open Visual Studio.
2. Start a new project.
3. Choose "Class Library" as the type of project.

## Step 2: Add EA API Assembly Reference

1. Right-click on your project in the Solution Explorer.
2. Choose "Add" > "Reference...".
3. Select the "Browse" tab.
4. Navigate to the EA installation folder (default: [Program Files]\Sparx Systems\EA).
5. Select the file "Interop.EA.dll".
6. Click "OK" to add the reference.

## Step 3: Configure Build Options

1. Double-click on the "Properties" folder under your project.
2. Click on the "Assembly Information" button.
3. Check the checkbox that says "Make assembly COM-visible".
4. Go to the "Build" tab.
5. Check the checkbox "Register for COM interop".

## Step 4: Rename and Modify Class

1. Rename the default `Class1.cs` to `MyAddinClass.cs`.
2. Replace the existing template code with your own code for the add-in functionality.

## Step 5: Add Registry Key

1. Open the Registry Editor (press Win + R, type `regedit`, and press Enter).
2. Navigate to `HKEY_CURRENT_USER\Software\Sparx Systems\EAAddins`.
3. Create a new key with a meaningful name.
4. Set the default value of the key to `[Namespace].[ClassName]` (e.g., `MyAddin.MyAddinClass`).

## Step 6: Try it Out in EA

1. Launch EA.
2. Open a project.
3. Right-click on an element in the project browser or a diagram.
4. You should see your additional menu option with the defined options.

## Contributing

We welcome contributions to enhance this EA plugin. To contribute, please fork the repository and submit pull requests.


