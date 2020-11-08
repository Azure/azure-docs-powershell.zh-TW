---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137791"
---
# Get-AzStorageQueue

## 摘要
列出 [儲存佇列]。

## 句法

### QueueName (預設) 
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzStorageQueue** Cmdlet 會列出與 Azure 儲存空間帳戶相關聯的儲存佇列。

## 示例

### 範例1：列出所有 Azure 儲存空間佇列
```
PS C:\>Get-AzStorageQueue
```

這個命令會取得目前儲存空間帳戶的所有儲存佇列清單。

### 範例2：使用萬用字元列出 Azure 儲存空間佇列
```
PS C:\>Get-AzStorageQueue -Name queue*
```

這個命令使用萬用字元來取得名稱以 queue 開頭的儲存佇列清單。

### 範例3：使用佇列名稱首碼列出 Azure 儲存空間佇列
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

這個範例使用 *Prefix* 參數來取得名稱以 queue 開頭的儲存佇列清單。

## 參數

### -內容
指定 Azure 儲存區內容。
您可以使用 **新的 AzStorageCoNtext** Cmdlet 來建立它。

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
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -名稱
指定名稱。
如果沒有指定名稱，則 Cmdlet 會取得所有佇列的清單。
如果指定完整或部分名稱，則 Cmdlet 會取得符合名稱模式的所有佇列。

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
指定要取得的佇列名稱中所用的首碼。

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### IStorageCoNtext 中的 [Common.]

## 輸出

### AzureStorageQueue WindowsAzure. ResourceModel。

## 筆記

## 相關連結

[新-AzStorageQueue](./New-AzStorageQueue.md)

[移除-AzStorageQueue](./Remove-AzStorageQueue.md)


