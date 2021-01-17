---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437943"
---
# Get-AzExpressRoutePort

## 摘要
取得 Azure ExpressRoutePort 資源。

## 句法

### ResourceNameParameterSet (預設) 
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzExpressRoutePort** Cmdlet 是用來從您的訂閱中檢索 ExpressRoutePort 物件。 傳回的 expressrouteport 物件可以用來做為在 ExpressRoutePort 上執行的其他 Cmdlet 的輸入。

## 示例

### 範例1
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

取得您訂閱中的 [資源群組] $rg 中名稱 $PortName 的 ExpressRoutePort 物件。

### 範例2
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

取得名稱以「test」開頭的所有 ExpressRoutePort 物件。

### 範例3
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

取得 ExpressRoutePort 物件，其中包含 ResourceId $id。 

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

### -名稱
ExpressRoutePort 的名稱。

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
ExpressRoutePort 的資源組名稱。

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceId
快速路由埠的 ResourceId。

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

## 輸出

### PSExpressRoutePort 中的 [.]

## 筆記

## 相關連結

[新-AzExpressRoutePort](./New-AzExpressRoutePort.md)

[移除-AzExpressRoutePort](./Remove-AzExpressRoutePort.md)

[Set-AzExpressRoutePort](./Set-AzExpressRoutePort.md)
