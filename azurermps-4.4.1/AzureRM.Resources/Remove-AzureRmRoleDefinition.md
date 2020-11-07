---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624767"
---
# <span data-ttu-id="85c86-101">Remove-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85c86-101">Remove-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="85c86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85c86-102">SYNOPSIS</span></span>
<span data-ttu-id="85c86-103">刪除 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="85c86-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="85c86-104">使用角色的識別碼屬性指定要刪除的角色。</span><span class="sxs-lookup"><span data-stu-id="85c86-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="85c86-105">如果有針對自訂角色的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="85c86-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c86-106">句法</span><span class="sxs-lookup"><span data-stu-id="85c86-106">SYNTAX</span></span>

### <span data-ttu-id="85c86-107">RoleDefinitionIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="85c86-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c86-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c86-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c86-109">說明</span><span class="sxs-lookup"><span data-stu-id="85c86-109">DESCRIPTION</span></span>
<span data-ttu-id="85c86-110">Remove-AzureRmRoleDefinition Cmdlet 會刪除 Azure Role-Based 存取控制中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="85c86-110">The Remove-AzureRmRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="85c86-111">提供現有自訂角色的識別碼參數以刪除該自訂角色。</span><span class="sxs-lookup"><span data-stu-id="85c86-111">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="85c86-112">根據預設，Remove-AzureRmRoleDefinition 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85c86-112">By default, Remove-AzureRmRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="85c86-113">若要取消提示，請使用 Force 參數。</span><span class="sxs-lookup"><span data-stu-id="85c86-113">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="85c86-114">如果已為要刪除的自訂角色所做的現有角色指派，刪除將會失敗。</span><span class="sxs-lookup"><span data-stu-id="85c86-114">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="85c86-115">示例</span><span class="sxs-lookup"><span data-stu-id="85c86-115">EXAMPLES</span></span>

### <span data-ttu-id="85c86-116">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="85c86-116">--------------------------  Example 1  --------------------------</span></span>
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### <span data-ttu-id="85c86-117">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="85c86-117">--------------------------  Example 2  --------------------------</span></span>
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="85c86-118">參數</span><span class="sxs-lookup"><span data-stu-id="85c86-118">PARAMETERS</span></span>

### <span data-ttu-id="85c86-119">-Force</span><span class="sxs-lookup"><span data-stu-id="85c86-119">-Force</span></span>
<span data-ttu-id="85c86-120">如果設定，則在刪除自訂角色前，不會提示您確認</span><span class="sxs-lookup"><span data-stu-id="85c86-120">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="85c86-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="85c86-121">-Id</span></span>
<span data-ttu-id="85c86-122">要刪除的角色定義識別碼</span><span class="sxs-lookup"><span data-stu-id="85c86-122">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="85c86-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="85c86-123">-Name</span></span>
<span data-ttu-id="85c86-124">要刪除之角色定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="85c86-124">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="85c86-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85c86-125">-PassThru</span></span>
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

### <span data-ttu-id="85c86-126">-範圍</span><span class="sxs-lookup"><span data-stu-id="85c86-126">-Scope</span></span>
<span data-ttu-id="85c86-127">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="85c86-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85c86-128">-確認</span><span class="sxs-lookup"><span data-stu-id="85c86-128">-Confirm</span></span>
<span data-ttu-id="85c86-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85c86-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c86-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c86-130">-WhatIf</span></span>
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

### <span data-ttu-id="85c86-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c86-131">-DefaultProfile</span></span>
<span data-ttu-id="85c86-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85c86-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c86-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c86-133">CommonParameters</span></span>
<span data-ttu-id="85c86-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85c86-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c86-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85c86-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c86-136">輸入</span><span class="sxs-lookup"><span data-stu-id="85c86-136">INPUTS</span></span>

## <span data-ttu-id="85c86-137">輸出</span><span class="sxs-lookup"><span data-stu-id="85c86-137">OUTPUTS</span></span>

### <span data-ttu-id="85c86-138">System.object</span><span class="sxs-lookup"><span data-stu-id="85c86-138">System.Boolean</span></span>

## <span data-ttu-id="85c86-139">筆記</span><span class="sxs-lookup"><span data-stu-id="85c86-139">NOTES</span></span>
<span data-ttu-id="85c86-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="85c86-140">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="85c86-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="85c86-141">RELATED LINKS</span></span>

[<span data-ttu-id="85c86-142">新-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85c86-142">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="85c86-143">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85c86-143">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="85c86-144">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="85c86-144">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

