<div align="center">

## Hide Your Program


</div>

### Description

This code hides your applicatoin from CTRL+ALT+DEL List. Useful for spying purpose. Plz Do vote Me. or mail me for info , sirdneo@yahoo.com
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[M\. Zeeshan Umar](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/m-zeeshan-umar.md)
**Level**          |Intermediate
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |Microsoft Visual C\+\+
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__3-14.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/m-zeeshan-umar-hide-your-program__3-6666/archive/master.zip)





### Source Code

```
void Hide(void)
{
	typedef DWORD (__stdcall *pRegFunction)(DWORD, DWORD);
	HINSTANCE		hKernelLib;
	pRegFunction	RegisterServiceProcess;
	hKernelLib = LoadLibrary("kernel32.dll");
	if (hKernelLib)
	{
		RegisterServiceProcess = (pRegFunction)GetProcAddress(hKernelLib, "RegisterServiceProcess");
		if (RegisterServiceProcess)
			RegisterServiceProcess(GetCurrentProcessId(), 1);
		::FreeLibrary(hKernelLib);
	}						//change 1 to 0 for ctrl+alt+del to view app
}
```

