---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 52e5dce154b6798a0bddb0416235d371d6c85910
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449669"
---
# Remove-AzureRmWebAppSSLBinding

## 摘要
從上傳的憑證中移除 SSL 系結。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### S1
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmWebAppSSLBinding** Cmdlet 會從 Azure Web APP (SSL) 系結來移除安全通訊端層。
SSL 系結是用來將 Web App 與憑證建立關聯。

## 示例

### 範例1：移除 web 應用程式的 SSL 系結
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

這個命令會移除 web 應用程式 ContosoWebApp 的 SSL 系結。
由於不包含 *DeleteCertificate* 參數，因此如果證書不再有任何 SSL 系結，就會將它刪除。

### 範例2：移除 SSL 系結但不移除憑證
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

與範例1類似，這個命令也會移除 Web App ContosoWebApp 的 SSL 系結。
但在此情況下，會包含 *DeleteCertificate* 參數，而參數值會設定為 $False。
這表示無論是否有任何 SSL 綁定，證書都不會被刪除。

### 範例3：使用物件參照來移除 SSL 系結
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

這個範例使用 Web App 網站的物件參考來移除 Web 應用程式的 SSL 系結。
第一個命令使用 Get-AzureRmWebApp Cmdlet 來建立名為 ContosoWebApp 的 Web App 的物件參考。
該物件參照會儲存在名為 $WebApp 的變數中。
第二個命令使用物件參照和 **AzureRmWebAppSSLBinding** Cmdlet 來移除 SSL 系結。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteCertificate
指定在移除 SSL 系結是憑證所使用的唯一系結時要發生的動作。
如果 *DeleteCertificate* 設定為 $False，則刪除系結時，不會刪除憑證。
如果 *DeleteCertificate* 設定為 $True 或不包含在命令中，則會將憑證與 SSL 系結一起刪除。
只有在已移除 SSL 系結是認證所使用的唯一系結時，才能刪除證書。
如果憑證有一個以上的系結，不論 *DeleteCertificate* 參數的值為何，都不會移除證書。

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定 Web 應用程式的名稱。

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
若要取得部署槽，請使用 Get-AzureRMWebAppSlot Cmdlet。

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
若要取得 Web 應用程式，請使用 Get-AzureRmWebApp Cmdlet。
您無法在與 *ResourceGroupName* 參數和/或 *WebAppName* 相同的命令中使用 *WebApp* 參數。

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
指定 Web 應用程式的名稱。
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

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### [Microsoft Azure. 管理] 網站
參數： WebApp (ByValue) 

## 輸出

### System.void

## 筆記

## 相關連結

[AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[新-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[AzureRmWebApp](./Get-AzureRmWebApp.md)


