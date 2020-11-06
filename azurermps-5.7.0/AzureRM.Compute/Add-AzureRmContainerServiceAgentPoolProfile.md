---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450700"
---
# Add-AzureRmContainerServiceAgentPoolProfile

## 摘要
新增容器服務代理程式組件池設定檔。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmContainerServiceAgentPoolProfile** Cmdlet 會將容器服務代理程式池設定檔新增到本機容器服務物件。

## 示例

### 範例1：新增設定檔
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

這個命令會將容器服務代理程式池配置區新增到本機容器服務物件。

## 參數

### -ContainerService
指定此 Cmdlet 新增代理池設定檔的容器服務物件。
若要取得 **ContainerService** 物件，請使用 [AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) Cmdlet。

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Count
指定主機容器的代理數目。
此參數可接受的值為：從1到100的整數。
預設值為1。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsPrefix
指定此 Cmdlet 用來建立此代理池之完整功能變數名稱的 DNS 前置詞。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定代理池設定檔的名稱。
此值在訂閱和資源群組的內容中必須是唯一的。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
指定代理程式的虛擬機器大小。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
這個 Cmdlet 不接受任何輸入。

## 輸出

## 筆記

## 相關連結

[新-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md)

[移除-AzureRmContainerServiceAgentPoolProfile](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
