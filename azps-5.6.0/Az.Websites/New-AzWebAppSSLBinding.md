---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 3429868b1d603606f64c75ec23505cf63f9ade03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914241"
---
# New-AzWebAppSSLBinding

## 簡介
為 Azure Web App 建立 SSL 憑證綁定。

## 語法

### S1
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S3
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### S4
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzWebAppSSLBinding** Cmdlet 會為 Azure Web App 建立安全通訊端層 (SSL) 憑證綁定。
Cmdlet 會以兩種方式建立 SSL 綁定： 
- 您可以將 Web App 綁定至現有的憑證。
- 您可以上傳新憑證，然後將 Web App 綁定至此新憑證。
無論您使用哪種方法，憑證和 Web App 都必須與相同的 Azure 資源群組相關聯。
如果您在資源群組 A 中擁有 Web App，而且想要將 Web App 綁定至資源群組 B 中的憑證，唯一的方法就是將憑證的一份副本上傳到資源群組 A。如果您上傳新的憑證，請記住 Azure SSL 憑證的下列需求： 
- 憑證必須包含私密金鑰。 
- 憑證必須使用個人資訊 Exchange (PFX) 格式。 
- 憑證的主體名稱必須與用來存取 Web App 的網域相符。 
- 憑證必須至少使用 2048 位加密。

## 例子

### 範例 1：將憑證綁定至 Web App
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

此命令會使用 Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) 將現有的 (Azure 憑證) 與名為 ContosoWebApp 的憑證綁定。

### 範例 2

為 Azure Web App 建立 SSL 憑證綁定。  (自動) 

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## 參數

### -CertificateFilePath
指定要上傳之憑證的檔案路徑。
只有在憑證尚未上傳到 Azure 時，才需要 *CertificateFilePath* 參數。

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
指定憑證的解密密碼。

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定 Web App 的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定憑證指派給的資源組名。
您無法在同一 *個命令中使用 ResourceGroupName* 參數和 *WebApp* 參數。

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
指定 Web App 部署時段的名稱。
您可以使用 Cmdlet Get-AzWebAppSlot取得插槽。
部署插槽提供一種方式，方便您進行階段和驗證 Web App，而不需要這些 App 可經由網際網路進行。
一般來說，您將將變更部署到暫存網站、驗證這些變更，然後部署到可 (網際網路) 生產。

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SslState
指定憑證是否已啟用。
將 *SSLState* 參數設為 1 以啟用憑證，或將 *SSLState 設為* 0 以停用憑證。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -拇指列印
指定憑證的唯一識別碼。

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
指定 Web App。
若要取得 Web App，請使用 Get-AzWebApp Cmdlet。
您無法在 *ResourceGroupName* 參數和/或 *WebAppName* 的相同命令中，使用 WebApp 參數。 

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
指定要建立新 SSL 裝訂的 Web App 名稱。
您無法在同一個命令中使用 *WebAppName* 參數和 *WebApp* 參數。

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.WebApps.models.PSSite

## 輸出

### Microsoft.Azure.management.Websites.models.HostNameSslState

## 筆記

## 相關連結

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


