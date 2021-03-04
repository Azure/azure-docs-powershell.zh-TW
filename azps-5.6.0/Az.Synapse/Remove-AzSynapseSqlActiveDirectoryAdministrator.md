---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 88e65b1c38f7550e5e7f90aa436fd510e203acf4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914246"
---
# <span data-ttu-id="4dc71-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="4dc71-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="4dc71-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4dc71-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc71-103">移除 Synapse Analytics Workspace 的 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="4dc71-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="4dc71-104">語法</span><span class="sxs-lookup"><span data-stu-id="4dc71-104">SYNTAX</span></span>

### <span data-ttu-id="4dc71-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4dc71-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4dc71-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dc71-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc71-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dc71-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc71-108">描述</span><span class="sxs-lookup"><span data-stu-id="4dc71-108">DESCRIPTION</span></span>
<span data-ttu-id="4dc71-109">**Remove-AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會移除 Azure Synapse Analytics Workspace 的 Azure Active Directory (Azure AD) 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="4dc71-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="4dc71-110">例子</span><span class="sxs-lookup"><span data-stu-id="4dc71-110">EXAMPLES</span></span>

### <span data-ttu-id="4dc71-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="4dc71-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="4dc71-112">此命令會移除名為 ContosoWorkspace 之工作區的 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="4dc71-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4dc71-113">參數</span><span class="sxs-lookup"><span data-stu-id="4dc71-113">PARAMETERS</span></span>

### <span data-ttu-id="4dc71-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dc71-114">-AsJob</span></span>
<span data-ttu-id="4dc71-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4dc71-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dc71-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc71-116">-DefaultProfile</span></span>
<span data-ttu-id="4dc71-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dc71-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc71-118">-強制</span><span class="sxs-lookup"><span data-stu-id="4dc71-118">-Force</span></span>
<span data-ttu-id="4dc71-119">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="4dc71-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4dc71-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dc71-120">-InputObject</span></span>
<span data-ttu-id="4dc71-121">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="4dc71-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc71-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dc71-122">-PassThru</span></span>
<span data-ttu-id="4dc71-123">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="4dc71-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4dc71-124">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="4dc71-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4dc71-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc71-125">-ResourceGroupName</span></span>
<span data-ttu-id="4dc71-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4dc71-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc71-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dc71-127">-ResourceId</span></span>
<span data-ttu-id="4dc71-128">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4dc71-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc71-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4dc71-129">-WorkspaceName</span></span>
<span data-ttu-id="4dc71-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="4dc71-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4dc71-131">-確認</span><span class="sxs-lookup"><span data-stu-id="4dc71-131">-Confirm</span></span>
<span data-ttu-id="4dc71-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4dc71-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc71-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc71-133">-WhatIf</span></span>
<span data-ttu-id="4dc71-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4dc71-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc71-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4dc71-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc71-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc71-136">CommonParameters</span></span>
<span data-ttu-id="4dc71-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4dc71-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc71-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dc71-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc71-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4dc71-139">INPUTS</span></span>

### <span data-ttu-id="4dc71-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4dc71-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4dc71-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4dc71-141">OUTPUTS</span></span>

### <span data-ttu-id="4dc71-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dc71-142">System.Boolean</span></span>

## <span data-ttu-id="4dc71-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4dc71-143">NOTES</span></span>

## <span data-ttu-id="4dc71-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dc71-144">RELATED LINKS</span></span>
