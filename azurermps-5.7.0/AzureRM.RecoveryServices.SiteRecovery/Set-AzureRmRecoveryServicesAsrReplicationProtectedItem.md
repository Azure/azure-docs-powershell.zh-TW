---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: a3ae73e9831202418d35481270a1d04b1cb09a59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448601"
---
# Set-AzureRmRecoveryServicesAsrReplicationProtectedItem

## 摘要
針對指定的複製受保護專案設定恢復屬性，例如目標網路和虛擬機器大小。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-UseManagedDisk <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 說明
**AzureRmRecoveryServicesAsrReplicationProtectedItem** Cmdlet 會為複製受保護的專案設定復原屬性。

## 示例

### 範例1
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -PrimaryNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

啟動使用指定參數來更新禁止複製專案設定的作業，並傳回用於追蹤作業的 ASR 作業。

## 參數

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

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。
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

### -InputObject
Cmdlet 的輸入物件：與要更新之受複製受保護的專案對應的 ASR 複製受保護專案物件。

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LicenseType
指定要用於 Windows Server 虛擬機器的授權類型選取專案。 如果您有資格使用 Azure 混合式使用優惠 (中樞) 進行遷移，且想要指定在容錯移轉此受保護的專案時使用中樞設定，請將 [授權類型] 設定為 [WindowsServer]。

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定將在容錯移轉時建立的恢復虛擬機器的名稱。

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

### -NicSelectionType
指定 (NIC 的網路介面卡，) 由使用者設定的屬性或依預設設定的內容。
您可以指定 NotSelected，以回到預設值。

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNic
指定此 Cmdlet 設定 [復原網路] 屬性的虛擬機器 NIC。

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

### -RecoveryAvailabilitySet
容錯移轉之後，已針對複製受保護的專案進行可用性設定。

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

### -RecoveryCloudServiceId
要將此虛擬機器容錯移轉至其中的復原雲端服務的資源識別碼。

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

### -RecoveryNetworkId
指定受保護專案應針對其進行容錯移轉之 Azure 虛擬網路的識別碼。

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

### -RecoveryNicStaticIPAddress
指定在恢復時應該指派給主要 NIC 的靜態 IP 位址。

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

### -RecoveryNicSubnetName
指定要在容錯移轉時，將受保護之專案的這個 NIC 連線至之 [復原] Azure 虛擬網路上的子網名稱。

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

### -RecoveryResourceGroupId
修復區域中的 Azure 資源群組的識別碼，受保護的專案將會在容錯移轉時復原。

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

### -大小
指定復原虛擬電腦大小。
此值應該是由 Azure 虛擬機器支援的大小集合所組成。

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

### -UseManagedDisk
指定在容錯移轉中建立的 Azure 虛擬機器是否應使用受管理的磁片。

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

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

### RecoveryServices. SiteRecovery. ASRReplicationProtectedItem

## 輸出

### RecoveryServices. SiteRecovery. ASRJob

## 筆記

## 相關連結

[AzureRmRecoveryServicesAsrReplicationProtectedItem](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[新-AzureRmRecoveryServicesAsrReplicationProtectedItem](./New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[移除-AzureRmRecoveryServicesAsrReplicationProtectedItem](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
