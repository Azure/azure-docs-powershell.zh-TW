---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284039"
---
# Update-AzCustomIpPrefix

## 摘要
更新 CustomIpPrefix

## 句法

### UpdateByNameParameterSet
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### UpdateByInputObjectParameterSet
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByResourceIdParameterSet
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzCustomIpPrefix** Cmdlet 可讓使用者在傭金或解除其 CustomIpPrefix，或編輯資源的標籤。

## 示例

### 範例1：傭金為 CustomIpPrefix
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

上述命令會啟動 CustomIpPrefix 的 commissioning 進程。

### 範例2：解除 CustomIpPrefix
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

上述命令會啟動 CustomIpPrefix 的取消 commissioning 進程。

### 範例3：更新 CustomIpPrefix 的標記
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

上述命令會更新 CustomIpPrefix 的標記。

## 參數

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -傭金
在背景中執行 Cmdlet

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Decomission
在背景中執行 Cmdlet

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
要設定的 CustomIpPrefix。

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -名稱
資源名稱。

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組的名稱。

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
[資源識別碼]。

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
代表資源標記的 hashtable。

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### PSCustomIpPrefix 中的 [.]

### [System.object] 集合. Hashtable

## 輸出

### PSCustomIpPrefix 中的 [.]

## 筆記

## 相關連結

[AzCustomIpPrefix](./Get-AzCustomIpPrefix.md)

[新-AzCustomIpPrefix](./New-AzCustomIpPrefix.md)

[移除-AzCustomIpPrefix](./Remove-AzCustomIpPrefix.md)