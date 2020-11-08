---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969103"
---
# <span data-ttu-id="fdf2e-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2e-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="fdf2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf2e-103">建立管理群組</span><span class="sxs-lookup"><span data-stu-id="fdf2e-103">Creates a Management Group</span></span>

## <span data-ttu-id="fdf2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdf2e-104">SYNTAX</span></span>

### <span data-ttu-id="fdf2e-105">GroupOperations (預設) </span><span class="sxs-lookup"><span data-stu-id="fdf2e-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf2e-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="fdf2e-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="fdf2e-107">DESCRIPTION</span></span>
<span data-ttu-id="fdf2e-108">**新的-AzManagementGroup** Cmdlet 會建立管理群組。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="fdf2e-109">示例</span><span class="sxs-lookup"><span data-stu-id="fdf2e-109">EXAMPLES</span></span>

### <span data-ttu-id="fdf2e-110">範例1：建立管理群組</span><span class="sxs-lookup"><span data-stu-id="fdf2e-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="fdf2e-111">建立新群組 `DisplayName` ，並將其 `ParentId` 設定為 `null` 。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="fdf2e-112">[與 `DisplayName` 群組的父項一樣] 就會 `GroupName` 是租使用者。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="fdf2e-113">範例2：使用顯示名稱建立管理群組</span><span class="sxs-lookup"><span data-stu-id="fdf2e-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="fdf2e-114">在這種情況下，群組的父級將是租使用者， `DisplayName` 將會設定為提供的值。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="fdf2e-115">範例3：使用父級和顯示名稱建立管理群組</span><span class="sxs-lookup"><span data-stu-id="fdf2e-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

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

### <span data-ttu-id="fdf2e-116">範例4：使用上層物件建立包含父項 (的管理群組) </span><span class="sxs-lookup"><span data-stu-id="fdf2e-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="fdf2e-117">參數</span><span class="sxs-lookup"><span data-stu-id="fdf2e-117">PARAMETERS</span></span>

### <span data-ttu-id="fdf2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf2e-118">-DefaultProfile</span></span>
<span data-ttu-id="fdf2e-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf2e-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fdf2e-120">-DisplayName</span></span>
<span data-ttu-id="fdf2e-121">管理群組的顯示名稱</span><span class="sxs-lookup"><span data-stu-id="fdf2e-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="fdf2e-122">-[名]</span><span class="sxs-lookup"><span data-stu-id="fdf2e-122">-GroupName</span></span>
<span data-ttu-id="fdf2e-123">管理群組識別碼</span><span class="sxs-lookup"><span data-stu-id="fdf2e-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2e-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="fdf2e-124">-ParentId</span></span>
<span data-ttu-id="fdf2e-125">管理群組的父識別碼</span><span class="sxs-lookup"><span data-stu-id="fdf2e-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2e-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fdf2e-126">-ParentObject</span></span>
<span data-ttu-id="fdf2e-127">上層物件</span><span class="sxs-lookup"><span data-stu-id="fdf2e-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdf2e-128">-確認</span><span class="sxs-lookup"><span data-stu-id="fdf2e-128">-Confirm</span></span>
<span data-ttu-id="fdf2e-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdf2e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf2e-130">-WhatIf</span></span>
<span data-ttu-id="fdf2e-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdf2e-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdf2e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf2e-133">CommonParameters</span></span>
<span data-ttu-id="fdf2e-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf2e-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fdf2e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf2e-136">輸入</span><span class="sxs-lookup"><span data-stu-id="fdf2e-136">INPUTS</span></span>

### <span data-ttu-id="fdf2e-137">所有</span><span class="sxs-lookup"><span data-stu-id="fdf2e-137">None</span></span>

## <span data-ttu-id="fdf2e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="fdf2e-138">OUTPUTS</span></span>

### <span data-ttu-id="fdf2e-139">[ManagementGroups].. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2e-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="fdf2e-140">筆記</span><span class="sxs-lookup"><span data-stu-id="fdf2e-140">NOTES</span></span>

## <span data-ttu-id="fdf2e-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdf2e-141">RELATED LINKS</span></span>

[<span data-ttu-id="fdf2e-142">移除-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2e-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="fdf2e-143">更新-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2e-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="fdf2e-144">AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="fdf2e-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)