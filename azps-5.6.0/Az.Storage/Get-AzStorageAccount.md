---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2c8980f198dc675e12a9b9c6048a4960c1998f9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915157"
---
# Get-AzStorageAccount

## 簡介
獲得儲存空間帳戶。

## 語法

### ResourceGroupParameterSet
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### AccountNameParameterSet
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### BlobRestoreStatusParameterSet
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzStorageAccount** Cmdlet 會取得指定的儲存空間帳戶，或資源群組或訂閱中所有的儲存空間帳戶。

## 例子

### 範例 1：取得指定的儲存空間帳戶
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

此命令會獲得指定的儲存空間帳戶。

### 範例 2：取得資源群組中所有的儲存空間帳戶
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

此命令會獲得資源群組中所有的儲存空間帳戶。

### 範例 3：取得訂閱中所有的儲存空間帳戶
```
PS C:\>Get-AzStorageAccount
```

此命令會獲得訂閱中所有的儲存空間帳戶。

### 範例 4：取得儲存空間帳戶及其 Blob 還原狀態
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

此命令會獲得具有 Blob 還原狀態的儲存空間帳戶，並且顯示 Blob 還原狀態。

## 參數

### -AsJob
在背景中執行 Cmdlet

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -IncludeBlobRestoreStatus
取得儲存空間帳戶的 BlobRestoreStatus。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeGeoReplicationStats
取得儲存空間帳戶的 GeoReplicationStats。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得的儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含要取得儲存空間帳戶的資源組名。

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.management.storage.models.PSStorageAccount

## 筆記

## 相關連結

[New-AzStorageAccount](./New-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)


