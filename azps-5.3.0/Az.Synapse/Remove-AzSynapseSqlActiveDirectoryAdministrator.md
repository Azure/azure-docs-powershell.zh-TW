---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288128"
---
# <span data-ttu-id="6723f-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="6723f-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="6723f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6723f-102">SYNOPSIS</span></span>
<span data-ttu-id="6723f-103">移除 Synapse Analytics 工作區的 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="6723f-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="6723f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6723f-104">SYNTAX</span></span>

### <span data-ttu-id="6723f-105">RemoveByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6723f-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6723f-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6723f-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6723f-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6723f-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6723f-108">說明</span><span class="sxs-lookup"><span data-stu-id="6723f-108">DESCRIPTION</span></span>
<span data-ttu-id="6723f-109">**AzSynapseSqlActiveDirectoryAdministrator** Cmdlet 會針對 Azure Synapse Analytics 工作區 (azure AD) 管理員，移除 Azure Active Directory。</span><span class="sxs-lookup"><span data-stu-id="6723f-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="6723f-110">示例</span><span class="sxs-lookup"><span data-stu-id="6723f-110">EXAMPLES</span></span>

### <span data-ttu-id="6723f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6723f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="6723f-112">這個命令會移除名為 ContosoWorkspace 之工作區的 Azure AD 系統管理員。</span><span class="sxs-lookup"><span data-stu-id="6723f-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="6723f-113">參數</span><span class="sxs-lookup"><span data-stu-id="6723f-113">PARAMETERS</span></span>

### <span data-ttu-id="6723f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6723f-114">-AsJob</span></span>
<span data-ttu-id="6723f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6723f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6723f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6723f-116">-DefaultProfile</span></span>
<span data-ttu-id="6723f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6723f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6723f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6723f-118">-Force</span></span>
<span data-ttu-id="6723f-119">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="6723f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6723f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6723f-120">-InputObject</span></span>
<span data-ttu-id="6723f-121">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="6723f-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6723f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6723f-122">-PassThru</span></span>
<span data-ttu-id="6723f-123">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="6723f-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6723f-124">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6723f-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6723f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6723f-125">-ResourceGroupName</span></span>
<span data-ttu-id="6723f-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6723f-126">Resource group name.</span></span>

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

### <span data-ttu-id="6723f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6723f-127">-ResourceId</span></span>
<span data-ttu-id="6723f-128">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6723f-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="6723f-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6723f-129">-WorkspaceName</span></span>
<span data-ttu-id="6723f-130">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="6723f-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6723f-131">-確認</span><span class="sxs-lookup"><span data-stu-id="6723f-131">-Confirm</span></span>
<span data-ttu-id="6723f-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6723f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6723f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6723f-133">-WhatIf</span></span>
<span data-ttu-id="6723f-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6723f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6723f-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6723f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6723f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6723f-136">CommonParameters</span></span>
<span data-ttu-id="6723f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6723f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6723f-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6723f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6723f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6723f-139">INPUTS</span></span>

### <span data-ttu-id="6723f-140">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="6723f-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="6723f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="6723f-141">OUTPUTS</span></span>

### <span data-ttu-id="6723f-142">System.object</span><span class="sxs-lookup"><span data-stu-id="6723f-142">System.Boolean</span></span>

## <span data-ttu-id="6723f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6723f-143">NOTES</span></span>

## <span data-ttu-id="6723f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6723f-144">RELATED LINKS</span></span>
