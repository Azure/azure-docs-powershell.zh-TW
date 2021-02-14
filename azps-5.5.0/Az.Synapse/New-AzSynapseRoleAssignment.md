---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134314"
---
# <span data-ttu-id="fe3b2-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="fe3b2-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="fe3b2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3b2-103">建立 Synapse 分析角色指派。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fe3b2-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe3b2-104">SYNTAX</span></span>

### <span data-ttu-id="fe3b2-105">NewByWorkspaceNameAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fe3b2-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe3b2-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe3b2-113">說明</span><span class="sxs-lookup"><span data-stu-id="fe3b2-113">DESCRIPTION</span></span>
<span data-ttu-id="fe3b2-114">**新的-AzSynapseRoleAssignment** Cmdlet 會建立 Azure Synapse 分析角色分派。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="fe3b2-115">示例</span><span class="sxs-lookup"><span data-stu-id="fe3b2-115">EXAMPLES</span></span>

### <span data-ttu-id="fe3b2-116">範例1</span><span class="sxs-lookup"><span data-stu-id="fe3b2-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fe3b2-117">這個命令會將 ContosoRole 指派給其主要名稱為 ContosoName 的使用者。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="fe3b2-118">範例2</span><span class="sxs-lookup"><span data-stu-id="fe3b2-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="fe3b2-119">這個命令會將 ContosoRole 指派給主要名稱是透過管道 ContosoName 的使用者。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="fe3b2-120">參數</span><span class="sxs-lookup"><span data-stu-id="fe3b2-120">PARAMETERS</span></span>

### <span data-ttu-id="fe3b2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe3b2-121">-AsJob</span></span>
<span data-ttu-id="fe3b2-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fe3b2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe3b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe3b2-123">-DefaultProfile</span></span>
<span data-ttu-id="fe3b2-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe3b2-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fe3b2-125">-ObjectId</span></span>
<span data-ttu-id="fe3b2-126">使用者、群組或服務主體的 Azure AD ObjectId。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="fe3b2-127">-RoleDefinitionId</span></span>
<span data-ttu-id="fe3b2-128">指派給主體的角色識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-129">-RoleDefinitionName</span></span>
<span data-ttu-id="fe3b2-130">指派給主體的角色名稱。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-131">-ServicePrincipalName</span></span>
<span data-ttu-id="fe3b2-132">服務主體的 ServicePrincipalName。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-133">-SignInName</span></span>
<span data-ttu-id="fe3b2-134">使用者的電子郵件地址或使用者主要名稱。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fe3b2-135">-WorkspaceName</span></span>
<span data-ttu-id="fe3b2-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="fe3b2-137">-WorkspaceObject</span></span>
<span data-ttu-id="fe3b2-138">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe3b2-139">-確認</span><span class="sxs-lookup"><span data-stu-id="fe3b2-139">-Confirm</span></span>
<span data-ttu-id="fe3b2-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3b2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3b2-141">-WhatIf</span></span>
<span data-ttu-id="fe3b2-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe3b2-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3b2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3b2-144">CommonParameters</span></span>
<span data-ttu-id="fe3b2-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3b2-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3b2-147">輸入</span><span class="sxs-lookup"><span data-stu-id="fe3b2-147">INPUTS</span></span>

### <span data-ttu-id="fe3b2-148">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="fe3b2-149">輸出</span><span class="sxs-lookup"><span data-stu-id="fe3b2-149">OUTPUTS</span></span>

### <span data-ttu-id="fe3b2-150">PSRoleAssignmentDetails 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="fe3b2-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="fe3b2-151">筆記</span><span class="sxs-lookup"><span data-stu-id="fe3b2-151">NOTES</span></span>

## <span data-ttu-id="fe3b2-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe3b2-152">RELATED LINKS</span></span>
