---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2b937f147eebecd8a2aac7e2a70de1af4aa20c4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909390"
---
# <span data-ttu-id="e6cbb-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="e6cbb-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="e6cbb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e6cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cbb-103">啟用工作區上的進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="e6cbb-104">語法</span><span class="sxs-lookup"><span data-stu-id="e6cbb-104">SYNTAX</span></span>

### <span data-ttu-id="e6cbb-105">EnableByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6cbb-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cbb-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6cbb-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cbb-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6cbb-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6cbb-108">描述</span><span class="sxs-lookup"><span data-stu-id="e6cbb-108">DESCRIPTION</span></span>
<span data-ttu-id="e6cbb-109">**Enable-AzSynapseSqlAdvancedDataSecurity** Cmdlet 可在工作區上啟用進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="e6cbb-110">進位資料安全性是一個統一的安全性套件，其中包含適用于您工作區的資料分類、弱點評估及進一威脅防護。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="e6cbb-111"> (儲存弱點評定時，系統會自動建立新的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="e6cbb-112">如果儲存空間帳戶先前已建立為此用途，將會改為) </span><span class="sxs-lookup"><span data-stu-id="e6cbb-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="e6cbb-113">例子</span><span class="sxs-lookup"><span data-stu-id="e6cbb-113">EXAMPLES</span></span>

### <span data-ttu-id="e6cbb-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="e6cbb-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e6cbb-115">此命令可啟用工作區進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="e6cbb-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="e6cbb-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="e6cbb-117">此命令可讓工作區透過管線使用進位資料安全性。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="e6cbb-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="e6cbb-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="e6cbb-119">此命令可透過管線啟用工作區進位資料安全性，而且不會自動啟用弱點評定。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="e6cbb-120">參數</span><span class="sxs-lookup"><span data-stu-id="e6cbb-120">PARAMETERS</span></span>

### <span data-ttu-id="e6cbb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6cbb-121">-AsJob</span></span>
<span data-ttu-id="e6cbb-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e6cbb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6cbb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cbb-123">-DefaultProfile</span></span>
<span data-ttu-id="e6cbb-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6cbb-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="e6cbb-125">-DeploymentName</span></span>
<span data-ttu-id="e6cbb-126">提供進位資料安全性部署的自訂名稱。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-126">Supply a custom name for Advanced Data Security deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cbb-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="e6cbb-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="e6cbb-128">請勿自動啟用弱點評估 (這麼做不會建立儲存空間帳戶) 。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="e6cbb-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6cbb-129">-InputObject</span></span>
<span data-ttu-id="e6cbb-130">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-130">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: EnableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cbb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cbb-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6cbb-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cbb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6cbb-133">-ResourceId</span></span>
<span data-ttu-id="e6cbb-134">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-134">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cbb-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6cbb-135">-WorkspaceName</span></span>
<span data-ttu-id="e6cbb-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cbb-137">-確認</span><span class="sxs-lookup"><span data-stu-id="e6cbb-137">-Confirm</span></span>
<span data-ttu-id="e6cbb-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6cbb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cbb-139">-WhatIf</span></span>
<span data-ttu-id="e6cbb-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cbb-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6cbb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cbb-142">CommonParameters</span></span>
<span data-ttu-id="e6cbb-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e6cbb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cbb-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6cbb-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cbb-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e6cbb-145">INPUTS</span></span>

### <span data-ttu-id="e6cbb-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6cbb-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e6cbb-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e6cbb-147">OUTPUTS</span></span>

### <span data-ttu-id="e6cbb-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="e6cbb-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="e6cbb-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e6cbb-149">NOTES</span></span>

## <span data-ttu-id="e6cbb-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6cbb-150">RELATED LINKS</span></span>
