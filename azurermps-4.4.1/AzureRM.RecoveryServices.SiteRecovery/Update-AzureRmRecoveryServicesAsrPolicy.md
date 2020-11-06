---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453319"
---
# Update-AzureRmRecoveryServicesAsrPolicy

## 摘要
更新 Azure 網站恢復複製原則。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrPolicy** Cmdlet 會更新指定的 Azure Site Recovery 複製原則。

## 示例

### 範例1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

使用指定的參數啟動更新複製原則作業，並傳回用於追蹤作業的 ASR 作業。

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
Parameter Sets: (All)
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
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Cmdlet 的輸入物件：指定對應到要更新之複製原則的 ASR 複製原則物件。

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Parameter Sets: (All)
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
Parameter Sets: (All)
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

Required: False
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
Parameter Sets: (All)
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
Parameter Sets: (All)
Aliases: 

Required: False
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

### RecoveryServices. SiteRecovery. ASRPolicy

## 輸出

### System.object

## 筆記

## 相關連結

