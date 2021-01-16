---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276363"
---
# <span data-ttu-id="006f5-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="006f5-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="006f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="006f5-102">SYNOPSIS</span></span>
<span data-ttu-id="006f5-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="006f5-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="006f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="006f5-104">SYNTAX</span></span>

### <span data-ttu-id="006f5-105">SetByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="006f5-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="006f5-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="006f5-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006f5-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="006f5-107">SetByParentObject</span></span>
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

### <span data-ttu-id="006f5-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="006f5-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006f5-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="006f5-109">SetByResourceId</span></span>
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

### <span data-ttu-id="006f5-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="006f5-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="006f5-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="006f5-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="006f5-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="006f5-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="006f5-113">說明</span><span class="sxs-lookup"><span data-stu-id="006f5-113">DESCRIPTION</span></span>
<span data-ttu-id="006f5-114">**AzSynapseIntegrationRuntime** Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="006f5-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="006f5-115">示例</span><span class="sxs-lookup"><span data-stu-id="006f5-115">EXAMPLES</span></span>

### <span data-ttu-id="006f5-116">範例1</span><span class="sxs-lookup"><span data-stu-id="006f5-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="006f5-117">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="006f5-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="006f5-118">範例2</span><span class="sxs-lookup"><span data-stu-id="006f5-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="006f5-119">此 Cmdlet 會新增工作區以使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="006f5-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="006f5-120">使用 `-SharedIntegrationRuntimeResourceId` 參數時， `-Type` 也必須包含。</span><span class="sxs-lookup"><span data-stu-id="006f5-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="006f5-121">請注意，在執行 Cmdlet 之前，必須先將工作區的許可權授與使用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="006f5-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="006f5-122">參數</span><span class="sxs-lookup"><span data-stu-id="006f5-122">PARAMETERS</span></span>

### <span data-ttu-id="006f5-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="006f5-123">-AuthKey</span></span>
<span data-ttu-id="006f5-124">自託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="006f5-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="006f5-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="006f5-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="006f5-126">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="006f5-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="006f5-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="006f5-127">-CatalogPricingTier</span></span>
<span data-ttu-id="006f5-128">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="006f5-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="006f5-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="006f5-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="006f5-130">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="006f5-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="006f5-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="006f5-131">-DataFlowComputeType</span></span>
<span data-ttu-id="006f5-132">將執行資料流程程作業之資料流程群集的計算類型。</span><span class="sxs-lookup"><span data-stu-id="006f5-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="006f5-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="006f5-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="006f5-134">將執行資料流程程作業之資料流程群集的核心計數。</span><span class="sxs-lookup"><span data-stu-id="006f5-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="006f5-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="006f5-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="006f5-136">即時 () 設定將會執行資料流程程作業的資料流程群集的實際時間（分鐘）。</span><span class="sxs-lookup"><span data-stu-id="006f5-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="006f5-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="006f5-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="006f5-138">用作 proxy 的 Self-Hosted 整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="006f5-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="006f5-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="006f5-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="006f5-140">Azure Blob 儲存連結的服務名稱，參照要在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時使用的暫存資料存放區。</span><span class="sxs-lookup"><span data-stu-id="006f5-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="006f5-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="006f5-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="006f5-142">在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時，要使用暫存資料存放區中的路徑，如果未指定，則會使用預設容器。</span><span class="sxs-lookup"><span data-stu-id="006f5-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="006f5-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006f5-143">-DefaultProfile</span></span>
<span data-ttu-id="006f5-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="006f5-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006f5-145">-描述</span><span class="sxs-lookup"><span data-stu-id="006f5-145">-Description</span></span>
<span data-ttu-id="006f5-146">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="006f5-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="006f5-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="006f5-147">-Edition</span></span>
<span data-ttu-id="006f5-148">可能是標準或企業的 SSIS 整合執行時間版本，預設為標準（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="006f5-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="006f5-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="006f5-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="006f5-150">SSIS 整合執行時間的快速自訂設定，可用於設定設定和協力廠商元件（不含自訂安裝程式腳本）。</span><span class="sxs-lookup"><span data-stu-id="006f5-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="006f5-151">-Force</span><span class="sxs-lookup"><span data-stu-id="006f5-151">-Force</span></span>
<span data-ttu-id="006f5-152">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="006f5-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="006f5-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="006f5-153">-InputObject</span></span>
<span data-ttu-id="006f5-154">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="006f5-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="006f5-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="006f5-155">-LicenseType</span></span>
<span data-ttu-id="006f5-156">您要為 SSIS IR 選取的授權類型。</span><span class="sxs-lookup"><span data-stu-id="006f5-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="006f5-157">有兩種類型： LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="006f5-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="006f5-158">如果您符合 Azure 混合式使用優惠 (AHUB) 定價，請選取 [BasePrice]。</span><span class="sxs-lookup"><span data-stu-id="006f5-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="006f5-159">如果不是，請選取 [LicenseIncluded]。</span><span class="sxs-lookup"><span data-stu-id="006f5-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="006f5-160">-位置</span><span class="sxs-lookup"><span data-stu-id="006f5-160">-Location</span></span>
<span data-ttu-id="006f5-161">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="006f5-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="006f5-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="006f5-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="006f5-163">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="006f5-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="006f5-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="006f5-164">-Name</span></span>
<span data-ttu-id="006f5-165">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="006f5-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="006f5-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="006f5-166">-NodeCount</span></span>
<span data-ttu-id="006f5-167">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="006f5-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="006f5-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="006f5-168">-NodeSize</span></span>
<span data-ttu-id="006f5-169">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="006f5-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="006f5-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="006f5-170">-PublicIP</span></span>
<span data-ttu-id="006f5-171">整合執行時間將使用的靜態公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="006f5-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="006f5-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006f5-172">-ResourceGroupName</span></span>
<span data-ttu-id="006f5-173">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="006f5-173">Resource group name.</span></span>

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

