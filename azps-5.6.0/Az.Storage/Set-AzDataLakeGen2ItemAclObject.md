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
# <span data-ttu-id="4bb1b-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="4bb1b-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="4bb1b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4bb1b-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb1b-103">建立/更新 DataLake 第 2 代專案 ACL 物件，可用於 Update-AzDataLakeGen2Item Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="4bb1b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4bb1b-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="4bb1b-105">描述</span><span class="sxs-lookup"><span data-stu-id="4bb1b-105">DESCRIPTION</span></span>
<span data-ttu-id="4bb1b-106">**Set-AzDataLakeGen2ItemAclObject** Cmdlet 會建立/更新 DataLake 第 2 代專案 ACL 物件，可用於 Update-AzDataLakeGen2Item Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="4bb1b-107">如果輸入 ACL 中不存在具有相同 AccessControlType/EntityId/DefaultScope 的新 ACL 專案，將會建立一個新的 ACL 專案，否則會更新現有 ACL 專案的許可權。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="4bb1b-108">例子</span><span class="sxs-lookup"><span data-stu-id="4bb1b-108">EXAMPLES</span></span>

### <span data-ttu-id="4bb1b-109">範例 1：建立包含 3 ACL 專案之 ACL 物件，並更新目錄中的 ACL</span><span class="sxs-lookup"><span data-stu-id="4bb1b-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="4bb1b-110">此命令會建立一個包含 3 個 ACL 專案之 ACL 物件 (使用 -InputObject 參數將 acl 專案新增到現有的 acl 物件) ，並更新目錄中的 ACL。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="4bb1b-111">範例 2：建立包含 4 個 ACL 專案之 ACL 物件，以及更新現有 ACL 專案的許可權</span><span class="sxs-lookup"><span data-stu-id="4bb1b-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="4bb1b-112">此命令會先建立包含 4 個 ACL 專案之 ACL 物件，然後再次以不同的許可權執行 Cmdlet，但現有的 ACL 專案則使用相同的 AccessControlType/EntityId/DefaultScope。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="4bb1b-113">然後會更新 ACL 專案的許可權，但不會新增任何 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="4bb1b-114">參數</span><span class="sxs-lookup"><span data-stu-id="4bb1b-114">PARAMETERS</span></span>

### <span data-ttu-id="4bb1b-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="4bb1b-115">-AccessControlType</span></span>
<span data-ttu-id="4bb1b-116">有四種類型：「使用者」會授予擁有者或已命名使用者的許可權、「群組」會授予擁有權群組或已命名群組的許可權、「遮罩」會限制授予已命名使用者和群組成員的許可權，而「其他」則授予在任何其他專案內找不到的所有使用者許可權。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="4bb1b-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="4bb1b-117">-DefaultScope</span></span>
<span data-ttu-id="4bb1b-118">設定此參數以表示 ACE 屬於目錄的預設 ACL;否則為隱含範圍，且 ACE 屬於存取 ACL。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="4bb1b-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="4bb1b-119">-EntityId</span></span>
<span data-ttu-id="4bb1b-120">使用者或群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-120">The user or group identifier.</span></span>
<span data-ttu-id="4bb1b-121">在 AccessControlType 專案 "mask" 和 "other" 中省略此名稱。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="4bb1b-122">擁有者和擁有群組的使用者或群組識別碼也會省略。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="4bb1b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bb1b-123">-InputObject</span></span>
<span data-ttu-id="4bb1b-124">如果輸入 PSPathAccessControlEntry 物件，將會將新的 ACL 新增為 \[ \] 輸入 PSPathAccessControlEntry 物件 \[ \] 的新元素。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="4bb1b-125">-許可權</span><span class="sxs-lookup"><span data-stu-id="4bb1b-125">-Permission</span></span>
<span data-ttu-id="4bb1b-126">許可權欄位是一個 3 個字元的順序，其中第一個字元是'r'以授予讀取存取權，第二個字元是 'w' 以授予寫入存取權，第三個字元是 'x' 以授予執行許可權。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="4bb1b-127">如果未授予存取權，會使用 '-' 字元來表示許可權遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="4bb1b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb1b-128">CommonParameters</span></span>
<span data-ttu-id="4bb1b-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb1b-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4bb1b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb1b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4bb1b-131">INPUTS</span></span>

### <span data-ttu-id="4bb1b-132">沒有</span><span class="sxs-lookup"><span data-stu-id="4bb1b-132">None</span></span>

## <span data-ttu-id="4bb1b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4bb1b-133">OUTPUTS</span></span>

### <span data-ttu-id="4bb1b-134">Microsoft.WindowsAzure.Commands.storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="4bb1b-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="4bb1b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4bb1b-135">NOTES</span></span>

## <span data-ttu-id="4bb1b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bb1b-136">RELATED LINKS</span></span>
