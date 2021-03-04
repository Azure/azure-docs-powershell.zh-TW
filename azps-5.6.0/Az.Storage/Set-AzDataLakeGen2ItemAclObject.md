---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910345"
---
# Set-AzDataLakeGen2ItemAclObject

## 簡介
建立/更新 DataLake 第 2 代專案 ACL 物件，可用於 Update-AzDataLakeGen2Item Cmdlet。

## 語法

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## 描述
**Set-AzDataLakeGen2ItemAclObject** Cmdlet 會建立/更新 DataLake 第 2 代專案 ACL 物件，可用於 Update-AzDataLakeGen2Item Cmdlet。
如果輸入 ACL 中不存在具有相同 AccessControlType/EntityId/DefaultScope 的新 ACL 專案，將會建立一個新的 ACL 專案，否則會更新現有 ACL 專案的許可權。

## 例子

### 範例 1：建立包含 3 ACL 專案之 ACL 物件，並更新目錄中的 ACL
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

此命令會建立一個包含 3 個 ACL 專案之 ACL 物件 (使用 -InputObject 參數將 acl 專案新增到現有的 acl 物件) ，並更新目錄中的 ACL。

### 範例 2：建立包含 4 個 ACL 專案之 ACL 物件，以及更新現有 ACL 專案的許可權
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

此命令會先建立包含 4 個 ACL 專案之 ACL 物件，然後再次以不同的許可權執行 Cmdlet，但現有的 ACL 專案則使用相同的 AccessControlType/EntityId/DefaultScope。
然後會更新 ACL 專案的許可權，但不會新增任何 ACL 專案。

## 參數

### -AccessControlType
有四種類型：「使用者」會授予擁有者或已命名使用者的許可權、「群組」會授予擁有權群組或已命名群組的許可權、「遮罩」會限制授予已命名使用者和群組成員的許可權，而「其他」則授予在任何其他專案內找不到的所有使用者許可權。

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
設定此參數以表示 ACE 屬於目錄的預設 ACL;否則為隱含範圍，且 ACE 屬於存取 ACL。

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

### -EntityId
使用者或群組識別碼。
在 AccessControlType 專案 "mask" 和 "other" 中省略此名稱。
擁有者和擁有群組的使用者或群組識別碼也會省略。

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

### -InputObject
如果輸入 PSPathAccessControlEntry 物件，將會將新的 ACL 新增為 \[ \] 輸入 PSPathAccessControlEntry 物件 \[ \] 的新元素。

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -許可權
許可權欄位是一個 3 個字元的順序，其中第一個字元是'r'以授予讀取存取權，第二個字元是 'w' 以授予寫入存取權，第三個字元是 'x' 以授予執行許可權。
如果未授予存取權，會使用 '-' 字元來表示許可權遭到拒絕。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
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

### Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSPathAccessControlEntry

## 筆記

## 相關連結
