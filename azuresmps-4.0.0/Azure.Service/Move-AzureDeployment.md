---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967690"
---
# Move-AzureDeployment

## 摘要
在生產與轉移之間的交換部署。

## 句法

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureDeployment** Cmdlet 會交換生產與暫存環境中的部署虛擬 IP 位址。
這個 Cmdlet 會將目前在轉移環境中執行的部署交換到生產環境，以及在生產環境中執行的部署到暫存環境。
如果在暫存環境中有部署且生產環境中沒有部署，則此 Cmdlet 會將部署移至生產環境。
如果在生產環境中有部署，且在轉移環境中沒有部署，則 Cmdlet 會失敗。

## 示例

### 範例1：交換服務的部署
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

這個命令會在生產與轉移環境之間，交換名為 ContosoService 的服務部署。

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

### -ServiceName
指定此 Cmdlet 要調換生產與暫存部署的服務名稱。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### ManagementOperationCoNtext

## 筆記

## 相關連結

[AzureDeployment](./Get-AzureDeployment.md)

[AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[新-AzureDeployment](./New-AzureDeployment.md)

[移除-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


