---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: 90b7b0b1d7909210d86ec1d5ac6b465f6e9fb239
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801538"
---
# <span data-ttu-id="e6852-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e6852-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="e6852-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6852-102">SYNOPSIS</span></span>
<span data-ttu-id="e6852-103">刪除 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e6852-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="e6852-104">使用角色的識別碼屬性指定要刪除的角色。</span><span class="sxs-lookup"><span data-stu-id="e6852-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="e6852-105">如果有針對自訂角色的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6852-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6852-106">句法</span><span class="sxs-lookup"><span data-stu-id="e6852-106">SYNTAX</span></span>

### <span data-ttu-id="e6852-107">RoleDefinitionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6852-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6852-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6852-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6852-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6852-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6852-110">說明</span><span class="sxs-lookup"><span data-stu-id="e6852-110">DESCRIPTION</span></span>
<span data-ttu-id="e6852-111">Remove-AzureRmRoleDefinition Cmdlet 會刪除 Azure Role-Based 存取控制中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e6852-111">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="e6852-112">提供現有自訂角色的識別碼參數以刪除該自訂角色。</span><span class="sxs-lookup"><span data-stu-id="e6852-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="e6852-113">根據預設，Remove-AzureRmRoleDefinition 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6852-113">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="e6852-114">若要取消提示，請使用 Force 參數。</span><span class="sxs-lookup"><span data-stu-id="e6852-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="e6852-115">如果已為要刪除的自訂角色所做的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e6852-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="e6852-116">示例</span><span class="sxs-lookup"><span data-stu-id="e6852-116">EXAMPLES</span></span>

### <span data-ttu-id="e6852-117">範例1</span><span class="sxs-lookup"><span data-stu-id="e6852-117">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="e6852-118">範例2</span><span class="sxs-lookup"><span data-stu-id="e6852-118">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="e6852-119">參數</span><span class="sxs-lookup"><span data-stu-id="e6852-119">PARAMETERS</span></span>

### <span data-ttu-id="e6852-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6852-120">-DefaultProfile</span></span>
<span data-ttu-id="e6852-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e6852-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6852-122">-Force</span><span class="sxs-lookup"><span data-stu-id="e6852-122">-Force</span></span>
<span data-ttu-id="e6852-123">如果設定，則在刪除自訂角色前，不會提示您確認</span><span class="sxs-lookup"><span data-stu-id="e6852-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="e6852-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e6852-124">-Id</span></span>
<span data-ttu-id="e6852-125">要刪除的角色定義識別碼</span><span class="sxs-lookup"><span data-stu-id="e6852-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="e6852-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6852-126">-InputObject</span></span>
<span data-ttu-id="e6852-127">代表要移除之角色定義的物件。</span><span class="sxs-lookup"><span data-stu-id="e6852-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="e6852-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="e6852-128">-Name</span></span>
<span data-ttu-id="e6852-129">要刪除之角色定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6852-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="e6852-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6852-130">-PassThru</span></span>
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

### <span data-ttu-id="e6852-131">-範圍</span><span class="sxs-lookup"><span data-stu-id="e6852-131">-Scope</span></span>
<span data-ttu-id="e6852-132">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="e6852-132">Role definition scope.</span></span>

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

### <span data-ttu-id="e6852-133">-確認</span><span class="sxs-lookup"><span data-stu-id="e6852-133">-Confirm</span></span>
<span data-ttu-id="e6852-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6852-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6852-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6852-135">-WhatIf</span></span>
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

### <span data-ttu-id="e6852-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6852-136">CommonParameters</span></span>
<span data-ttu-id="e6852-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6852-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6852-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6852-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6852-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e6852-139">INPUTS</span></span>

### <span data-ttu-id="e6852-140">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="e6852-140">System.Guid</span></span>

### <span data-ttu-id="e6852-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e6852-141">System.String</span></span>

### <span data-ttu-id="e6852-142">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="e6852-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>
<span data-ttu-id="e6852-143">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e6852-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e6852-144">輸出</span><span class="sxs-lookup"><span data-stu-id="e6852-144">OUTPUTS</span></span>

### <span data-ttu-id="e6852-145">System.object</span><span class="sxs-lookup"><span data-stu-id="e6852-145">System.Boolean</span></span>

## <span data-ttu-id="e6852-146">筆記</span><span class="sxs-lookup"><span data-stu-id="e6852-146">NOTES</span></span>
<span data-ttu-id="e6852-147">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="e6852-147">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e6852-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6852-148">RELATED LINKS</span></span>

[<span data-ttu-id="e6852-149">新-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e6852-149">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="e6852-150">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e6852-150">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="e6852-151">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="e6852-151">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

