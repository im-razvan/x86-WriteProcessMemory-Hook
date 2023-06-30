# x86 WriteProcessMemory Hook (V1.1)

🔗 Introduction

This is a simple project that hooks the `WriteProcessMemory` function in x86 (32-bit) Windows processes. It saves the `lpBuffer` parameter to a file called `dump_{processname}.bin` whenever `WriteProcessMemory` is called. The compiled hook is available as a DLL named `dumper_razvan.dll`.

💡 Usage

1. Inject the `dumper_razvan.dll` into the target process.

2. Once the `dumper_razvan.dll` is injected into the target process, it will automatically hook the `WriteProcessMemory` function and start saving the `lpBuffer` parameter to the `dump_{processname}.bin` file.

3. The `dump_{processname}.bin` file will be created in the same directory as the target process executable. If the file already exists, the new data will be appended to the existing file.

⚠️ Limitations

- The project is only compatible with x86 (32-bit) Windows processes.
- The hooking mechanism might not work on protected processes or processes with anti-debugging measures.
- Private source code.

🔧 Example

Let's say that you want to dump a CS:GO cheat that has a loader that injects in both Steam and CS:GO. After the injection is completed, you will be left with two dump files: one called `dump_steam.bin` and the other one `dump_csgo.bin`.

---