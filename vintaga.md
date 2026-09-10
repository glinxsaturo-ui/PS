Enable-WindowsOptionalFeature -Online -FeatureName IIS-FTPServer -All
$password = ConvertTo-SecureString "VINTAGA" -AsPlainText -Force
New-LocalUser `
    -Name "user" `
    -Password $password `
    -FullName "FTP User" `
    -Description "FTP "
