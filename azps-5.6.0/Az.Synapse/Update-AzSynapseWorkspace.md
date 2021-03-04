---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseWorkspace.md
ms.openlocfilehash: 60631b8d4c42ac314268453c5dedf16893281861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913294"
---
# <span data-ttu-id="ea68f-101">Update-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea68f-101">Update-AzSynapseWorkspace</span></span>

## <span data-ttu-id="ea68f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea68f-102">SYNOPSIS</span></span>
<span data-ttu-id="ea68f-103">更新 Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="ea68f-103">Updates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ea68f-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea68f-104">SYNTAX</span></span>

### <span data-ttu-id="ea68f-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ea68f-105">SetByNameParameterSet (Default)</span></span>
```
Update-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>] [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea68f-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea68f-106">SetByInputObjectParameterSet</span></span>
```
Update-AzSynapseWorkspace -InputObject <PSSynapseWorkspace> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea68f-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea68f-107">SetByResourceIdParameterSet</span></span>
```
Update-AzSynapseWorkspace -ResourceId <String> [-Tag <Hashtable>]
 [-SqlAdministratorLoginPassword <SecureString>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea68f-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea68f-108">DESCRIPTION</span></span>
<span data-ttu-id="ea68f-109">**Update-AzSynapseWorkspace** Cmdlet 會更新 Azure Synapse Analytics 工作區。</span><span class="sxs-lookup"><span data-stu-id="ea68f-109">The **Update-AzSynapseWorkspace** cmdlet updates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="ea68f-110">例子</span><span class="sxs-lookup"><span data-stu-id="ea68f-110">EXAMPLES</span></span>

### <span data-ttu-id="ea68f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="ea68f-111">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -Name ContosoWorkspace -Tag @{'key'='value'}
```

<span data-ttu-id="ea68f-112">這個命令會更新指定之 Azure Synapse Analytics 工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="ea68f-112">This commands updates tags for the specififed Azure Synapse Analytics workspace.</span></span>

### <span data-ttu-id="ea68f-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="ea68f-113">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseWorkspace -Tag @{'key'='value1'}
```

<span data-ttu-id="ea68f-114">這個命令會透過管道更新指定 Azure Synapse Analytics 工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="ea68f-114">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline.</span></span>

### <span data-ttu-id="ea68f-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="ea68f-115">Example 3</span></span>
```powershell
PS C:\> Update-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace -Tag @{'key'='value2'}
```

<span data-ttu-id="ea68f-116">這個命令會使用資源識別碼透過管線更新指定 Azure Synapse Analytics 工作區的標記。</span><span class="sxs-lookup"><span data-stu-id="ea68f-116">This commands updates tags for the specififed Azure Synapse Analytics workspace through pipeline with resource ID.</span></span>

## <span data-ttu-id="ea68f-117">參數</span><span class="sxs-lookup"><span data-stu-id="ea68f-117">PARAMETERS</span></span>

### <span data-ttu-id="ea68f-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea68f-118">-AsJob</span></span>
<span data-ttu-id="ea68f-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ea68f-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea68f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea68f-120">-DefaultProfile</span></span>
<span data-ttu-id="ea68f-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea68f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea68f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea68f-122">-InputObject</span></span>
<span data-ttu-id="ea68f-123">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="ea68f-123">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea68f-124">-Name</span></span>
<span data-ttu-id="ea68f-125">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ea68f-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea68f-126">-ResourceGroupName</span></span>
<span data-ttu-id="ea68f-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ea68f-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea68f-128">-ResourceId</span></span>
<span data-ttu-id="ea68f-129">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea68f-129">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-130">-SqlAdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="ea68f-130">-SqlAdministratorLoginPassword</span></span>
<span data-ttu-id="ea68f-131">工作區的新 SQL 系統管理員密碼。</span><span class="sxs-lookup"><span data-stu-id="ea68f-131">The new SQL administrator password for the workspace.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-132">-標記</span><span class="sxs-lookup"><span data-stu-id="ea68f-132">-Tag</span></span>
<span data-ttu-id="ea68f-133">與資源關聯的標記字串字典。</span><span class="sxs-lookup"><span data-stu-id="ea68f-133">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea68f-134">-確認</span><span class="sxs-lookup"><span data-stu-id="ea68f-134">-Confirm</span></span>
<span data-ttu-id="ea68f-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea68f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea68f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea68f-136">-WhatIf</span></span>
<span data-ttu-id="ea68f-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea68f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea68f-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea68f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea68f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea68f-139">CommonParameters</span></span>
<span data-ttu-id="ea68f-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea68f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea68f-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea68f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea68f-142">輸入</span><span class="sxs-lookup"><span data-stu-id="ea68f-142">INPUTS</span></span>

### <span data-ttu-id="ea68f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea68f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea68f-144">輸出</span><span class="sxs-lookup"><span data-stu-id="ea68f-144">OUTPUTS</span></span>

### <span data-ttu-id="ea68f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ea68f-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ea68f-146">筆記</span><span class="sxs-lookup"><span data-stu-id="ea68f-146">NOTES</span></span>

## <span data-ttu-id="ea68f-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea68f-147">RELATED LINKS</span></span>
