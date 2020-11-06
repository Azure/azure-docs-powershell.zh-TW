---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceKey.md
ms.openlocfilehash: 5b366a3be8ca715a42c1c1f916d8ebf327dff8fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452348"
---
# New-AzureRmServiceBusNamespaceKey

## 摘要
重新產生服務匯流排命名空間的主要或次要連接字串。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
New-AzureRmServiceBusNamespaceKey [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmServiceBusNamespace** Cmdlet 會針對指定的命名空間和授權規則產生新的主要或次要連接字串。

## 示例

### 範例1
```
PS C:\> New-AzureRmServiceBusNamespaceKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -RegenerateKeys PrimaryKey
```

重新生成命名空間的主要或次要連接字串。

## 參數

### -RegenerateKeys
重新產生金鑰： PrimaryKey/SecondaryKey。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroup
資源群組的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroupName

Required: True
Position: 0
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

### -名稱
授權規則名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

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
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### -ResourceGroup
 System.object
 

### -NamespaceName
 System.object
 

### -AuthorizationRuleName
 System.object
 

### -RegenerateKeys
 System.object

## 輸出

### ResourceListKeys （即 Azure。
PrimaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey 值} SecondaryConnectionString： Endpoint = sb：//sb-example1.servicebus.windows.net/;SharedAccessKeyName = AuthoRule1;SharedAccessKey = {SharedAccessKey 值} PrimaryKey： {PrimaryKey 值} SecondaryKey： {SecondaryKey 值} KeyName： AuthoRule1

## 筆記

## 相關連結

