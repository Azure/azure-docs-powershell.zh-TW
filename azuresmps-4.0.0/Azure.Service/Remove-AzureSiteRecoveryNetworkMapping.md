---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967556"
---
# Remove-AzureSiteRecoveryNetworkMapping

## 摘要
從 Site Recovery 保存庫移除網路對應。

## 句法

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureSiteRecoveryNetworkMapping** Cmdlet 會從目前的 Azure Site Recovery 保存庫中移除網路對應。

## 示例

### 範例1：移除網路與恢復網路之間的對應
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

第一個命令 Cmdlet 會使用 **AzureSiteRecoveryServer** Cmdlet，為目前的 Azure Site Recovery 保存庫取得伺服器。
該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。

第二個命令會在主要網路和恢復網路之間取得對應，然後將它儲存在 $NetworkMapping 變數中。
命令會將網路對應的主伺服器指定為 $Servers 的第一個元素。
該命令會將恢復網路的伺服器指定為 $Servers 的第二個元素。

最後一個命令會在 $NetworkMapping 中移除網路對應。

### 範例2：移除網路與 Azure 虛擬機器網路之間的對應
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

第一個命令 Cmdlet 會針對目前的網站復原電子倉庫取得伺服器。
該命令會將網站復原伺服器儲存在 $Servers 陣列變數中。

第二個命令會在主要網路和 Azure 虛擬機器網路之間取得對應，然後將它儲存在 $NetworkMapping 變數中。
該命令會將網路的主要伺服器指定為 $Servers 的第一個元素。
命令會指定 *Azure* 參數。
因此，命令會取得 Azure 虛擬機器網路的對應。

最後一個命令會在 $NetworkMapping 中移除網路對應。

## 參數

### -NetworkMapping
指定要移除的網路對應。

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。
如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
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

## 輸出

## 筆記

## 相關連結

[AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[新-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


