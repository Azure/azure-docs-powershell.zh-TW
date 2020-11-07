---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967329"
---
# Publish-AzureServiceProject

## 摘要
將目前的服務發佈到 Windows Azure。

## 句法

### PublishFromServiceDefinition (預設) 
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

**AzureServiceProject** Cmdlet 會將目前的服務發佈到雲端。
您可以在命令列上指定發佈設定 (例如 **訂閱** 、 **StorageAccountName** 、 **位置** 、 **槽** ) ，或透過 **AzureServiceProject** Cmdlet 在本機設定中指定。

## 示例

### 範例1：發佈含預設值的服務專案
```
PS C:\> Publish-AzureServiceProject
```

這個範例會使用目前的服務設定和目前的 Azure 發佈設定檔，發佈目前的服務。

### 範例2：建立部署套件
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

這個範例會在 service 目錄中建立部署套件 () 檔案，但不會發佈到 Windows Azure。

## 參數

### -AffinityGroup
指定您希望服務使用的地緣群組。

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -配置
指定服務設定檔。
如果您指定此參數，請指定 *Package* 參數。

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentName
指定部署名稱。

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -啟動
開啟瀏覽器視窗，讓您在部署之後就能查看應用程式。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
將託管應用程式的地區。
可能的值包括： 
  
- 亞洲任何地方
- 歐洲任何地方
- 美國任何地方
- 東亞
- 東美國
- 美國中北部
- 北歐
- 美國中南部
- 東南亞
- 西歐
- 美國西部
 
如果未指定位置，則會使用在最後一次呼叫 **AzureServiceProject** 中指定的位置。 如果未指定位置，位置將會從「中北部」和「中南部 US」位置隨機選取。

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -套件
指定要部署的套件檔案。
指定副檔名為 cspkg 的本機檔案，或是包含該套件之 blob 的 URI。
如果您指定此參數，請勿指定 *ServiceName* 參數。

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
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

### -ServiceName
指定發佈至 Windows Azure 時要用於服務的名稱。
名稱會判斷 cloudapp.net 子域中的部分標籤，用來在 Windows (Azure 中託管（cloudapp.net **) ）時** 用來處理服務。
發佈服務時指定的任何名稱會覆寫建立服務時所提供的名稱。
 (查看 **新的 AzureServiceProject** Cmdlet) 。

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -槽
要用於此服務的部署槽位。
可能的值為「分段」和「生產」。
如果未指定任何槽，則會使用在最後一個 Set-AzureDeploymentSlot 呼叫中提供的槽。
如果沒有指定任何槽，則會使用「生產」槽。

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
指定發佈服務時要使用的 Windows Azure 儲存空間帳戶名稱。
在發行服務之前，不會使用這個值。
如果未指定此參數，則會從最後一個 [ **設定 AzureServiceProject** ] 命令取得值。
如果您從未指定過儲存空間，就會使用符合服務名稱的儲存空間帳戶。
如果不存在這樣的儲存帳戶，此 Cmdlet 會嘗試建立新帳戶。
不過，如果在其他訂閱中存在與服務名稱相符的儲存空間帳戶，嘗試可能會失敗。

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
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

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


