---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 196cc354ddac7f317400b7baa665b8975dcc9df9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622016"
---
# Get-AzExpressRoutePortsLocation

## 摘要
取得 ExpressRoutePort 資源可供使用的位置。

## 句法

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzExpressRoutePortsLocation** Cmdlet 是用來檢索 ExpressRoutePort 資源可用的位置。 已知特定位置作為輸入，此 Cmdlet 會顯示該位置的詳細資料，例如該位置的可用頻寬清單。

## 示例

### 範例1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

列出可用 ExpressRoutePort 資源的位置。

### 範例2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

列出 $loc 位置的可用 ExpressRoutePort 頻寬。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -LocationName
位置的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSExpressRoutePortsLocation 中的 [.]

## 筆記

## 相關連結
