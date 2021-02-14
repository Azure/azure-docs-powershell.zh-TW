---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134639"
---
# Start-AzRecoveryServicesAsrPlannedFailoverJob

## 摘要
啟動計畫的容錯移轉作業。

## 句法

### ByRPIObject (預設) 
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByRPObject
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**AzRecoveryServicesAsrPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 複製受保護的專案或復原方案啟動已規劃的容錯移轉。
您可以使用 Get-AzRecoveryServicesAsrJob Cmdlet 來檢查作業是否成功完成。

## 示例

### 範例1
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

針對指定的 ASR 恢復方案啟動已計畫的容錯移轉，並傳回用來追蹤作業的 ASR 作業。

## 參數

### -CreateVmIfNotFound
如果找不到在備用位置復原中使用的主要區域 (，請建立虛擬機器。 ) 此參數可接受的值為：

- 是的
- 不

```yaml
Type: System.String
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
Type: System.String
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
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

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
Type: System.String
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
當從 Azure 網站完成容錯移轉到需要大量資料同步處理的內部部署網站時，就會套用此參數。
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
Type: System.String
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
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
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
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
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
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
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
顯示在執行 Cmdlet 時會發生什麼情況。 未執行 Cmdlet。

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

### RecoveryServices. SiteRecovery. ASRRecoveryPlan

### RecoveryServices. SiteRecovery. ASRReplicationProtectedItem

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結
