Enable-WindowsOptionalFeature -Online -FeatureName IIS-FTPServer -All
$password = ConvertTo-SecureString "VINTAGA" -AsPlainText -Force
New-LocalUser `
    -Name "ftpuser" `
    -Password $password `
    -FullName "FTP User" `
    -Description "FTP "
