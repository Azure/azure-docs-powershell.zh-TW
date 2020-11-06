---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: DBB0E08F-63F4-4D61-A69E-3C16A35301EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryPlannedFailoverJob.md
ms.openlocfilehash: e723aacbfbd1b782a91fdc6aa589bfe15df42cff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449495"
---
# Start-AzureRmSiteRecoveryPlannedFailoverJob

## 摘要
啟動網站復原計畫的容錯移轉作業。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByPEObject (預設) 
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-Server <ASRServer>]
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPObject
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPIObject
```
Start-AzureRmSiteRecoveryPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmSiteRecoveryPlannedFailoverJob** Cmdlet 會針對 Azure Site Recovery 保護實體或復原方案啟動計畫的容錯移轉。
您可以使用 Get-AzureRmSiteRecoveryJob Cmdlet 來檢查作業是否成功完成。

## 示例

## 參數

### -CreateVmIfNotFound
此參數可接受的值為：

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

### -ProtectionEntity
指定網站復原保護實體物件。

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPlan
指定復原方案物件。

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -伺服器
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRServer
Parameter Sets: ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicesProvider
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
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

### ASRProtectionEntity
形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值

### ASRRecoveryPlan
形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值

### ASRReplicationProtectedItem
形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值

## 輸出

### ASRJob 中的 SiteRecovery

## 筆記

## 相關連結

