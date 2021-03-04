---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915106"
---
# New-AzStorageAccountSASToken

## 簡介
建立帳戶層級的 SAS 權杖。

## 語法

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzStorageSASToken Cmdlet** 會建立帳戶層級的共用存取簽章 (AZURE) 帳戶的 SAS) 權杖。
您可以使用 SAS 權杖來委派多個服務的許可權，或委派物件層級 SAS 權杖中未提供之服務的許可權。

## 例子

### 範例 1：建立具有完整許可權的帳戶層級 SAS 權杖
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

此命令會建立具有完整許可權的帳戶層級 SAS 權杖。

### 範例 2：為 IP 位址範圍建立帳戶層級的 SAS 權杖
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

此命令會針對來自指定 IP 位址範圍的 HTTPS 要求建立帳戶層級的 SAS 權杖。

## 參數

### -內容
指定 Azure 儲存內容。
您可以使用 New-AzStorageContext Cmdlet 取得 **AzureStorageCoNtext** 物件。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
指定共用存取簽章變成不正確時間。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddressOrRange
指定要接受要求之 IP 位址或 IP 位址範圍，例如 168.1.5.65 或 168.1.5.60-168.1.5.70。
此範圍包含。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -許可權
指定儲存空間帳戶的許可權。
許可權只有在符合指定的資源類型時才能有效。
請注意，這是一個字串，例如用於讀取 (寫入和 `rwd` 刪除) 。
有關可接受的許可權值詳細資訊，請參閱建構帳戶 SAS http://go.microsoft.com/fwlink/?LinkId=799514

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -通訊協定
指定針對帳戶 SAS 要求所允許的通訊協定。
此參數可接受的值為：
- HTTPsOnly
- HTTPsOrHttp 預設值為 HTTPsOrHttp。

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
指定 SAS 權杖中可用的資源類型。
此參數可接受的值為：
- 沒有
- 服務
- 容器
- 物件

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -服務
指定服務。
此參數可接受的值為：
- 沒有
- Blob
- 檔
- 佇列
- 表

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
指定時間 ，做為 **DateTime** 物件，在該物件中，SAS 會變為有效。
若要取得 **DateTime** 物件，請使用 Get-Date Cmdlet。

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### System.String

## 筆記

## 相關連結

[New-AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[New-AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[New-AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[New-AzStorageShareSASToken](./New-AzStorageShareSASToken.md)

[New-AzStorageTableSASToken](./New-AzStorageTableSASToken.md)


