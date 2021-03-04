---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: 0f74ad9b146a0c5d2f2c65b7109fb57f56902834
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915102"
---
# New-AzStorageBlobRangeToRestore

## 簡介
建立 Blob 範圍物件以還原儲存空間帳戶。

## 語法

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**New-AzStorageBlobRangeToRestore** Cmdlet 會建立 Blob 範圍物件，可用於 Restore-AzStorageBlobRange。

## 例子

### 範例 1：建立 Blob 範圍以還原
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

此命令會建立要還原的 blob 範圍，從 container1/blob1 開始， (包含) ，結尾是 container2/blob2 (排除) 。

### 範例 2：建立 Blob 範圍，以字母順序從第一個 Blob 還原到特定的 blob， (排除) 
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

此命令會建立 Blob 範圍，從第一個按字母順序的 Blob 還原到特定的 Blob 容器2/blob2， (排除) 

### 範例 3：建立 Blob 範圍，該範圍會從特定的 blob (包含) ，還原到最後一個 blob，並按字母順序
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

此命令會建立 Blob 範圍，從特定的 Blob 容器1/blob1 (包含) ，以字母順序還原到最後一個 Blob。

### 範例 4：建立 Blob 範圍以還原所有 Blob
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

此命令會建立一個 Blob 範圍，可還原所有 Blob。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndRange
指定 Blob 還原結束範圍。
還原 Blob 中會排除結束範圍。
將其設定為空白字串以還原到結尾。

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

### -StartRange
指定 Blob 還原開始範圍。
還原 Blob 中會包含開始範圍。
將其設定為空白字串，以從頭開始還原。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### 沒有

## 輸出

### Microsoft.Azure.Commands.management.storage.models.PSBlobRestoreRange

## 筆記

## 相關連結
