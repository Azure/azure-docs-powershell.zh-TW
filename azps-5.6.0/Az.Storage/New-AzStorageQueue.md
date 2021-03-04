---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 55cee15e3b5327fa0a10def6e2090a77b68b207e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915058"
---
# New-AzStorageQueue

## 簡介
建立儲存佇列。

## 語法

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**New-AzStorageQueue** Cmdlet 在 Azure 中建立儲存佇列。

## 例子

### 範例 1：建立 Azure 儲存佇列
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

此範例會建立名為 queueabc 的儲存佇列。

### 範例 2：建立多個 Azure 儲存佇列
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

此範例會建立多個儲存佇列。
它使用 .NET String 類的 Split 方法，然後傳遞管線上的名稱。

## 參數

### -內容
指定 Azure 儲存內容。
您可以使用 Cmdlet New-AzStorageContext建立。

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

### -名稱
指定佇列的名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext

## 輸出

### Microsoft.WindowsAzure.Commands.Common.storage.ResourceModel.AzureStorageQueue

## 筆記

## 相關連結

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


