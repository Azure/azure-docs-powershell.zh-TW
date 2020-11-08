---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128629"
---
# <span data-ttu-id="8553e-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8553e-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="8553e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8553e-102">SYNOPSIS</span></span>
<span data-ttu-id="8553e-103">取得管理群組 (s) </span><span class="sxs-lookup"><span data-stu-id="8553e-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="8553e-104">句法</span><span class="sxs-lookup"><span data-stu-id="8553e-104">SYNTAX</span></span>

### <span data-ttu-id="8553e-105">ListOperation (預設) </span><span class="sxs-lookup"><span data-stu-id="8553e-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8553e-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="8553e-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8553e-107">說明</span><span class="sxs-lookup"><span data-stu-id="8553e-107">DESCRIPTION</span></span>
<span data-ttu-id="8553e-108">Get-AzManagementGroup Cmdlet 會取得全部或特定的管理群組。</span><span class="sxs-lookup"><span data-stu-id="8553e-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="8553e-109">示例</span><span class="sxs-lookup"><span data-stu-id="8553e-109">EXAMPLES</span></span>

### <span data-ttu-id="8553e-110">範例1：取得所有管理群組</span><span class="sxs-lookup"><span data-stu-id="8553e-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="8553e-111">範例2：取得特定的管理群組</span><span class="sxs-lookup"><span data-stu-id="8553e-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8553e-112">範例3：取得特定的管理群組和第一層階層</span><span class="sxs-lookup"><span data-stu-id="8553e-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="8553e-113">有了 `Expand` 標誌，一個可以在陣列中流覽 `Children` ，並取得每個子代的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8553e-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="8553e-114">例如， `Children[0]` 將會提供顯示名稱之群組的詳細資料 `TestGroup1DisplayName` 。</span><span class="sxs-lookup"><span data-stu-id="8553e-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="8553e-115">範例4：取得特定的管理群組及所有層級</span><span class="sxs-lookup"><span data-stu-id="8553e-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="8553e-116">參數</span><span class="sxs-lookup"><span data-stu-id="8553e-116">PARAMETERS</span></span>

### <span data-ttu-id="8553e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8553e-117">-DefaultProfile</span></span>
<span data-ttu-id="8553e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8553e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8553e-119">-展開</span><span class="sxs-lookup"><span data-stu-id="8553e-119">-Expand</span></span>
<span data-ttu-id="8553e-120">展開輸出以列出管理群組的子系</span><span class="sxs-lookup"><span data-stu-id="8553e-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8553e-121">-[名]</span><span class="sxs-lookup"><span data-stu-id="8553e-121">-GroupName</span></span>
<span data-ttu-id="8553e-122">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="8553e-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8553e-123">-遞迴</span><span class="sxs-lookup"><span data-stu-id="8553e-123">-Recurse</span></span>
<span data-ttu-id="8553e-124">遞迴清單管理群組的子系</span><span class="sxs-lookup"><span data-stu-id="8553e-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8553e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8553e-125">-Confirm</span></span>
<span data-ttu-id="8553e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8553e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8553e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8553e-127">-WhatIf</span></span>
<span data-ttu-id="8553e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8553e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8553e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8553e-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8553e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8553e-130">CommonParameters</span></span>
<span data-ttu-id="8553e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8553e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8553e-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8553e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8553e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8553e-133">INPUTS</span></span>

### <span data-ttu-id="8553e-134">所有</span><span class="sxs-lookup"><span data-stu-id="8553e-134">None</span></span>

## <span data-ttu-id="8553e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="8553e-135">OUTPUTS</span></span>

### <span data-ttu-id="8553e-136">[ManagementGroups].. PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="8553e-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="8553e-137">[ManagementGroups].. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8553e-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="8553e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8553e-138">NOTES</span></span>

## <span data-ttu-id="8553e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="8553e-139">RELATED LINKS</span></span>