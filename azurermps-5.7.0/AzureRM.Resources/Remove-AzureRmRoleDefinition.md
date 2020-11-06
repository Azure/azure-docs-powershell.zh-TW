---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: ae4f8e11ac213943d8cfcec162b43abde60fe753
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454127"
---
# <span data-ttu-id="42065-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42065-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="42065-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42065-102">SYNOPSIS</span></span>
<span data-ttu-id="42065-103">刪除 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="42065-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="42065-104">使用角色的識別碼屬性指定要刪除的角色。</span><span class="sxs-lookup"><span data-stu-id="42065-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="42065-105">如果有針對自訂角色的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="42065-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42065-106">句法</span><span class="sxs-lookup"><span data-stu-id="42065-106">SYNTAX</span></span>

### <span data-ttu-id="42065-107">RoleDefinitionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="42065-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42065-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42065-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42065-109">說明</span><span class="sxs-lookup"><span data-stu-id="42065-109">DESCRIPTION</span></span>
<span data-ttu-id="42065-110">Remove-AzureRmRoleDefinition Cmdlet 會刪除 Azure Role-Based 存取控制中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="42065-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="42065-111">提供現有自訂角色的識別碼參數以刪除該自訂角色。</span><span class="sxs-lookup"><span data-stu-id="42065-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="42065-112">根據預設，Remove-AzureRmRoleDefinition 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42065-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="42065-113">若要取消提示，請使用 Force 參數。</span><span class="sxs-lookup"><span data-stu-id="42065-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="42065-114">如果已為要刪除的自訂角色所做的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="42065-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="42065-115">示例</span><span class="sxs-lookup"><span data-stu-id="42065-115">EXAMPLES</span></span>

### <span data-ttu-id="42065-116">範例1</span><span class="sxs-lookup"><span data-stu-id="42065-116">Example 1</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="42065-117">範例2</span><span class="sxs-lookup"><span data-stu-id="42065-117">Example 2</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="42065-118">參數</span><span class="sxs-lookup"><span data-stu-id="42065-118">PARAMETERS</span></span>

### <span data-ttu-id="42065-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42065-119">-DefaultProfile</span></span>
<span data-ttu-id="42065-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42065-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42065-121">-Force</span><span class="sxs-lookup"><span data-stu-id="42065-121">-Force</span></span>
<span data-ttu-id="42065-122">如果設定，則在刪除自訂角色前，不會提示您確認</span><span class="sxs-lookup"><span data-stu-id="42065-122">If set, does not prompt for a confirmation before deleting the custom role</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42065-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="42065-123">-Id</span></span>
<span data-ttu-id="42065-124">要刪除的角色定義識別碼</span><span class="sxs-lookup"><span data-stu-id="42065-124">Id of the Role definition to be deleted</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42065-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="42065-125">-Name</span></span>
<span data-ttu-id="42065-126">要刪除之角色定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="42065-126">Name of the Role definition to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42065-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42065-127">-PassThru</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42065-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="42065-128">-Scope</span></span>
<span data-ttu-id="42065-129">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="42065-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42065-130">-確認</span><span class="sxs-lookup"><span data-stu-id="42065-130">-Confirm</span></span>
<span data-ttu-id="42065-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="42065-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42065-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42065-132">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42065-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42065-133">CommonParameters</span></span>
<span data-ttu-id="42065-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42065-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42065-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42065-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42065-136">輸入</span><span class="sxs-lookup"><span data-stu-id="42065-136">INPUTS</span></span>

### <span data-ttu-id="42065-137">所有</span><span class="sxs-lookup"><span data-stu-id="42065-137">None</span></span>
<span data-ttu-id="42065-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="42065-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42065-139">輸出</span><span class="sxs-lookup"><span data-stu-id="42065-139">OUTPUTS</span></span>

### <span data-ttu-id="42065-140">System.object</span><span class="sxs-lookup"><span data-stu-id="42065-140">System.Boolean</span></span>

## <span data-ttu-id="42065-141">筆記</span><span class="sxs-lookup"><span data-stu-id="42065-141">NOTES</span></span>
<span data-ttu-id="42065-142">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="42065-142">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="42065-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="42065-143">RELATED LINKS</span></span>

[<span data-ttu-id="42065-144">新-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42065-144">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="42065-145">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42065-145">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="42065-146">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="42065-146">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

