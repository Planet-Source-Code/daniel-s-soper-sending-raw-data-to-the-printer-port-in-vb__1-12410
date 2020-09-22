<div align="center">

## Sending Raw Data to the Printer Port in VB


</div>

### Description

Have you ever tried to send raw data to a printer port (LPT1 for example) using Visual Basic without using VB's printer object or an outside DLL or API? If you have then you know that it is virtually impossible because Visual Basic cannot directly access any system devices. This very simple code demonstrates how to use an undocumented feature of VB's 'OPEN' statement to allow direct access to the printer port as if it were a file. Accessing system devices as if they were a file is a method that was built into the old DOS-based versions of Basic, but until now I was unaware that this functionality still exists in Visual Basic. This method even works in Windows 2000, which is supposed to block direct port access for security purposes.
 
### More Info
 
Whatever raw data you want to send to the printer port. This data should be in string format.

Using this code bypasses Windows' built in print spooler, and sends only raw data to the printer port.

None known. Tested on Windows 98 and Windows 2000 Professional.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Daniel S\. Soper](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/daniel-s-soper.md)
**Level**          |Intermediate
**User Rating**    |4.8 (63 globes from 13 users)
**Compatibility**  |VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/daniel-s-soper-sending-raw-data-to-the-printer-port-in-vb__1-12410/archive/master.zip)

### API Declarations

None. =-]


### Source Code

```
Dim printString as String
printString = "Sample Raw Data"
Open "LPT1:" For Output Access Write As #1
 Print #1, printString
Close #1
```

