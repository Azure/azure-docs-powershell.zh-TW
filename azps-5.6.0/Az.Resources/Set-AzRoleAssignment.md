---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 785ddf5dac50a84c678ea995a3b948702b60195b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913333"
---
# <span data-ttu-id="4c0b8-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c0b8-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="4c0b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c0b8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0b8-103">更新現有的角色指派。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="4c0b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c0b8-104">SYNTAX</span></span>

### <span data-ttu-id="4c0b8-105">RoleAssignmentParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4c0b8-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0b8-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c0b8-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0b8-107">描述</span><span class="sxs-lookup"><span data-stu-id="4c0b8-107">DESCRIPTION</span></span>
<span data-ttu-id="4c0b8-108">使用 New-AzRoleAssignment 命令修改現有的作業。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="4c0b8-109">描述可以是任何有效的字串，請使用該字串來彼此推斷。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="4c0b8-110">如果條件已設定為條件版本，但如果您要更新不需要的條件，</span><span class="sxs-lookup"><span data-stu-id="4c0b8-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="4c0b8-111">條件版本可以從 1.0 升級至 2.0，但無法降級回來。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="4c0b8-112">請小心使用 2.0，因為 1.0 無法回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="4c0b8-113">例子</span><span class="sxs-lookup"><span data-stu-id="4c0b8-113">EXAMPLES</span></span>

### <span data-ttu-id="4c0b8-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="4c0b8-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="4c0b8-115">修改物件以更新現有角色指派</span><span class="sxs-lookup"><span data-stu-id="4c0b8-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="4c0b8-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="4c0b8-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="4c0b8-117">使用檔案更新現有的角色指派</span><span class="sxs-lookup"><span data-stu-id="4c0b8-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="4c0b8-118">參數</span><span class="sxs-lookup"><span data-stu-id="4c0b8-118">PARAMETERS</span></span>

### <span data-ttu-id="4c0b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0b8-119">-DefaultProfile</span></span>
<span data-ttu-id="4c0b8-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c0b8-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="4c0b8-121">-InputFile</span></span>
<span data-ttu-id="4c0b8-122">包含單一角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c0b8-123">-InputObject</span></span>
<span data-ttu-id="4c0b8-124">角色指派。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c0b8-125">-PassThru</span></span>
<span data-ttu-id="4c0b8-126">如果指定，會顯示更新的角色指派</span><span class="sxs-lookup"><span data-stu-id="4c0b8-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="4c0b8-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4c0b8-127">-Confirm</span></span>
<span data-ttu-id="4c0b8-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0b8-129">-WhatIf</span></span>
<span data-ttu-id="4c0b8-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c0b8-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c0b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0b8-132">CommonParameters</span></span>
<span data-ttu-id="4c0b8-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c0b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0b8-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c0b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0b8-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4c0b8-135">INPUTS</span></span>

### <span data-ttu-id="4c0b8-136">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c0b8-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="4c0b8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4c0b8-137">OUTPUTS</span></span>

### <span data-ttu-id="4c0b8-138">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="4c0b8-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="4c0b8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4c0b8-139">NOTES</span></span>

## <span data-ttu-id="4c0b8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c0b8-140">RELATED LINKS</span></span>
