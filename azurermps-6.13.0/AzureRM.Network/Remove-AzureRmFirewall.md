---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmFirewall.md
ms.openlocfilehash: 1a6c5ae69ef6aa6dc0f64d118fcbc733c97e23a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448320"
---
# Remove-AzureRmFirewall

## 摘要
移除防火牆。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmFirewall** Cmdlet 會移除 Azure 防火牆。

## 示例

### 1：建立及刪除防火牆
```
New-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

這個範例會建立防火牆，然後將它刪除。 若要在刪除防火牆時取消提示，請使用-Force 標誌。

### 2：解除配置防火牆，然後刪除防火牆
```
$firewall=Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzureRmFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

這個範例會檢索防火牆、解除防火牆的釋放，然後刪除防火牆。 解除配置命令會移除執行中的服務，但會保留防火牆的設定。 如果使用者想要再次啟動服務，請在防火牆上呼叫 Allocate 方法。
若要在刪除防火牆時取消提示，請使用-Force 標誌。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
強制執行命令，而不要求使用者確認。

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

### -名稱
指定此 Cmdlet 移除的防火牆名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
傳回代表您正在使用之專案的物件。
根據預設，這個 Cmdlet 不會產生任何輸出。

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

### -ResourceGroupName
指定包含此 Cmdlet 移除之防火牆之資源群組的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PSAzureFirewall
已從管線接受類型 "PSAzureFirewall"

## 輸出

## 筆記

## 相關連結

[AzureRmFirewall](./Get-AzureRmFirewall.md)

[新-AzureRmFirewall](./New-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
