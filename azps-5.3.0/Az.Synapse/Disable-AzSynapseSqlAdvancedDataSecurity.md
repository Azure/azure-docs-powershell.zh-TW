---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288340"
---
# <span data-ttu-id="d3a11-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="d3a11-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="d3a11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3a11-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a11-103">停用工作區上的 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="d3a11-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="d3a11-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3a11-104">SYNTAX</span></span>

### <span data-ttu-id="d3a11-105">DisableByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d3a11-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a11-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a11-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3a11-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3a11-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a11-108">說明</span><span class="sxs-lookup"><span data-stu-id="d3a11-108">DESCRIPTION</span></span>
<span data-ttu-id="d3a11-109">**Disable AzSynapseSqlAdvancedDataSecurity** Cmdlet 會停用工作區上的 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="d3a11-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="d3a11-110">示例</span><span class="sxs-lookup"><span data-stu-id="d3a11-110">EXAMPLES</span></span>

### <span data-ttu-id="d3a11-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d3a11-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d3a11-112">這個命令會在名為 ContosoWorkspace 的工作區上停用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="d3a11-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="d3a11-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d3a11-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="d3a11-114">這個命令會在名為 ContosoWorkspace 的工作區上停用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="d3a11-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="d3a11-115">參數</span><span class="sxs-lookup"><span data-stu-id="d3a11-115">PARAMETERS</span></span>

### <span data-ttu-id="d3a11-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3a11-116">-AsJob</span></span>
<span data-ttu-id="d3a11-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d3a11-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3a11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a11-118">-DefaultProfile</span></span>
<span data-ttu-id="d3a11-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3a11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a11-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3a11-120">-InputObject</span></span>
<span data-ttu-id="d3a11-121">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="d3a11-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3a11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a11-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3a11-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d3a11-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3a11-124">-ResourceId</span></span>
<span data-ttu-id="d3a11-125">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3a11-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a11-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d3a11-126">-WorkspaceName</span></span>
<span data-ttu-id="d3a11-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3a11-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a11-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d3a11-128">-Confirm</span></span>
<span data-ttu-id="d3a11-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3a11-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a11-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a11-130">-WhatIf</span></span>
<span data-ttu-id="d3a11-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3a11-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a11-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3a11-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a11-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a11-133">CommonParameters</span></span>
<span data-ttu-id="d3a11-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3a11-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a11-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3a11-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a11-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d3a11-136">INPUTS</span></span>

### <span data-ttu-id="d3a11-137">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d3a11-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d3a11-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d3a11-138">OUTPUTS</span></span>

### <span data-ttu-id="d3a11-139">WorkspaceAdvancedDataSecurityPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="d3a11-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="d3a11-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d3a11-140">NOTES</span></span>

## <span data-ttu-id="d3a11-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3a11-141">RELATED LINKS</span></span>
