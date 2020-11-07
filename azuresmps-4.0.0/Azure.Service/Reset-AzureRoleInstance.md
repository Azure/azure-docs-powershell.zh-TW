---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966926"
---
# Reset-AzureRoleInstance

## 摘要
要求單一角色實例的重新開機或重新鏡像，或特定角色的所有角色實例。

## 句法

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 說明
**Reset AzureRoleInstance** Cmdlet 會要求重新開機或重新鏡像在部署中執行的角色實例。
此操作會同步執行。
當您重新開機角色實例時，Azure 會將實例設為離線，重新開機該實例的基礎作業系統，然後將該實例傳回線上。
任何寫入本機磁片的資料都會在重新開機後繼續。
任何記憶體中的資料都會遺失。

根據角色類型，對角色實例進行映射，會產生不同的行為。
針對網站或 worker 角色，當角色為 reimaged 時，Azure 會將該角色設為離線，並將 Azure 客體作業系統的全新安裝寫入虛擬機器。
然後，角色就會再次回到線上。
針對 VM 角色，當角色為 reimaged 時，Azure 會將角色設為離線，重新應用您提供給它的自訂影像，然後使角色回到線上。

當角色為 reimaged 時，Azure 會嘗試在任何本機存儲資源中維護資料;不過，如果暫時性的硬體失敗，本機儲存資源可能會遺失。
如果您的應用程式要求資料保持不變，建議寫入持久資料來源（例如 Azure 磁碟機）。
如果角色是 reimaged，則任何寫入本機存儲資源所定義的本地目錄以外的資料都會遺失。

## 示例

### 範例1：重新開機角色實例
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

這個命令會在 MySvc01 服務的暫存部署中重新開機名為 MyWebRole_IN_0 的角色實例。

### 範例2：重新鏡像角色實例
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

這個命令會 reimages MySvc01 雲端服務的過渡部署中的角色實例。

### 範例3：重新鏡像所有角色實例
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

此命令會 reimages MySvc01 服務的生產部署中的所有角色實例。

## 參數

### -InformationAction
指定這個 Cmdlet 回應資訊事件的方式。

此參數可接受的值為：

- 持續
- 理會
- 看
- SilentlyContinue
- 停止
- 封存

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
指定資訊變數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceName
指定要重新映射或重新開機的角色實例名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -重新開機
指定此 Cmdlet 會重新開機指定的角色實例，或者如果沒有指定，則是所有角色實例。
您必須包含 *重新開機* 或重新 *映射* 參數，但不能同時包含兩者。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -重新映射
指定此 Cmdlet 會 reimages 指定的角色實例，或者如果沒有指定，則是所有角色實例。
您必須包含 *重新開機* 或重新 *映射* 參數，但不能同時包含兩者。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
指定服務的名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -槽
指定角色實例執行所在的部署環境。
有效值為： [生產] 和 [轉移]。
您可以包含 *DeploymentName* 或 *槽* 參數，但不能同時包含兩者。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

## 筆記

## 相關連結

[Set-AzureRole](./Set-AzureRole.md)


