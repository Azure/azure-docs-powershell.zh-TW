---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: a76731c52de32f8b92ed244f82c6afd69bab32d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916326"
---
# <span data-ttu-id="b20fc-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b20fc-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="b20fc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b20fc-102">SYNOPSIS</span></span>
<span data-ttu-id="b20fc-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="b20fc-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="b20fc-104">語法</span><span class="sxs-lookup"><span data-stu-id="b20fc-104">SYNTAX</span></span>

### <span data-ttu-id="b20fc-105">SetBy以預設 (名稱) </span><span class="sxs-lookup"><span data-stu-id="b20fc-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-106">SetByLinked一起執行TimeName</span><span class="sxs-lookup"><span data-stu-id="b20fc-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-108">SetByLinked一起執行時ParentObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b20fc-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-110">SetByLinked一起執行TimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b20fc-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-111">SetBy一文集RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20fc-112">SetByLinked一起執行TimeObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b20fc-113">描述</span><span class="sxs-lookup"><span data-stu-id="b20fc-113">DESCRIPTION</span></span>
<span data-ttu-id="b20fc-114">**Set-AzSynapse RuntimeRuntime** Cmdlet 會更新與特定參數的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="b20fc-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="b20fc-115">例子</span><span class="sxs-lookup"><span data-stu-id="b20fc-115">EXAMPLES</span></span>

### <span data-ttu-id="b20fc-116">範例 1</span><span class="sxs-lookup"><span data-stu-id="b20fc-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="b20fc-117">Cmdlet 會更新名為"test-selfhost-ir"的整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="b20fc-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="b20fc-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="b20fc-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="b20fc-119">Cmdlet 會新增工作區以使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="b20fc-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="b20fc-120">使用 `-SharedIntegrationRuntimeResourceId` 參數時 `-Type` ，也必須包含。</span><span class="sxs-lookup"><span data-stu-id="b20fc-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="b20fc-121">請注意，執行 Cmdlet 之前，工作區需要獲得使用整合執行時間的許可權。</span><span class="sxs-lookup"><span data-stu-id="b20fc-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="b20fc-122">參數</span><span class="sxs-lookup"><span data-stu-id="b20fc-122">PARAMETERS</span></span>

