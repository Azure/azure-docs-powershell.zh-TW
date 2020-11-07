---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966995"
---
# Get-AzureStorageAccount

## 摘要
取得目前 Azure 訂閱的儲存空間帳戶。

## 句法

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 說明
**AzureStorageAccount** Cmdlet 會傳回一個物件，其中包含目前訂閱之儲存空間帳戶的相關資訊。
如果指定了 *StorageAccountName* 參數，則只會傳回指定儲存空間帳戶的相關資訊。

## 示例

### 範例1：返回所有儲存空間帳戶
```
PS C:\> Get-AzureStorageAccount
```

這個命令會傳回與目前訂閱相關聯之所有儲存空間帳戶的物件。

### 範例2：返回指定帳戶的帳戶資訊
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

這個命令會傳回只有 ContosoStore01 帳戶資訊的物件。

### 範例3：顯示儲存空間帳戶資料表
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

這個命令會傳回與目前訂閱相關的所有儲存空間帳戶的物件，並將其輸出為顯示帳戶名稱、帳戶標籤和儲存位置的表格。

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

### -StorageAccountName
指定儲存空間帳戶的名稱。
如果已指定，這個 Cmdlet 只會傳回指定的儲存空間帳戶物件。

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
* 輸入 `help node-dev` 以取得 Node.js 與開發相關的 Cmdlet 的說明。 輸入 `help php-dev` 以取得有關 PHP 開發相關 Cmdlet 的說明。

## 相關連結

[新-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


