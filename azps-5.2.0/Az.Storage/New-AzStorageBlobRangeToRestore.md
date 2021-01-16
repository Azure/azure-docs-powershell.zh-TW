---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobrangetorestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobRangeToRestore.md
ms.openlocfilehash: cfbe2cc695ceb2db7c498e8ee2750fa0427da114
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98273727"
---
# New-AzStorageBlobRangeToRestore

## 摘要
建立 [Blob 範圍] 物件來還原儲存空間帳戶。

## 句法

```
New-AzStorageBlobRangeToRestore [-StartRange <String>] [-EndRange <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzStorageBlobRangeToRestore** Cmdlet 會建立可在 Restore-AzStorageBlobRange 中使用的 Blob 範圍物件。

## 示例

### 範例1：建立要還原的 blob 範圍
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
```

這個命令會建立一個要還原的 blob 範圍，這會從 container1/blob1 (包含) ，而結束于 container2/blob2 (排除) ]。

### 範例2：建立一個 blob 範圍，該範圍會從第一個 blob 依字母順序還原至特定的 blob (排除) 
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange container2/blob2
```

這個命令會建立一個 blob 範圍，該範圍會從字母順序的第一個 blob 還原到特定的 blob container2/blob2 (排除) 

### 範例3：建立將從特定的 blob （依字母順序）到最後一個 blob (包含) 的 blob 範圍
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange ""
```

這個命令會建立從特定的 blob container1/blob1 中還原的 blob 範圍， (包含) ，以字母順序排列到最後一個 blob。

### 範例4：建立將還原所有 blob 的 blob 範圍
```powershell
PS C:\> $range = New-AzStorageBlobRangeToRestore -StartRange "" -EndRange ""
```

這個命令會建立一個將還原所有 blob 的 blob 範圍。

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
指定 [blob 還原] 結束範圍。
[結束範圍] 會在還原 blob 中排除。
將它設為空白 strng，以還原到結尾。

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
指定 [blob 還原起始範圍]。
開始範圍將包含在還原 blob 中。
將它設為空白字串，即可從頭開始還原。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSBlobRestoreRange 中的 [管理]。

## 筆記

## 相關連結
