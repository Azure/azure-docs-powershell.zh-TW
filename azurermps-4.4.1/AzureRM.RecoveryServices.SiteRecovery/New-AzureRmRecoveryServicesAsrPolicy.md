---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448048"
---
# New-AzureRmRecoveryServicesAsrPolicy

## 摘要
建立 Azure Site Recovery 複製原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### EnterpriseToAzure (預設) 
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EnterpriseToEnterprise
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
**新的-AzureRmRecoveryServicesAsrPolicy** Cmdlet 會建立 Azure Site Recovery 複製原則。
複製原則是用來指定複製設定，例如複製頻率和復原點數的數量。

## 示例

### 範例1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

使用指定的參數開始複製原則建立作業，並傳回用來追蹤操作的 ASR 作業。

## 參數

### -ApplicationConsistentSnapshotFrequencyInHours
指定要建立應用程式一致復原點的頻率 (，單位為小時) 。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -驗證
指定所使用的驗證類型。
有效值為：

- 憑證
-  V5

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 壓縮
指定是否應啟用壓縮。

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -加密
指定應該啟用還是停用加密。

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定 ASR 複製原則的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NumberOfRecoveryPointsToRetain
指定要保留的復原點數。

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAzureStorageAccountId
指定複製目標的 Azure 儲存空間帳戶識別碼。 如果您在使用 New-AzureRmRecoveryServicesASRReplicationProtectedItem Cmdlet 啟用複製時未提供備用，就會將它當作複製的目標儲存空間帳戶使用。

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicaDeletion
指定在停用從 VMM 管理的網站到另一個網站的複製時，是否應該刪除複本虛擬機器。

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationFrequencyInSeconds
指定複製頻率間隔（以秒為單位）。
有效值為：

- 為期
- 300
- 900

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationMethod
指定複製方法。
有效值為：

- Online
- 處於

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPort
指定用於複製的埠。

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProvider
指定複製提供者。
有效值為：

- HyperVReplica2012R2
- HyperVReplica2012
- HyperVReplicaAzure

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartTime
指定複製開始時間。
從工作開始，該作業不能遲于24小時。

```yaml
Type: TimeSpan
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

## 輸出

### System.object

## 筆記

## 相關連結

[AzureRmRecoveryServicesAsrPolicy](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[移除-AzureRmRecoveryServicesAsrPolicy](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
