---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: b1d9aa1f212ce31a8bb7fadeff4e0ca8afcf05e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903750"
---
# Remove-AzWebAppSSLBinding

## 簡介
從上傳的憑證移除 SSL 綁定。

## 語法

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
**Remove-AzWebAppSSLBinding** Cmdlet 會從 Azure Web App 移除安全通訊端層 (SSL) 綁定。
SSL 系裝訂可用來將 Web App 與憑證關聯。

## 例子

### 範例 1：移除 Web App 的 SSL 綁定
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

此命令會移除 Web App ContosoWebApp 的 SSL 綁定。
由於 *DeleteCertificate* 參數不包含在內，如果憑證不再具有任何 SSL 綁定，將會刪除該憑證。

### 範例 2：移除 SSL 綁定而不移除憑證
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

與範例 1 類似，此命令也會移除 Web App ContosoWebApp 的 SSL 綁定。
不過，在此案例中，會包含 *DeleteCertificate* 參數，參數值會設為 $False。
這表示無論憑證是否具有任何 SSL 綁定，都將不會刪除。

### 範例 3：使用物件參照移除 SSL 綁定
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

此範例使用對 Web App 網站的物件參照來移除 Web App 的 SSL 綁定。
第一個命令使用 Get-AzWebApp Cmdlet 建立名為 ContosoWebApp 的 Web App 物件參照。
該物件參照會儲存在名為 $WebApp 的變數中。
第二個命令使用物件參照和 **Remove-AzWebAppSSLBinding** Cmdlet 來移除 SSL 綁定。

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

### -DeleteCertificate
指定移除 SSL 綁定時要採取的動作，這是憑證使用的唯一綁定。
如果 *DeleteCertificate* 設定為 $False，則刪除綁定時不會刪除憑證。
如果 *DeleteCertificate* 設定為 $True或不包含在命令中，憑證會連同 SSL 綁定一起刪除。
只有在要移除的 SSL 綁定是憑證使用的唯一綁定時，憑證才能刪除。
如果憑證具有一種以上裝訂，無論 *DeleteCertificate* 參數的值如何，都將不會移除憑證。

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

### -強制
強制執行命令，但不要求使用者確認。

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
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
指定 Web App 部署插槽。
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
您無法在 *ResourceGroupName* 參數和/或 *WebAppName* 的相同命令中，使用 WebApp 參數。 

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
指定 Web App 的名稱。
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

### -確認
執行 Cmdlet 之前，提示您確認。

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
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

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
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.WebApps.models.PSSite

## 輸出

### System.Void

## 筆記

## 相關連結

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


