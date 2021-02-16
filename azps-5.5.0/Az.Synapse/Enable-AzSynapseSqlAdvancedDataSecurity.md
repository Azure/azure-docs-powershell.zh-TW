---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: dea0770af8cca14ebd523f67b69d7a12931183ec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137718"
---
# <span data-ttu-id="48839-101">Enable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="48839-101">Enable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="48839-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48839-102">SYNOPSIS</span></span>
<span data-ttu-id="48839-103">在工作區上啟用 [高級資料安全性]。</span><span class="sxs-lookup"><span data-stu-id="48839-103">Enables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="48839-104">句法</span><span class="sxs-lookup"><span data-stu-id="48839-104">SYNTAX</span></span>

### <span data-ttu-id="48839-105">EnableByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="48839-105">EnableByNameParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48839-106">EnableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48839-106">EnableByInputObjectParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace>
 [-DoNotConfigureVulnerabilityAssessment] [-DeploymentName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48839-107">EnableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="48839-107">EnableByResourceIdParameterSet</span></span>
```
Enable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-DoNotConfigureVulnerabilityAssessment]
 [-DeploymentName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48839-108">說明</span><span class="sxs-lookup"><span data-stu-id="48839-108">DESCRIPTION</span></span>
<span data-ttu-id="48839-109">**Enable-AzSynapseSqlAdvancedDataSecurity** Cmdlet 可在工作區上啟用高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="48839-109">The **Enable-AzSynapseSqlAdvancedDataSecurity** cmdlet enables Advanced Data Security on a workspace.</span></span> <span data-ttu-id="48839-110">[高級資料安全性] 是一個整合的安全性套件，其中包含您工作區的資料分類、漏洞評估及高級威脅防護。</span><span class="sxs-lookup"><span data-stu-id="48839-110">Advanced Data Security is a unified security package that includes Data Classification, Vulnerability Assessment and Advanced Threat Protection for your workspace.</span></span> <span data-ttu-id="48839-111"> (會自動建立新的儲存空間帳戶來儲存漏洞評量。</span><span class="sxs-lookup"><span data-stu-id="48839-111">(A new storage account will automatically be created for saving vulnerability assessments.</span></span> <span data-ttu-id="48839-112">如果先前已針對此目的建立儲存空間帳戶，則會改為使用它) </span><span class="sxs-lookup"><span data-stu-id="48839-112">If a storage account was previously created for this purpose, it will be used instead)</span></span>

## <span data-ttu-id="48839-113">示例</span><span class="sxs-lookup"><span data-stu-id="48839-113">EXAMPLES</span></span>

### <span data-ttu-id="48839-114">範例1</span><span class="sxs-lookup"><span data-stu-id="48839-114">Example 1</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="48839-115">這個命令會啟用工作區高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="48839-115">This command enables workspace Advanced Data Security.</span></span>

### <span data-ttu-id="48839-116">範例2</span><span class="sxs-lookup"><span data-stu-id="48839-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Enable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="48839-117">這個命令會透過管線啟用工作區高級資料安全性。</span><span class="sxs-lookup"><span data-stu-id="48839-117">This command enables workspace Advanced Data Security through pipeline.</span></span>

### <span data-ttu-id="48839-118">範例3</span><span class="sxs-lookup"><span data-stu-id="48839-118">Example 3</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace -DoNotConfigureVulnerabilityAssessment
```

<span data-ttu-id="48839-119">這個命令可透過管線啟用工作區高級資料安全性，且不會自動啟用漏洞評估。</span><span class="sxs-lookup"><span data-stu-id="48839-119">This command enables workspace Advanced Data Security through pipeline and does not auto enable Vulnerability Assessment.</span></span>

## <span data-ttu-id="48839-120">參數</span><span class="sxs-lookup"><span data-stu-id="48839-120">PARAMETERS</span></span>

### <span data-ttu-id="48839-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48839-121">-AsJob</span></span>
<span data-ttu-id="48839-122">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="48839-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48839-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48839-123">-DefaultProfile</span></span>
<span data-ttu-id="48839-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="48839-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48839-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="48839-125">-DeploymentName</span></span>
<span data-ttu-id="48839-126">為高級資料安全性部署提供自訂名稱。</span><span class="sxs-lookup"><span data-stu-id="48839-126">Supply a custom name for Advanced Data Security deployment.</span></span>

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

### <span data-ttu-id="48839-127">-DoNotConfigureVulnerabilityAssessment</span><span class="sxs-lookup"><span data-stu-id="48839-127">-DoNotConfigureVulnerabilityAssessment</span></span>
<span data-ttu-id="48839-128">請勿自動啟用漏洞評估 (這不會建立儲存空間帳戶) 。</span><span class="sxs-lookup"><span data-stu-id="48839-128">Do not auto enable Vulnerability Assessment (This will not create a storage account).</span></span>

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

### <span data-ttu-id="48839-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48839-129">-InputObject</span></span>
<span data-ttu-id="48839-130">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="48839-130">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="48839-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48839-131">-ResourceGroupName</span></span>
<span data-ttu-id="48839-132">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="48839-132">Resource group name.</span></span>

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

### <span data-ttu-id="48839-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48839-133">-ResourceId</span></span>
<span data-ttu-id="48839-134">Synapse 工作區的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="48839-134">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="48839-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="48839-135">-WorkspaceName</span></span>
<span data-ttu-id="48839-136">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="48839-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="48839-137">-確認</span><span class="sxs-lookup"><span data-stu-id="48839-137">-Confirm</span></span>
<span data-ttu-id="48839-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48839-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48839-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48839-139">-WhatIf</span></span>
<span data-ttu-id="48839-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48839-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48839-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48839-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48839-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48839-142">CommonParameters</span></span>
<span data-ttu-id="48839-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48839-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48839-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="48839-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48839-145">輸入</span><span class="sxs-lookup"><span data-stu-id="48839-145">INPUTS</span></span>

### <span data-ttu-id="48839-146">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="48839-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="48839-147">輸出</span><span class="sxs-lookup"><span data-stu-id="48839-147">OUTPUTS</span></span>

### <span data-ttu-id="48839-148">WorkspaceAdvancedDataSecurityPolicy 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="48839-148">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="48839-149">筆記</span><span class="sxs-lookup"><span data-stu-id="48839-149">NOTES</span></span>

## <span data-ttu-id="48839-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="48839-150">RELATED LINKS</span></span>
