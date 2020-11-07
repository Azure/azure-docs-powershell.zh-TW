---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: cc65c4b4d7d4cc9cf73d3abdf135fd985f71efd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795173"
---
# <span data-ttu-id="8c312-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c312-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="8c312-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c312-102">SYNOPSIS</span></span>
<span data-ttu-id="8c312-103">更新管理群組</span><span class="sxs-lookup"><span data-stu-id="8c312-103">Updates a Management Group</span></span>

## <span data-ttu-id="8c312-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c312-104">SYNTAX</span></span>

### <span data-ttu-id="8c312-105">GroupOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="8c312-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c312-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c312-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c312-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c312-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c312-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="8c312-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c312-109">說明</span><span class="sxs-lookup"><span data-stu-id="8c312-109">DESCRIPTION</span></span>
<span data-ttu-id="8c312-110">**更新-AzManagementGroup** Cmdlet 會更新管理群組的 **ParentId** 或 **DisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="8c312-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="8c312-111">示例</span><span class="sxs-lookup"><span data-stu-id="8c312-111">EXAMPLES</span></span>

### <span data-ttu-id="8c312-112">範例1：更新管理群組的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8c312-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="8c312-113">範例2：更新管理群組的父項</span><span class="sxs-lookup"><span data-stu-id="8c312-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8c312-114">範例3：依管道 PSManagementGroup 物件更新管理群組</span><span class="sxs-lookup"><span data-stu-id="8c312-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="8c312-115">範例4：使用 ParentObject 更新管理群組的父項</span><span class="sxs-lookup"><span data-stu-id="8c312-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="8c312-116">參數</span><span class="sxs-lookup"><span data-stu-id="8c312-116">PARAMETERS</span></span>

### <span data-ttu-id="8c312-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c312-117">-DefaultProfile</span></span>
<span data-ttu-id="8c312-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c312-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8c312-119">-DisplayName</span></span>
<span data-ttu-id="8c312-120">管理群組的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="8c312-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="8c312-121">-[名]</span><span class="sxs-lookup"><span data-stu-id="8c312-121">-GroupName</span></span>
<span data-ttu-id="8c312-122">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="8c312-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c312-123">-InputObject</span></span>
<span data-ttu-id="8c312-124">從 [取得通話] 輸入物件</span><span class="sxs-lookup"><span data-stu-id="8c312-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="8c312-125">-ParentId</span></span>
<span data-ttu-id="8c312-126">管理群組的父識別碼</span><span class="sxs-lookup"><span data-stu-id="8c312-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8c312-127">-ParentObject</span></span>
<span data-ttu-id="8c312-128">從 [取得通話] 輸入物件</span><span class="sxs-lookup"><span data-stu-id="8c312-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c312-129">-確認</span><span class="sxs-lookup"><span data-stu-id="8c312-129">-Confirm</span></span>
<span data-ttu-id="8c312-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c312-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c312-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c312-131">-WhatIf</span></span>
<span data-ttu-id="8c312-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c312-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c312-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c312-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c312-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c312-134">CommonParameters</span></span>
<span data-ttu-id="8c312-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c312-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c312-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c312-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c312-137">輸入</span><span class="sxs-lookup"><span data-stu-id="8c312-137">INPUTS</span></span>

### <span data-ttu-id="8c312-138">[ManagementGroups].. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c312-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>
<span data-ttu-id="8c312-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="8c312-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8c312-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8c312-140">OUTPUTS</span></span>

### <span data-ttu-id="8c312-141">[ManagementGroups].. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8c312-141">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="8c312-142">筆記</span><span class="sxs-lookup"><span data-stu-id="8c312-142">NOTES</span></span>

## <span data-ttu-id="8c312-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c312-143">RELATED LINKS</span></span>
