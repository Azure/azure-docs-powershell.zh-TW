---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957169"
---
# <span data-ttu-id="bf198-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="bf198-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="bf198-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf198-102">SYNOPSIS</span></span>
<span data-ttu-id="bf198-103">建立/更新 DataLake gen2 專案 ACL 物件，可在 Update-AzDataLakeGen2Item Cmdlet 中使用。</span><span class="sxs-lookup"><span data-stu-id="bf198-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="bf198-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf198-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="bf198-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf198-105">DESCRIPTION</span></span>
<span data-ttu-id="bf198-106">**AzDataLakeGen2ItemAclObject** Cmdlet 會建立/更新 DataLake GEN2 專案 ACL 物件，可在 Update-AzDataLakeGen2Item Cmdlet 中使用。</span><span class="sxs-lookup"><span data-stu-id="bf198-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="bf198-107">如果輸入 ACL 中不存在具有相同 AccessControlType/EntityId/DefaultScope 的新 ACL 專案，將會建立新的 ACL 專案，否則就會自動更新現有 ACL 專案的許可權。</span><span class="sxs-lookup"><span data-stu-id="bf198-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="bf198-108">示例</span><span class="sxs-lookup"><span data-stu-id="bf198-108">EXAMPLES</span></span>

### <span data-ttu-id="bf198-109">範例1：使用3個 ACL 專案建立 ACL 物件，並更新目錄上的 ACL</span><span class="sxs-lookup"><span data-stu-id="bf198-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="bf198-110">這個命令會建立含3個 ACL 專案的 ACL 物件 (使用-InputObject 參數，將 acl 專案新增至現有的 ACL 物件) ，並更新目錄上的 ACL。</span><span class="sxs-lookup"><span data-stu-id="bf198-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="bf198-111">範例2：建立具有4個 ACL 專案的 ACL 物件，以及更新現有 ACL 專案的許可權</span><span class="sxs-lookup"><span data-stu-id="bf198-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="bf198-112">這個命令會先建立具有4個 ACL 專案的 ACL 物件，然後以不同的許可權再次執行 Cmdlet，但現有 ACL 專案的 AccessControlType/EntityId/DefaultScope 相同。</span><span class="sxs-lookup"><span data-stu-id="bf198-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="bf198-113">然後更新 ACL 專案的許可權，但不會新增任何新的 ACL 專案。</span><span class="sxs-lookup"><span data-stu-id="bf198-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="bf198-114">參數</span><span class="sxs-lookup"><span data-stu-id="bf198-114">PARAMETERS</span></span>

### <span data-ttu-id="bf198-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="bf198-115">-AccessControlType</span></span>
<span data-ttu-id="bf198-116">共有四種類型：「使用者」授與擁有者的許可權，或命名的使用者、「群組」授與擁有權的群組或命名的群組、「遮罩」限制已命名的使用者和群組成員的許可權，而「其他」則授與其他任何專案中都未找到的所有使用者的權利。</span><span class="sxs-lookup"><span data-stu-id="bf198-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="bf198-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="bf198-117">-DefaultScope</span></span>
<span data-ttu-id="bf198-118">設定此參數，表示 ACE 屬於目錄的預設 ACL;其他範圍是隱含的，且 ACE 屬於存取 ACL。</span><span class="sxs-lookup"><span data-stu-id="bf198-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="bf198-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="bf198-119">-EntityId</span></span>
<span data-ttu-id="bf198-120">使用者或群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf198-120">The user or group identifier.</span></span>
<span data-ttu-id="bf198-121">AccessControlType "mask" 和 "other" 的專案會省略它。</span><span class="sxs-lookup"><span data-stu-id="bf198-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="bf198-122">對於擁有者和擁有者群組，也會省略使用者或群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf198-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="bf198-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf198-123">-InputObject</span></span>
<span data-ttu-id="bf198-124">如果輸入 PSPathAccessControlEntry \[ \] 物件，會將新的 ACL 新增為輸入 PSPathAccessControlEntry 物件的新元素 \[ \] 。</span><span class="sxs-lookup"><span data-stu-id="bf198-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="bf198-125">-許可權</span><span class="sxs-lookup"><span data-stu-id="bf198-125">-Permission</span></span>
<span data-ttu-id="bf198-126">[許可權] 欄位是3個字元的序列，其中第一個字元是 "r" 以准許讀取存取權，第二個字元是 "w" 以授與寫入存取權，而第三個字元是 "x" 來授與執行許可權。</span><span class="sxs-lookup"><span data-stu-id="bf198-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="bf198-127">如果沒有授與存取權，則會使用 "-" 字元表示該許可權遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="bf198-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="bf198-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf198-128">CommonParameters</span></span>
<span data-ttu-id="bf198-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf198-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf198-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf198-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf198-131">輸入</span><span class="sxs-lookup"><span data-stu-id="bf198-131">INPUTS</span></span>

### <span data-ttu-id="bf198-132">所有</span><span class="sxs-lookup"><span data-stu-id="bf198-132">None</span></span>

## <span data-ttu-id="bf198-133">輸出</span><span class="sxs-lookup"><span data-stu-id="bf198-133">OUTPUTS</span></span>

### <span data-ttu-id="bf198-134">WindowsAzure. ResourceModel.. PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="bf198-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="bf198-135">筆記</span><span class="sxs-lookup"><span data-stu-id="bf198-135">NOTES</span></span>

## <span data-ttu-id="bf198-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf198-136">RELATED LINKS</span></span>
