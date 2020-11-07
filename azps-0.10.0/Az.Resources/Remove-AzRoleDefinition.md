---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f31a09f0d148d25796e157eb300a6f5918dade44
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795215"
---
# <span data-ttu-id="e5b05-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e5b05-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="e5b05-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5b05-102">SYNOPSIS</span></span>
<span data-ttu-id="e5b05-103">刪除 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e5b05-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e5b05-104">使用角色的識別碼屬性指定要刪除的角色。</span><span class="sxs-lookup"><span data-stu-id="e5b05-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="e5b05-105">如果有針對自訂角色的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e5b05-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="e5b05-106">句法</span><span class="sxs-lookup"><span data-stu-id="e5b05-106">SYNTAX</span></span>

### <span data-ttu-id="e5b05-107">RoleDefinitionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e5b05-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5b05-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b05-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5b05-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5b05-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5b05-110">說明</span><span class="sxs-lookup"><span data-stu-id="e5b05-110">DESCRIPTION</span></span>
<span data-ttu-id="e5b05-111">Remove-AzRoleDefinition Cmdlet 會刪除 Azure Role-Based 存取控制中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e5b05-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e5b05-112">提供現有自訂角色的識別碼參數以刪除該自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e5b05-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="e5b05-113">根據預設，Remove-AzRoleDefinition 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5b05-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="e5b05-114">若要取消提示，請使用 Force 參數。</span><span class="sxs-lookup"><span data-stu-id="e5b05-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="e5b05-115">如果已為要刪除的自訂角色所做的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e5b05-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="e5b05-116">示例</span><span class="sxs-lookup"><span data-stu-id="e5b05-116">EXAMPLES</span></span>

### <span data-ttu-id="e5b05-117">範例1</span><span class="sxs-lookup"><span data-stu-id="e5b05-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="e5b05-118">範例2</span><span class="sxs-lookup"><span data-stu-id="e5b05-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="e5b05-119">參數</span><span class="sxs-lookup"><span data-stu-id="e5b05-119">PARAMETERS</span></span>

### <span data-ttu-id="e5b05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5b05-120">-DefaultProfile</span></span>
<span data-ttu-id="e5b05-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5b05-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5b05-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e5b05-122">-Force</span></span>
<span data-ttu-id="e5b05-123">如果設定，則在刪除自訂角色前，不會提示您確認</span><span class="sxs-lookup"><span data-stu-id="e5b05-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="e5b05-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e5b05-124">-Id</span></span>
<span data-ttu-id="e5b05-125">要刪除的角色定義識別碼</span><span class="sxs-lookup"><span data-stu-id="e5b05-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b05-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5b05-126">-InputObject</span></span>
<span data-ttu-id="e5b05-127">代表要移除之角色定義的物件。</span><span class="sxs-lookup"><span data-stu-id="e5b05-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b05-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5b05-128">-Name</span></span>
<span data-ttu-id="e5b05-129">要刪除之角色定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5b05-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b05-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5b05-130">-PassThru</span></span>
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

### <span data-ttu-id="e5b05-131">-範圍</span><span class="sxs-lookup"><span data-stu-id="e5b05-131">-Scope</span></span>
<span data-ttu-id="e5b05-132">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="e5b05-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5b05-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e5b05-133">-Confirm</span></span>
<span data-ttu-id="e5b05-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5b05-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5b05-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5b05-135">-WhatIf</span></span>
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

### <span data-ttu-id="e5b05-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5b05-136">CommonParameters</span></span>
<span data-ttu-id="e5b05-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5b05-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5b05-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5b05-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5b05-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e5b05-139">INPUTS</span></span>

### <span data-ttu-id="e5b05-140">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="e5b05-140">System.Guid</span></span>

### <span data-ttu-id="e5b05-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e5b05-141">System.String</span></span>

### <span data-ttu-id="e5b05-142">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="e5b05-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="e5b05-143">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e5b05-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e5b05-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e5b05-144">OUTPUTS</span></span>

### <span data-ttu-id="e5b05-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e5b05-145">System.Boolean</span></span>

## <span data-ttu-id="e5b05-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e5b05-146">NOTES</span></span>
<span data-ttu-id="e5b05-147">關鍵字： azure，Az，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="e5b05-147">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e5b05-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5b05-148">RELATED LINKS</span></span>

[<span data-ttu-id="e5b05-149">新-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e5b05-149">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="e5b05-150">AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e5b05-150">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="e5b05-151">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e5b05-151">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

