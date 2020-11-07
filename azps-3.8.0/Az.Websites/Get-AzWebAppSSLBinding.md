---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957955"
---
# Get-AzWebAppSSLBinding

## 摘要
取得 Azure Web App 憑證 SSL 系結。

## 句法

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

## 說明
**AzWebAppSSLBinding** Cmdlet 會針對 Azure Web APP (SSL) 系結，取得安全通訊端層。
SSL 系結是用來將 Web 應用程式與上傳的憑證建立關聯。
Web 應用程式可以系結至多個憑證。

## 示例

### 範例1：取得 Web 應用程式的 SSL 系結
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

這個命令會檢索與資源群組 ContosoResourceGroup 相關聯的 Web App ContosoWebApp SSL 系結。

### 範例2：使用物件參考來取得 Web 應用程式的 SSL 系結
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

這個範例中的命令也會取得 Web 應用程式 ContosoWebApp 的 SSL 系結;但在此情況下，會使用物件參照，而不是使用 Web App 名稱和相關聯的資源群組的名稱。
這個物件參照是由範例中的第一個命令所建立，它使用 **AzWebApp** 來建立名為 ContosoWebApp 的 Web App 的物件參考。
該物件參照會儲存在名為 $WebApp 的變數中。
這個變數及 **AzWebAppSSLBinding** Cmdlet 接著是由第二個命令用來取得 SSL 系結。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定 SSL 系結的名稱。

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
指定指派憑證的資源群組的名稱。
您無法在同一命令中使用 *ResourceGroupName* 參數和 *WebApp* 參數。

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

### -槽
指定 Web 應用程式部署槽。
若要取得部署槽，請使用 Get-AzWebAppSlot Cmdlet。

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
指定 Web 應用程式。
若要取得 Web 應用程式，請使用 Get-AzWebApp Cmdlet。

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
指定此 Cmdlet 取得 SSL 系結的 Web App 名稱。
您無法在同一命令中使用 *WebAppName* 參數和 *WebApp* 參數。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSSite 中的 WebApps。

## 輸出

### HostNameSslState 中的 [網站]。

## 筆記

## 相關連結

[新-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[移除-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[AzWebApp](./Get-AzWebApp.md)


