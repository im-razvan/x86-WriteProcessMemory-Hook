# x86 WriteProcessMemory Hook

🔗🔧 Introduction

This is a simple project that hooks the `WriteProcessMemory` function in x86 (32-bit) Windows processes. It saves the `lpBuffer` parameter to a file called `dump.bin` whenever `WriteProcessMemory` is called. The compiled hook is available as a DLL named `dumper_razvan.dll`.

💡 Usage

1. Inject the `dumper_razvan.dll` into the target process.

2. Once the `dumper_razvan.dll` is injected into the target process, it will automatically hook the `WriteProcessMemory` function and start saving the `lpBuffer` parameter to the `dump.bin` file.

3. The `dump.bin` file will be created in the same directory as the target process executable. If the file already exists, the new data will be appended to the existing file.

⚠️ Limitations

- The project is only compatible with x86 (32-bit) Windows processes.
- The hooking mechanism might not work on protected processes or processes with anti-debugging measures.
- Private source code.

Enjoy using the `dumper_razvan.dll` to hook `WriteProcessMemory` and capture data with ease! 🎉

---