### <span data-ttu-id="b20fc-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="b20fc-123">-AuthKey</span></span>
<span data-ttu-id="b20fc-124">自我託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="b20fc-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="b20fc-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="b20fc-126">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="b20fc-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="b20fc-127">-CatalogPricingTier</span></span>
<span data-ttu-id="b20fc-128">整合執行時間的目錄資料庫定價層級。</span><span class="sxs-lookup"><span data-stu-id="b20fc-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b20fc-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="b20fc-130">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="b20fc-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="b20fc-131">-DataFlowComputeType</span></span>
<span data-ttu-id="b20fc-132">會執行資料流程工作之資料流程組的計算類型。</span><span class="sxs-lookup"><span data-stu-id="b20fc-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="b20fc-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="b20fc-134">會執行資料流程工作之資料流程組的核心計數。</span><span class="sxs-lookup"><span data-stu-id="b20fc-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b20fc-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="b20fc-136">若要即時 (，) 資料流程組設定 ，即可執行資料流程工作。</span><span class="sxs-lookup"><span data-stu-id="b20fc-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-137">-DataProxy一起使用RuntimeName</span><span class="sxs-lookup"><span data-stu-id="b20fc-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="b20fc-138">用來Self-Hosted Proxy 的整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="b20fc-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="b20fc-140">在 Self-Hosted 與 Azure-SSIS 整合執行時間之間移動資料時，參照暫存資料存放區之 Azure Blob 儲存體連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="b20fc-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="b20fc-142">在 Self-Hosted 和 Azure-SSIS 整合執行時間之間移動資料時，要用於暫存資料存放區的路徑，未指定時，會使用預設容器。</span><span class="sxs-lookup"><span data-stu-id="b20fc-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b20fc-143">-DefaultProfile</span></span>
<span data-ttu-id="b20fc-144">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b20fc-145">-描述</span><span class="sxs-lookup"><span data-stu-id="b20fc-145">-Description</span></span>
<span data-ttu-id="b20fc-146">整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="b20fc-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="b20fc-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="b20fc-147">-Edition</span></span>
<span data-ttu-id="b20fc-148">SSIS 整合執行時間的版本可能是標準版或企業版，如果未指定，預設值為 Standard。</span><span class="sxs-lookup"><span data-stu-id="b20fc-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="b20fc-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="b20fc-150">SSIS 整合執行時間的快速自訂設定，可用於設定設定和協力廠商元件，而不需要自訂設定腳本。</span><span class="sxs-lookup"><span data-stu-id="b20fc-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-151">-強制</span><span class="sxs-lookup"><span data-stu-id="b20fc-151">-Force</span></span>
<span data-ttu-id="b20fc-152">請勿要求確認。</span><span class="sxs-lookup"><span data-stu-id="b20fc-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b20fc-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-153">-InputObject</span></span>
<span data-ttu-id="b20fc-154">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="b20fc-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b20fc-155">-LicenseType</span></span>
<span data-ttu-id="b20fc-156">您想要為 SSIS IR 選取授權類型。</span><span class="sxs-lookup"><span data-stu-id="b20fc-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="b20fc-157">有兩種類型：LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="b20fc-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="b20fc-158">如果您符合 Azure 混合式使用權益 (AHUB) ，請選取 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="b20fc-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="b20fc-159">如果沒有，請選取 LicenseIncluded。</span><span class="sxs-lookup"><span data-stu-id="b20fc-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-160">-位置</span><span class="sxs-lookup"><span data-stu-id="b20fc-160">-Location</span></span>
<span data-ttu-id="b20fc-161">整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="b20fc-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="b20fc-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="b20fc-163">受管理的專用整合執行時間每個節點的並存執行計數上限。</span><span class="sxs-lookup"><span data-stu-id="b20fc-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="b20fc-164">-Name</span></span>
<span data-ttu-id="b20fc-165">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="b20fc-166">-NodeCount</span></span>
<span data-ttu-id="b20fc-167">整合執行時間的目標節點計數。</span><span class="sxs-lookup"><span data-stu-id="b20fc-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="b20fc-168">-NodeSize</span></span>
<span data-ttu-id="b20fc-169">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="b20fc-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="b20fc-170">-PublicIP</span></span>
<span data-ttu-id="b20fc-171">整合執行時間將使用的靜態公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="b20fc-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b20fc-172">-ResourceGroupName</span></span>
<span data-ttu-id="b20fc-173">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b20fc-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b20fc-174">-ResourceId</span></span>
<span data-ttu-id="b20fc-175">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b20fc-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="b20fc-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="b20fc-177">包含自訂設定腳本的 Azure Blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="b20fc-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-178">-SharedSourceRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="b20fc-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="b20fc-179">共用自我託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b20fc-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-180">-子網</span><span class="sxs-lookup"><span data-stu-id="b20fc-180">-Subnet</span></span>
<span data-ttu-id="b20fc-181">VNet 中的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-182">-類型</span><span class="sxs-lookup"><span data-stu-id="b20fc-182">-Type</span></span>
<span data-ttu-id="b20fc-183">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="b20fc-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="b20fc-184">-VNetId</span></span>
<span data-ttu-id="b20fc-185">整合執行時間將加入的 VNet 識別碼。</span><span class="sxs-lookup"><span data-stu-id="b20fc-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b20fc-186">-WorkspaceName</span></span>
<span data-ttu-id="b20fc-187">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="b20fc-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b20fc-188">-WorkspaceObject</span></span>
<span data-ttu-id="b20fc-189">工作區輸入物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="b20fc-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b20fc-190">-確認</span><span class="sxs-lookup"><span data-stu-id="b20fc-190">-Confirm</span></span>
<span data-ttu-id="b20fc-191">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b20fc-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b20fc-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b20fc-192">-WhatIf</span></span>
<span data-ttu-id="b20fc-193">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b20fc-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b20fc-194">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b20fc-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b20fc-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20fc-195">CommonParameters</span></span>
<span data-ttu-id="b20fc-196">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b20fc-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20fc-197">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b20fc-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20fc-198">輸入</span><span class="sxs-lookup"><span data-stu-id="b20fc-198">INPUTS</span></span>

### <span data-ttu-id="b20fc-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b20fc-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="b20fc-200">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="b20fc-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b20fc-201">輸出</span><span class="sxs-lookup"><span data-stu-id="b20fc-201">OUTPUTS</span></span>

### <span data-ttu-id="b20fc-202">Microsoft.Azure.Commands.Synapse.Models.PS方格Runtime</span><span class="sxs-lookup"><span data-stu-id="b20fc-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b20fc-203">筆記</span><span class="sxs-lookup"><span data-stu-id="b20fc-203">NOTES</span></span>

## <span data-ttu-id="b20fc-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="b20fc-204">RELATED LINKS</span></span>
