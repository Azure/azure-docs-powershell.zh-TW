---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967707"
---
# Import-AzurePublishSettingsFile

## 摘要
匯入可讓您在 Windows PowerShell 中管理 Azure 帳戶的發佈設定檔。

## 句法

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
匯 **入-AzurePublishSettingsFile** Cmdlet 會 ( *. publishsettings) 中匯入發佈設定檔案，其中包含 Azure 帳戶的相關資訊，並將訂閱資料檔案儲存在您的電腦上。
當 Cmdlet 完成時，您可以在 Windows PowerShell 中管理 Azure 帳戶。

在執行匯 **入-AzurePublishSettingsFile** 之前，請執行 **AzurePublishSettingsFile** ，這會下載並儲存發佈設定檔案，以便您匯入。

若要讓您的 Azure 帳戶可供 Windows PowerShell 使用，您可以使用發佈設定檔案或 **AzureAccount** Cmdlet。
[發佈設定檔案] 可讓您事先準備會話，讓您能夠以無人參與的方式執行腳本和背景作業。
不過，並非所有的服務都支援發佈設定檔案。
例如， **AzureResourceManager** 模組不支援發佈設定檔案。

**安全性注意事項：** 發佈設定檔案包含已編碼但未加密的管理憑證。
如果惡意使用者存取您的發佈設定檔案，他們可能可以編輯、建立及刪除您的 Azure 服務。
為安全性最佳做法，請將檔案儲存到 [下載] 或 [檔] 資料夾中的某個位置，然後在使用匯 **入 AzurePublishSettingsFile** Cmdlet 匯入設定之後刪除該位置。

## 示例

### 範例1：匯入檔案
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

這個命令會將 [C:\Temp\MyAccount.publishsettings] 檔案匯入。

## 參數

### -環境
指定 Azure 環境。

Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。
您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。
如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。

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

### -設定檔
指定此 Cmdlet 讀取的 Azure 設定檔。 如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。

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

### -PublishSettingsFile
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

### 所有
您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。

## 輸出

### 所有
這個 Cmdlet 不會產生任何輸出。

## 筆記
* "發佈設定檔案" 是副檔名為 publishsettings 的 XML 檔案。 檔案包含為您的 Azure 訂閱提供管理認證的編碼證書。 匯入此檔案之後，請將其刪除以避免安全性風險。
* 「訂閱資料檔」是可在您的電腦上安全儲存的 XML 檔案。 根據預設，它會儲存在您的漫遊使用者設定檔中 ($home/AppData/Roaming) ]。

## 相關連結

[如何安裝和設定 Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[附加 AzureAccount](./Add-AzureAccount.md)

[AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


