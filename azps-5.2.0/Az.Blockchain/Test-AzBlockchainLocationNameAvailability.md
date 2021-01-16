---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/test-azblockchainlocationnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Test-AzBlockchainLocationNameAvailability.md
ms.openlocfilehash: 42bd50dd96d235db823ec12498388f78d5ec641c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282359"
---
# Test-AzBlockchainLocationNameAvailability

## 摘要
檢查資源名稱是否可用。

## 句法

```
Test-AzBlockchainLocationNameAvailability -Location <String> [-SubscriptionId <String>] [-Name <String>]
 [-Type <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## 說明
檢查資源名稱是否可用。

## 示例

### 範例1：檢查資源名稱是否可供使用
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name erw123 -type Microsoft.Blockchain/blockchainMembers

Message NameAvailable Reason
------- ------------- ------
        True          NotSpecified
```

該命令會檢查資源名稱是否可用。

### 範例2：檢查資源名稱是否可供使用
```powershell
PS C:\> Test-AzBlockchainLocationNameAvailability -Location eastus -Name 123 -Type Microsoft.Blockchain/blockchainMembers

Message                                                                                                                                                                             NameAvailable Reason
-------                                                                                                                                                                             ------------- ------
The blockchain member name is invalid. It can contain only lowercase letters and numbers. The first character must be a letter. The value must be between 2 and 20 characters long. False         Invalid
```

該命令會檢查資源名稱是否可用。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -位置
位置名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
取得或設定要檢查的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。
訂閱識別碼是每個服務呼叫 URI 的一部分。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -類型
取得或設定要檢查的資源類型。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

## 輸出

### INameAvailability （Blockchain）。 Api20180601Preview。

## 筆記

別名

## 相關連結

