---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283752"
---
# Get-AzWcfRelay

## 摘要
傳回指定 WcfRelay 的描述。

## 句法

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzWcfRelay** Cmdlet 會傳回指定 WcfRelay 的描述。

## 示例

### 範例1
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

傳回 WcfRelay 的描述。

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
WcfRelay [名稱]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -命名空間
命名空間名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSWcfRelayAttributes 中的 [.]

## 筆記

## 相關連結
