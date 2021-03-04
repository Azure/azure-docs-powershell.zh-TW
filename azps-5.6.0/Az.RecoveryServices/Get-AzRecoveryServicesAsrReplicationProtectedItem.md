---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 66fb9d5ba499a320ba1c4d7bfb44c3fd15f4ecb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915261"
---
# Get-AzRecoveryServicesAsrReplicationProtectedItem

## 簡介
獲得 Azure 網站復原複本受保護的專案的屬性。

## 語法

### ByObject (預設) 
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithName
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByObjectWithWithWithLyName
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByProtectableItemObject
```
Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzRecoveryServicesAsrReplicationProtecedItem** Cmdlet 會從指定的 ASR 保護容器取得所有或指定的 ASR 複製受保護專案的屬性。

## 例子

### 範例 1
```powershell
PS C:\> $ReplicationProtectedItems = Get-AzRecoveryServicesAsrReplicationProtectedItem -ProtectionContainer $PrimaryContainer
```

列出指定 ASR 保護容器中所有複製受保護的專案。

### 範例 2

獲得 Azure 網站復原複本受保護的專案的屬性。  (自動) 

```powershell
<!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesAsrReplicationProtectedItem -FriendlyName XXXXXXXXXX -ProtectionContainer $PrimaryContainer
```

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。


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

### -FriendlyName
指定要取得之複製受保護專案的好用名稱。

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得之複製受保護專案的名稱。

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectableItem
指定 ASR 可保護的專案物件。 如果專案受到保護，Cmdlet 會獲得對應到指定 ASR 可保護專案的 ASR 複製受保護的專案。

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProtectionContainer
指定 ASR 保護容器對應到複製受保護專案的 ASR 保護容器物件。 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem

## 輸出

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## 筆記

## 相關連結

[New-AzRecoveryServicesAsrReplicationProtectedItem](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-AzRecoveryServicesAsrReplicationProtectedItem](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Set-AzRecoveryServicesAsrReplicationProtectedItem](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
