---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967029"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## 摘要
下載 XML 格式的 Azure Site Recovery 方案。

## 句法

### ByRPObject (預設) 
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzureSiteRecoveryRecoveryPlanFile** Cmdlet 會以 XML 格式下載 Azure 網站復原方案。
您可以使用此檔案來更新復原方案，然後將它上傳到網站復原伺服器。

針對容錯移轉與復原的目的，復原方案會收集群組中的虛擬機器。

## 示例

### 範例1：取得恢復計畫檔案
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

這個命令會使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet 來取得復原方案，然後將它儲存在 $RecoveryPlan 變數中。

第二個命令使用 **GetAzureSiteRecoveryRecoveryPlanFile** Cmdlet 來取得 $RecoveryPlan 中的網站復原計畫 XML 檔案。
該命令會將 XML 檔案儲存在指定的路徑。

## 參數

### -識別碼
指定要取得的復原方案 ID。

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
指定儲存恢復計畫 XML 檔案的完整路徑。

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

### -RecoveryPlan
指定要取得其恢復計畫的 **ASRRecoveryPlan** 物件。
若要取得 **ASRRecoveryPlan** 物件，請使用 **AzureSiteRecoveryRecoveryPlan** Cmdlet。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


