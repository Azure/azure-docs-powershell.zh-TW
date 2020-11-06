---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448032"
---
# Start-AzureRmRecoveryServicesAsrPlannedFailoverJob

## 摘要
啟動計畫的容錯移轉作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByRPIObject (預設) 
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 複製受保護的專案或復原方案啟動已規劃的容錯移轉。
您可以使用 Get-AzureRmRecoveryServicesAsrJob Cmdlet 來檢查作業是否成功完成。

## 示例

### 範例1
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

針對指定的 ASR 恢復方案啟動已計畫的容錯移轉，並傳回用來追蹤作業的 ASR 作業。

## 參數

### -CreateVmIfNotFound
如果找不到在備用位置復原中使用的主要區域 (，請建立虛擬機器。 ) 此參數可接受的值為：

- 是的
- 不

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataEncryptionPrimaryCertFile
指定主要憑證檔案。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataEncryptionSecondaryCertFile
指定次要憑證檔案。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 方向
指定容錯移轉的方向。
此參數可接受的值為：

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -優化
指定要優化的專案。
當從 Azure site 完成容錯移轉到需要大量資料同步處理的內部部署網站時，就會套用此參數。
有效值為：

- ForDowntime
- ForSynchronization

指定 **ForDowntime** 時，這表示資料在進行容錯移轉前已同步處理，以將停機時間降至最低。
不需關閉虛擬機器，就能執行同步處理。
同步處理完成後，作業就會暫停。
繼續工作以執行額外的同步處理操作，以關閉虛擬機器。

指定 **ForSynchronization** 時，這表示資料只會在容錯移轉期間進行同步處理，因此資料同步處理會最小化。
如果啟用此設定，就會立即關閉虛擬機器。
[關閉] 後開始進行同步處理，以完成容錯移轉作業。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPlan
指定對應到復原方案的 ASR 恢復方案物件，以進行容錯移轉。

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
指定對應至要進行容錯移轉之複製受保護專案的 ASR 複製受保護專案物件。

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServicesProvider
透過指定 ASR services 提供者物件（與主機上執行的 ASR 服務提供程式相對應），來識別要在其上建立虛擬機器的主機（在容錯移轉到備用位置時）。 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
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

### RecoveryServices. SiteRecovery. ASRRecoveryPlan
RecoveryServices. SiteRecovery. ASRReplicationProtectedItem

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

