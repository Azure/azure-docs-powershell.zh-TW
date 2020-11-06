---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 315c50dbbc68865058f6c5663952fe2f42bc5c85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446684"
---
# New-AzureRmRelayHybridConnection

## 摘要
在指定的中繼命名空間中建立 HybridConnection。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### HybridConnectionInputObjectSet
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-InputObject <HybridConnectionAttibutes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### HybridConnectionPropertiesSet
```
New-AzureRmRelayHybridConnection -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-RequiresClientAuthorization <Boolean>] [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
New-AzureRmRelayHybridConnection Cmdlet 會在指定的中繼命名空間中建立 HybridConnection。

## 示例

### 範例 1-InputObject
```
PS C:\> $getHybirdConnection = Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-HybirdConnection -Name TestHybirdConnection1
PS C:\> $getHybirdConnection.UserMetadata = "TestHybirdConnection2"
PS C:\> $getHybirdConnection.RequiresClientAuthorization = $False
PS C:\> New-AzureRmRelayHybridConnection -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection2 -InputObject $getHybirdConnection
```

\` \` 在指定的中繼命名空間 \` TestNameSpace-HybirdConnection 中建立新的 HybirdConnection TestHybirdConnection2 \` 。

### 範例 2-屬性
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-HybirdConnection -Name TestHybirdConnection1 -RequiresClientAuthorization $True -UserMetadata "User Meta data"
```

\` \` 在指定的中繼命名空間 \` TestNameSpace-HybirdConnection 中建立新的 HybirdConnection TestHybirdConnection1 \` 。

## 參數

### -RequiresClientAuthorization
如果此 HybridConnections 需要用戶端授權，則為 true;否則為 false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
取得或設定 usermetadata 是一個預留位置，用來儲存 HybridConnection 端點的使用者定義字串資料。例如，它可以用來儲存描述性資料，例如小組清單和連絡人資訊，也可以儲存使用者定義的設定設定。

```yaml
Type: System.String
Parameter Sets: HybridConnectionPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -InputObject
HybridConnections 物件。

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes
Parameter Sets: HybridConnectionInputObjectSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
HybridConnections [名稱]。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
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
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### -ResourceGroupName
System.object

### -NamespaceName
System.object

### -HybridConnectionsName
System.object

### -InputObject
HybridConnectionAttibutes 中的 [.]

### -RequiresClientAuthorization
System.object

### -UserMetadata
System.object

## 輸出

### HybridConnectionAttibutes 中的 [.]

### 範例-1： InputObject
CreatedAt： 4/26/2017 10:04:15 PM UpdatedAt： 4/26/2017 10:04:15 PM ListenerCount： RequiresClientAuthorization： True UserMetadata： User 中繼資料識別碼：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n2 Name： TestHybirdConnection2 類型： Microsoft. 中繼/HybridConnections

### 範例-2：屬性
CreatedAt： 4/26/2017 10:04:15 PM UpdatedAt： 4/26/2017 10:04:15 PM ListenerCount： RequiresClientAuthorization： True UserMetadata： User 中繼資料識別碼：/subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-HybirdConnection/HybridConnections/TestHybirdConnectio n1 Name： TestHybirdConnection1 Type： Microsoft. 中繼/HybridConnections

## 筆記

## 相關連結

