

# Step-by-Step Guide for Building `rubix.exe` for Windows
More about Rubix here - https://www.rubix.net/

This guide will walk you through the process of building the `rubix.exe` executable for Windows.

## Prerequisites

Before you begin, ensure that you have the following prerequisites installed on your system:

1. **Git:** https://git-scm.com/
2. **Go programming language:** https://golang.org/doc/install 
3. **Chocolate** (Required for make): https://chocolatey.org/install#individual (PowerShell with Admin Privilege preferred)
4. **cmake:** Once the Chocolate is installed, choco install cmake (PowerShell with Admin Privilege preferred)
5. **make:** Once the Chocolate is installed, choco install make (PowerShell with Admin Privilege preferred)
6. TDM-GCC: https://jmeubank.github.io/tdm-gcc/

Once the prerequisites are installed, close the PowerShell and open it again with admin privilege. This step is important! 

## Step 1: Clone the Repository

1. Open your command prompt or terminal or github desktop app.

2. Clone the `rubixgoplatform` repository in development mode using the following command:

   ```sh
   git clone https://github.com/rubixchain/rubixgoplatform.git
   ```

3. Change your current working directory to the cloned repository:

   ```sh
   cd rubixgoplatform
   ```

## Step 2: Switch to the `develop` Branch

1. To ensure you are on the `develop` branch, execute the following command:

   ```sh
   git checkout develop
   ```

## Step 3: Build `rubix.exe`

1. To build the `rubix.exe` executable for Windows, use the following command:

   ```sh
   make compile-windows
   ```

   This command will set the necessary environment variables, download dependencies, and compile the executable.

   Note: If you get any build errors, check for missing prerequisites or remove the .git folder temporarily (move to the recycle bin or another folder or rename) and try to build again.

## Step 4: Locate the `rubix.exe` Executable

1. Once the compilation process is complete, you can find the `rubix.exe` executable in the `windows` folder within your project directory (`rubixgoplatform`).

   Example path: `rubixgoplatform/windows/rubixgoplatform.exe`

## Congratulations!

You have successfully built the `rubix.exe` executable for Windows using the `make compile-windows` command. You can now use this executable to run various commands as needed for your project.

<footer>
© Meta Jupiter Software Solutions Private Limited (Jupiter Meta) - https://www.jupitermeta.io
</footer>
