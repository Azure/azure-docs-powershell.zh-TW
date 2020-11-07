---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967720"
---
# Get-AzureWebsite

## 摘要
取得目前訂閱中的 Azure 網站。

## 句法

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 說明
**AzureWebsite** Cmdlet 會取得目前訂閱中 Azure 網站的相關資訊。

根據預設， **AzureWebsite** 會取得目前訂閱中的所有 Azure 網站，並傳回提供網站基本資訊的物件。
當您使用 *Name* 參數時， **AzureWebsite** 會傳回包含大量資訊的物件，包括設定詳細資料。

目前的訂閱是指派為「目前」的訂閱。 若要尋找目前的訂閱，請使用 [AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) Cmdlet 的 *目前* 參數。
若要變更目前的訂閱，請使用 [AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) Cmdlet。

本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。
若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。

## 示例

### 範例1：取得訂閱中的所有網站
```
PS C:\> Get-AzureWebsite
```

這個命令會取得目前訂閱中的所有 Azure 網站。

### 範例2：依名稱取得網站
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

這個命令會取得 ContosoWeb Azure 網站的詳細資訊，包括設定資訊。
當您使用 *Name* 參數時， **AzureWebsite** 會傳回含有網站延伸資訊的 **SiteWithConfig** 物件。

### 範例3：取得所有網站的詳細資訊
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

這個命令會取得訂閱中所有網站的詳細資訊。
它會使用 **AzureWebsite** 命令來取得所有網站，然後使用 **ForEach 物件** Cmdlet，透過名稱取得每個網站。

### 範例4：取得有關部署槽的資訊
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

這個命令會取得 ContosoWeb 網站的暫存部署槽。
部署槽可讓您測試 Azure 網站的不同版本，而不需將其釋放到公用。

### 範例5：取得網站實例
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

這個範例中的命令使用 Azure 網站的實例屬性來取得目前執行的網站實例的相關資訊。
[ **範例** ] 屬性已新增至 Azure 模組版本0.8.3 中的 **SiteWithConfig** 物件。

第一個命令會取得網站所有目前執行實例的實例識別碼。
第二個命令會取得網站執行中的實例數。
您可以在任何陣列中使用 **Count** 屬性。

## 參數

### -名稱
取得指定網站的詳細配置資訊。
輸入訂閱中某個網站的名稱。
根據預設， **AzureWebsite 會取得** 目前訂閱中的所有網站。
[ *Name* ] （名稱）值不支援萬用字元字元。

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

### -槽
取得網站的指定部署槽。
輸入插槽名稱，例如「分段」或「生產」。
如需部署槽的詳細資訊，請參閱 Microsoft Azure 網站上的分段部署 https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ 。
若要將部署槽新增至現有的 Azure 網站，請使用 Set-AzureWebsite Cmdlet。

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

### WindowsAzure. WebEntities. Site （公用網站）
根據預設， **AzureWebsite** 會傳回 **網站** 物件的陣列。

### WindowsAzure. WebEntities. SiteWithConfig （）
當您使用 *Name* 參數時， **AzureWebsite** 會傳回 **SiteWithConfig** 物件。

## 筆記

## 相關連結

[新-AzureWebsite](./New-AzureWebsite.md)

[移除-AzureWebsite](./Remove-AzureWebsite.md)

[開始-AzureWebsite](./Start-AzureWebsite.md)

[停止 AzureWebsite](./Stop-AzureWebsite.md)

[顯示-AzureWebsite](./Show-AzureWebsite.md)