### <span data-ttu-id="006f5-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="006f5-174">-ResourceId</span></span>
<span data-ttu-id="006f5-175">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="006f5-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="006f5-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="006f5-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="006f5-177">包含自訂安裝程式腳本之 Azure blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="006f5-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="006f5-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="006f5-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="006f5-179">共用的自託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="006f5-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="006f5-180">-子網</span><span class="sxs-lookup"><span data-stu-id="006f5-180">-Subnet</span></span>
<span data-ttu-id="006f5-181">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="006f5-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="006f5-182">-類型</span><span class="sxs-lookup"><span data-stu-id="006f5-182">-Type</span></span>
<span data-ttu-id="006f5-183">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="006f5-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="006f5-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="006f5-184">-VNetId</span></span>
<span data-ttu-id="006f5-185">整合執行時間將加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="006f5-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="006f5-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="006f5-186">-WorkspaceName</span></span>
<span data-ttu-id="006f5-187">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="006f5-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="006f5-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="006f5-188">-WorkspaceObject</span></span>
<span data-ttu-id="006f5-189">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="006f5-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="006f5-190">-確認</span><span class="sxs-lookup"><span data-stu-id="006f5-190">-Confirm</span></span>
<span data-ttu-id="006f5-191">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="006f5-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="006f5-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="006f5-192">-WhatIf</span></span>
<span data-ttu-id="006f5-193">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="006f5-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="006f5-194">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="006f5-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="006f5-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006f5-195">CommonParameters</span></span>
<span data-ttu-id="006f5-196">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="006f5-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006f5-197">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="006f5-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006f5-198">輸入</span><span class="sxs-lookup"><span data-stu-id="006f5-198">INPUTS</span></span>

### <span data-ttu-id="006f5-199">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="006f5-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="006f5-200">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="006f5-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="006f5-201">輸出</span><span class="sxs-lookup"><span data-stu-id="006f5-201">OUTPUTS</span></span>

### <span data-ttu-id="006f5-202">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="006f5-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="006f5-203">筆記</span><span class="sxs-lookup"><span data-stu-id="006f5-203">NOTES</span></span>

## <span data-ttu-id="006f5-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="006f5-204">RELATED LINKS</span></span>
