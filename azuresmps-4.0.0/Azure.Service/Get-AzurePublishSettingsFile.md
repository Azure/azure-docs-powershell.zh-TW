---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967079"
---
# Get-AzurePublishSettingsFile

## 摘要
下載 Azure 訂閱的發佈設定檔案。

## 句法

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 說明
**AzurePublishSettingsFile** Cmdlet 會在您的帳戶中下載訂閱的發佈設定檔案。
當命令完成時，您可以使用 **PublishSettingsFile** Cmdlet，將檔案中的設定設為可供 Windows PowerShell 使用。

若要讓您的 Azure 帳戶可供 Windows PowerShell 使用，您可以使用發佈設定檔案或 **AzureAccount** Cmdlet。
[發佈設定檔案] 可讓您事先準備會話，讓您能夠以無人參與的方式執行腳本和背景作業。
不過，並非所有的服務都支援發佈設定檔案。
例如， **AzureResourceManager** 模組不支援發佈設定檔案。

當您執行 **AzurePublishSettingsFile** 時，會開啟您的預設瀏覽器，並提示您登入您的 Azure 帳戶、選取訂閱，然後選取發佈設定檔的檔案系統位置。
接著，它會將您訂閱的發佈設定檔案下載到您選取的檔案中。

"發佈設定檔案" 是副檔名為 publishsettings 的 XML 檔案。
檔案包含為您的 Azure 訂閱提供管理認證的編碼證書。

**安全性注意事項：** 發佈設定檔案包含用來管理 Azure 訂閱與服務的認證。
如果惡意使用者存取您的發佈設定檔案，他們就可以編輯、建立及刪除您的 Azure 服務。
為安全性最佳做法，請將檔案儲存到 [下載] 或 [檔] 資料夾中的某個位置，然後在使用匯 **入 AzurePublishSettingsFile** Cmdlet 匯入設定之後刪除該位置。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：下載發佈設定檔
```
PS C:\> Get-AzurePublishSettingsFile
```

這個命令會開啟您的預設瀏覽器、連線到您的 Windows Azure 帳戶，然後下載您帳戶的 publishsettings 檔案。

### 範例2：指定領域
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

這個命令會下載 contoso.com 網域中帳戶的發佈設定檔案。
當您使用組織帳戶（而非 Microsoft 帳戶）登入 Azure 時，請使用帶有 **Realm** 參數的命令。

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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
如果命令成功，則傳回 $True，且 $False 失敗。
根據預設，這個 Cmdlet 不會傳回任何輸出。

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

### -領域
指定組織識別碼中的組織。
例如，如果您登入 [Azure as] admin@contoso.com ，則會 contoso.com [ **Realm** ] 參數的值。
當您使用組織識別碼登入 Azure 入口網站時，請使用此參數。
如果您使用的是 Microsoft 帳戶，例如 outlook.com 或 live.com 帳戶，則不需要此參數。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### None 或 System.object
當您使用 *PassThru* 參數時，這個 Cmdlet 會傳回布林值。
否則，此 Cmdlet 不會傳回任何輸出

## 筆記

## 相關連結

[附加 AzureAccount](./Add-AzureAccount.md)

[匯入-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


