# Base64 Encoding Images in PowerShell

I needed to embed a couple of additional images into a HTML file. The output file already had a couple of base64 encoded SVGs within it, so I decided to try doing the same with the additional images.

Instead of using an online encoding service I tried to find if I could do it in PowerShell. I found the following solution.

```powershell
[Convert]::ToBase64String((Get-Content -Path .\myImage.png -Encoding Byte)) >> myImage.txt
```

## Explainer

```[Convert]::ToBase64String``` calls the ToBase64String method of the .NET Conversion class. Essentially using a .NET library to do the lifting. 

I then pass PowerShells Get-Content cmdlet as an argument with the path to the image. 

```>>``` simply redirects the output of the Convert method to a text file.

I can then paste the output of the text file into the HTML ```<img>``` tag.