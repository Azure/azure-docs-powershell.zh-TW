---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907346"
---
# Get-AzWebAppSSLBinding

## 簡介
獲得 Azure Web App 憑證 SSL 綁定。

## 語法

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzWebAppSSLBinding** Cmdlet 會為 Azure Web App (SSL) 安全通訊端層。
SSL 系帶可用來將 Web App 與上傳的憑證建立關聯。
Web App 可以綁定至多個憑證。

## 例子

### 範例 1：取得 Web App 的 SSL 綁定
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

此命令會針對與資源群組 ContosoResourceGroup 相關聯的 Web App ContosoWebApp，來取回 SSL 綁定。

### 範例 2：使用物件參照取得 Web App 的 SSL 綁定
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

此範例中的命令也會取得 Web App ContosoWebApp 的 SSL 綁定;不過，在此案例中，會使用物件參照，而不是使用 Web App 名稱和相關聯的資源組名。
此物件參照是由範例中的第一個命令所建立，該命令使用 **Get-AzWebApp** 建立名為 ContosoWebApp 的 Web App 物件參照。
該物件參照會儲存在名為 $WebApp 的變數中。
接著，第二個命令會使用 **這個變數和 Get-AzWebAppSSLBinding** Cmdlet 來取得 SSL 綁定。

## 參數

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
指定 SSL 綁定的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
指定 Web App 部署時段。
若要取得部署插槽，請使用 Get-AzWebAppSlot Cmdlet。

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
指定 Web App。
若要取得 Web App，請使用 Get-AzWebApp Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
指定此 Cmdlet 可獲取 SSL 綁定的 Web App 名稱。
您無法在同一個命令中使用 *WebAppName* 參數和 *WebApp* 參數。

```yaml
Type: System.String
Parameter Sets: S1
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

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


