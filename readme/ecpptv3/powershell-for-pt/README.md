# 1️⃣ 1 - Resource Development & Initial Access

#### Topics

> 1. [PowerShell for Pentesters](3.1.md)
> 2. [Client-Side Attacks](network-security/2.3/client-side-attacks.md)

## What is a PowerShell?

{% embed url="https://learn.microsoft.com/en-us/powershell/scripting/overview?view=powershell-7.4" %}

{% embed url="https://github.com/PowerShell/PowerShell" %}

## PowerShell and IDE

<details>

<summary>Powershell.exe and IDE</summary>

**PowerShell** is typically available in two main executable forms: `powershell.exe` and `powershell_ise.exe`. Each serves a different purpose in the PowerShell ecosystem.

1.  **powershell.exe:**

    * This is the standard PowerShell command-line interface (CLI) executable. When you open a regular PowerShell console or run PowerShell commands from the command prompt, you are interacting with `powershell.exe`.
    * You can use `powershell.exe` to execute individual commands, run scripts, and perform various administrative tasks using PowerShell.

    Example usage in the command prompt:

    ```arduino
    arduinoCopy codepowershell.exe -Command "Get-Process"
    ```
2.  **powershell\_ise.exe:**

    * This is the executable for the PowerShell Integrated Scripting Environment (ISE). The ISE is an interactive development environment for PowerShell scripting. It provides a graphical user interface (GUI) for writing, testing, and debugging PowerShell scripts.
    * The ISE includes features such as a script editor, a command pane, and a script output pane, making it easier for users to work with PowerShell scripts and functions.

    Example usage in the command prompt:

    ```
    Copy codepowershell_ise.exe
    ```

    When you run the `powershell_ise.exe` command, it opens the PowerShell ISE window.

In summary, `powershell.exe` is the standard command-line interface for executing PowerShell commands, while `powershell_ise.exe` is used to open the PowerShell Integrated Scripting Environment for script development and testing in a more interactive and visual manner. Users often choose between these executables based on their specific needs and preferences for working with PowerShell.

</details>

## PowerShell Commands

<details>

<summary>PowerShell Commands</summary>



In PowerShell, there are several types of commands, each serving a specific purpose and role in scripting and automation. Here's an overview of PowerShell cmdlets, functions, scripts, and native commands:

1. **Cmdlets (Commandlets):**
   * Cmdlets are lightweight commands in PowerShell. They are .NET classes with methods that perform specific tasks. Cmdlets follow a Verb-Noun naming convention (e.g., `Get-Process`, `New-Item`).
   * Cmdlets are the primary building blocks for PowerShell commands, and they are designed to be easily discoverable and consistent.
2.  **Functions:**

    * Functions in PowerShell allow you to group a series of PowerShell statements into a reusable unit. You can define functions to perform specific tasks, and they can accept parameters and return values.
    * Functions are useful for modularizing your code and avoiding code duplication. They can be defined within scripts or loaded from modules.

    Example of a simple function:

    ```powershell
    powershellCopy codefunction Get-Square {
        param (
            [int]$Number
        )
        $Square = $Number * $Number
        return $Square
    }
    ```

    Usage:

    ```powershell
    powershellCopy codeGet-Square -Number 5
    ```
3.  **Scripts:**

    * PowerShell scripts are sequences of PowerShell commands saved in a text file with a `.ps1` extension. Scripts can contain a series of cmdlets, functions, logic, and control flow statements.
    * Running a script is a way to execute a sequence of PowerShell commands as a single unit.

    Example script (`MyScript.ps1`):

    ```powershell
    powershellCopy code# MyScript.ps1
    Get-Process
    ```

    Running the script:

    ```powershell
    powershellCopy code.\MyScript.ps1
    ```
4.  **Native Commands (External Commands):**

    * PowerShell can also interact with external commands, executables, or scripts written in other languages (e.g., batch files, executable programs). These are referred to as native commands.
    * You can call native commands using the `&` operator or the `Invoke-Expression` cmdlet.

    Example of calling a native command:

    ```powershell
    powershellCopy code& "C:\Path\To\Your\Executable.exe" -Parameter1 Value1
    ```

    Keep in mind that while native commands can be called from PowerShell, the preferred and more PowerShell-centric approach is to use cmdlets and functions whenever possible for better consistency and integration with the PowerShell environment.

</details>

### Cmdlet

{% embed url="https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/cmdlet-overview?view=powershell-7.4" %}

{% hint style="danger" %}
#### ❗ Disclaimer

* **Never use tools and techniques on real IP addresses, hosts or networks without proper authorization!**
{% endhint %}
