---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452104"
---
# Get-AzureRmRecoveryServicesAsrEvent

## 摘要
取得保存庫中 Azure Site Recovery 事件的詳細資料。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ByParam (預設) 
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByResourceId
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByFabricId
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByName
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
AzureRmRecoveryServicesAsrEvent 會根據指定的選取範圍篩選， **取得** vault 中的事件清單。

## 示例

### 範例1
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

所有事件的清單。

### 範例2
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

依名稱取得事件。

### 範例3
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

受影響物件的事件清單。

### 範例4
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

在時間開始時間與結束時間、嚴重性緊急和健康情況類型 VmHealth 之間的事件清單。

## 參數

### -AffectedObjectFriendlyName
指定搜尋的 AffectedObject FriendlyName。

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
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

### -EndTime
指定搜尋視窗的結束時間。 使用這個參數，只取得在指定的時間之前發生的那些事件。

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -事件
依事件種類篩選事件。

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -結構
依指定結構篩選事件。

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FabricId
指定要篩選的 fabricId。

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要搜尋的事件名稱。

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifes 事件 ReourceId 事件。

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -嚴重度
要篩選的事件嚴重度。

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定搜尋視窗的開始時間。 使用這個參數，只取得在指定時間之後所發生的那些事件。

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### RecoveryServices. SiteRecovery. ASRFabric

## 輸出

### System.object. IEnumerable "1 [ASREvent，RecoveryServices. SiteRecovery，Version = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）

## 筆記

## 相關連結
