---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 58b2aa2f62de5cc47a9319c9cf36b0d2c8d55975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904206"
---
# <span data-ttu-id="21e0f-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="21e0f-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="21e0f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="21e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="21e0f-103">停用工作區上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="21e0f-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="21e0f-104">語法</span><span class="sxs-lookup"><span data-stu-id="21e0f-104">SYNTAX</span></span>

### <span data-ttu-id="21e0f-105">DisableByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21e0f-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e0f-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21e0f-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21e0f-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21e0f-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21e0f-108">描述</span><span class="sxs-lookup"><span data-stu-id="21e0f-108">DESCRIPTION</span></span>
<span data-ttu-id="21e0f-109">**Disable-AzSynapseSqlAdvancedDataSecurity** Cmdlet 會停用工作區上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="21e0f-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="21e0f-110">例子</span><span class="sxs-lookup"><span data-stu-id="21e0f-110">EXAMPLES</span></span>

### <span data-ttu-id="21e0f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="21e0f-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="21e0f-112">此命令會停用名為 ContosoWorkspace 之工作區上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="21e0f-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="21e0f-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="21e0f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="21e0f-114">此命令會透過管道停用名為 ContosoWorkspace 的工作區上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="21e0f-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="21e0f-115">參數</span><span class="sxs-lookup"><span data-stu-id="21e0f-115">PARAMETERS</span></span>

### <span data-ttu-id="21e0f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21e0f-116">-AsJob</span></span>
<span data-ttu-id="21e0f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="21e0f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21e0f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e0f-118">-DefaultProfile</span></span>
<span data-ttu-id="21e0f-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="21e0f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21e0f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21e0f-120">-InputObject</span></span>
<span data-ttu-id="21e0f-121">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="21e0f-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="21e0f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e0f-122">-ResourceGroupName</span></span>
<span data-ttu-id="21e0f-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="21e0f-123">Resource group name.</span></span>

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

### <span data-ttu-id="21e0f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21e0f-124">-ResourceId</span></span>
<span data-ttu-id="21e0f-125">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21e0f-125">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="21e0f-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="21e0f-126">-WorkspaceName</span></span>
<span data-ttu-id="21e0f-127">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="21e0f-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="21e0f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="21e0f-128">-Confirm</span></span>
<span data-ttu-id="21e0f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="21e0f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21e0f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21e0f-130">-WhatIf</span></span>
<span data-ttu-id="21e0f-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21e0f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21e0f-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21e0f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21e0f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e0f-133">CommonParameters</span></span>
<span data-ttu-id="21e0f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="21e0f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e0f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21e0f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e0f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="21e0f-136">INPUTS</span></span>

### <span data-ttu-id="21e0f-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="21e0f-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="21e0f-138">輸出</span><span class="sxs-lookup"><span data-stu-id="21e0f-138">OUTPUTS</span></span>

### <span data-ttu-id="21e0f-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="21e0f-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="21e0f-140">筆記</span><span class="sxs-lookup"><span data-stu-id="21e0f-140">NOTES</span></span>

## <span data-ttu-id="21e0f-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="21e0f-141">RELATED LINKS</span></span>
