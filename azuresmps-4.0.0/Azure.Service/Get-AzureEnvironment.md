---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967798"
---
# Get-AzureEnvironment

## 摘要
取得 Azure 環境

## 句法

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureEnvironment** Cmdlet 會取得適用于 Windows PowerShell 的 Azure 環境。

Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。
您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。
如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。

**AzureEnvironment** Cmdlet 會從您的訂閱資料檔案（而不是從 Azure）取得環境。
如果訂閱資料檔案已過時，請執行 **AzureAccount** 或 **Import PublishSettingsFile** Cmdlet 來重新整理。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：取得所有環境
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

這個命令會取得可供 Windows PowerShell 使用的所有環境。

### 範例2：依名稱取得環境
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

這個範例會取得 AzureCloud 環境。

### 範例3：取得所有環境的所有屬性
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

這個命令會取得所有環境的所有屬性。

此命令使用 **AzureEnvironment** Cmdlet 來取得此帳戶的所有 Azure 環境。
接著，它會使用 **Foreach 物件** Cmdlet 來執行 **AzureEnvironment** 命令，並在每個環境中使用 **Name** 參數。
**Name** 參數的值是每個環境的 **EnvironmentName** 屬性。

如果沒有參數， **AzureEnvironment** 只會取得環境的選取屬性。

## 參數

### -名稱
僅取得指定的環境。
輸入環境名稱。
參數值區分大小寫。
不允許通配字元。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有
您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。

## 輸出

### PSCustomObject 的系統管理功能
根據預設， **AzureEnvironment** 會傳回自訂物件。

### WindowsAzure. 常見. WindowsAzureEnvironment
當您使用 **Name** 參數執行 **AzureEnvironment** 時，它會傳回 **WindowsAzureEnvironment** 物件。

## 筆記

## 相關連結

[附加 AzureAccount](./Add-AzureAccount.md)

[附加 AzureEnvironment](./Add-AzureEnvironment.md)

[AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[匯入-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[移除-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


