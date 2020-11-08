---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137227"
---
# Set-AzDataLakeGen2ItemAclObject

## 摘要
建立/更新 DataLake gen2 專案 ACL 物件，可在 Update-AzDataLakeGen2Item Cmdlet 中使用。

## 句法

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## 說明
**AzDataLakeGen2ItemAclObject** Cmdlet 會建立/更新 DataLake GEN2 專案 ACL 物件，可在 Update-AzDataLakeGen2Item Cmdlet 中使用。
如果輸入 ACL 中不存在具有相同 AccessControlType/EntityId/DefaultScope 的新 ACL 專案，將會建立新的 ACL 專案，否則就會自動更新現有 ACL 專案的許可權。

## 示例

### 範例1：使用3個 ACL 專案建立 ACL 物件，並更新目錄上的 ACL
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

這個命令會建立含3個 ACL 專案的 ACL 物件 (使用-InputObject 參數，將 acl 專案新增至現有的 ACL 物件) ，並更新目錄上的 ACL。

### 範例2：建立具有4個 ACL 專案的 ACL 物件，以及更新現有 ACL 專案的許可權
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

這個命令會先建立具有4個 ACL 專案的 ACL 物件，然後以不同的許可權再次執行 Cmdlet，但現有 ACL 專案的 AccessControlType/EntityId/DefaultScope 相同。
然後更新 ACL 專案的許可權，但不會新增任何新的 ACL 專案。

## 參數

### -AccessControlType
共有四種類型：「使用者」授與擁有者的許可權，或命名的使用者、「群組」授與擁有權的群組或命名的群組、「遮罩」限制已命名的使用者和群組成員的許可權，而「其他」則授與其他任何專案中都未找到的所有使用者的權利。

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
設定此參數，表示 ACE 屬於目錄的預設 ACL;其他範圍是隱含的，且 ACE 屬於存取 ACL。

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
AccessControlType "mask" 和 "other" 的專案會省略它。
對於擁有者和擁有者群組，也會省略使用者或群組識別碼。

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
如果輸入 PSPathAccessControlEntry \[ \] 物件，會將新的 ACL 新增為輸入 PSPathAccessControlEntry 物件的新元素 \[ \] 。

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
[許可權] 欄位是3個字元的序列，其中第一個字元是 "r" 以准許讀取存取權，第二個字元是 "w" 以授與寫入存取權，而第三個字元是 "x" 來授與執行許可權。
如果沒有授與存取權，則會使用 "-" 字元表示該許可權遭到拒絕。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### WindowsAzure. ResourceModel.. PSPathAccessControlEntry

## 筆記

## 相關連結
