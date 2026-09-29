# Getting Started with C# in GitHub Codespaces

This guide explains how to check whether the .NET SDK is installed in your GitHub Codespace and how to create and run your first C# console application.

## 1. Open the Codespace Terminal

Open your GitHub Codespace and launch the terminal:

- Select **Terminal → New Terminal**
- Or use the keyboard shortcut:

```text
Ctrl + `
```

## 2. Check Whether .NET Is Installed

Run the following command:

```bash
dotnet --version
```

If .NET is installed, the terminal displays a version number, for example:

```text
8.0.404
```

You can also view detailed .NET information:

```bash
dotnet --info
```

## 3. Create a C# Console Application

If the `dotnet --version` command works, create a new console application:

```bash
dotnet new console -n MyApp
```

This creates a new folder named `MyApp` containing a basic C# project.

Move into the project directory:

```bash
cd MyApp
```

## 4. Run the Application

Start the application:

```bash
dotnet run
```

You should see:

```text
Hello, World!
```

Congratulations! You have successfully created and run your first C# application.

## Complete Command Sequence

Run the following commands in order:

```bash
dotnet --version
dotnet new console -n MyApp
cd MyApp
dotnet run
```

## 5. If .NET Is Not Installed

If you see an error such as:

```text
dotnet: command not found
```

you need to add the .NET development environment to your Codespace.

### Add the C#/.NET Dev Container Configuration

1. Press:

   ```text
   Ctrl+Shift+P
   ```

2. Search for and select:

   ```text
   Codespaces: Add Dev Container Configuration Files
   ```

3. Select:

   ```text
   Create a new configuration
   ```

4. Select:

   ```text
   C# (.NET)
   ```

5. Choose the required .NET version.

6. Select **Dotnet CLI** if prompted.

7. Choose:

   ```text
   Rebuild Now
   ```

Rebuilding the container installs the .NET SDK and configures the Codespace for C# development.

## 6. Verify the Installation

After the Codespace finishes rebuilding, open a new terminal and run:

```bash
dotnet --version
```

If a version number appears, the installation was successful.

You can now create and run a project:

```bash
dotnet new console -n MyApp
cd MyApp
dotnet run
```

## 7. Create a Project in the Current Directory

If you want to create the C# project in the folder you are currently using, run:

```bash
dotnet new console
dotnet run
```

## 8. Important Files in a C# Project

A newly created console project usually contains:

```text
MyApp/
├── MyApp.csproj
└── Program.cs
```

- `Program.cs` contains the C# source code.
- `MyApp.csproj` contains project configuration and dependencies.
- The project can be built and run using the .NET CLI.

## 9. Edit the Program

Open `Program.cs` and replace its contents with:

```csharp
Console.WriteLine("Welcome to C#!");
```

Run the application again:

```bash
dotnet run
```

The output should be:

```text
Welcome to C#!
```

## Troubleshooting

### `dotnet: command not found`

The .NET SDK is not installed or is not available in the current environment. Follow the **Add the C#/.NET Dev Container Configuration** steps above and rebuild the Codespace.

### The project does not run

Make sure you are inside the project directory:

```bash
cd MyApp
dotnet run
```

You can check your current directory with:

```bash
pwd
```

### Check the Installed SDK

Run:

```bash
dotnet --list-sdks
```

This displays all .NET SDK versions installed in the Codespace.

## Happy Coding!
