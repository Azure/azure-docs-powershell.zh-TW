---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137194"
---
# <span data-ttu-id="ed984-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ed984-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="ed984-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed984-102">SYNOPSIS</span></span>
<span data-ttu-id="ed984-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ed984-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="ed984-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed984-104">SYNTAX</span></span>

### <span data-ttu-id="ed984-105">SetByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="ed984-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="ed984-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ed984-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed984-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="ed984-107">SetByParentObject</span></span>
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

### <span data-ttu-id="ed984-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="ed984-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed984-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed984-109">SetByResourceId</span></span>
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

### <span data-ttu-id="ed984-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="ed984-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed984-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ed984-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="ed984-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ed984-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed984-113">說明</span><span class="sxs-lookup"><span data-stu-id="ed984-113">DESCRIPTION</span></span>
<span data-ttu-id="ed984-114">**AzSynapseIntegrationRuntime** Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ed984-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="ed984-115">示例</span><span class="sxs-lookup"><span data-stu-id="ed984-115">EXAMPLES</span></span>

### <span data-ttu-id="ed984-116">範例1</span><span class="sxs-lookup"><span data-stu-id="ed984-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="ed984-117">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="ed984-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="ed984-118">範例2</span><span class="sxs-lookup"><span data-stu-id="ed984-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="ed984-119">此 Cmdlet 會新增工作區以使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ed984-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="ed984-120">使用 `-SharedIntegrationRuntimeResourceId` 參數時， `-Type` 也必須包含。</span><span class="sxs-lookup"><span data-stu-id="ed984-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="ed984-121">請注意，在執行 Cmdlet 之前，必須先將工作區的許可權授與使用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ed984-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="ed984-122">參數</span><span class="sxs-lookup"><span data-stu-id="ed984-122">PARAMETERS</span></span>

### <span data-ttu-id="ed984-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="ed984-123">-AuthKey</span></span>
<span data-ttu-id="ed984-124">自託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="ed984-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ed984-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="ed984-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="ed984-126">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="ed984-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="ed984-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="ed984-127">-CatalogPricingTier</span></span>
<span data-ttu-id="ed984-128">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="ed984-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="ed984-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed984-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="ed984-130">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="ed984-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="ed984-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="ed984-131">-DataFlowComputeType</span></span>
<span data-ttu-id="ed984-132">將執行資料流程程作業之資料流程群集的計算類型。</span><span class="sxs-lookup"><span data-stu-id="ed984-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="ed984-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="ed984-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="ed984-134">將執行資料流程程作業之資料流程群集的核心計數。</span><span class="sxs-lookup"><span data-stu-id="ed984-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="ed984-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ed984-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="ed984-136">即時 () 設定將會執行資料流程程作業的資料流程群集的實際時間（分鐘）。</span><span class="sxs-lookup"><span data-stu-id="ed984-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="ed984-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ed984-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="ed984-138">用作 proxy 的 Self-Hosted 整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="ed984-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="ed984-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="ed984-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="ed984-140">Azure Blob 儲存連結的服務名稱，參照要在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時使用的暫存資料存放區。</span><span class="sxs-lookup"><span data-stu-id="ed984-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="ed984-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="ed984-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="ed984-142">在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時，要使用暫存資料存放區中的路徑，如果未指定，則會使用預設容器。</span><span class="sxs-lookup"><span data-stu-id="ed984-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="ed984-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed984-143">-DefaultProfile</span></span>
<span data-ttu-id="ed984-144">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed984-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed984-145">-描述</span><span class="sxs-lookup"><span data-stu-id="ed984-145">-Description</span></span>
<span data-ttu-id="ed984-146">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="ed984-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="ed984-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="ed984-147">-Edition</span></span>
<span data-ttu-id="ed984-148">可能是標準或企業的 SSIS 整合執行時間版本，預設為標準（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="ed984-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="ed984-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="ed984-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="ed984-150">SSIS 整合執行時間的快速自訂設定，可用於設定設定和協力廠商元件（不含自訂安裝程式腳本）。</span><span class="sxs-lookup"><span data-stu-id="ed984-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="ed984-151">-Force</span><span class="sxs-lookup"><span data-stu-id="ed984-151">-Force</span></span>
<span data-ttu-id="ed984-152">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="ed984-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ed984-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed984-153">-InputObject</span></span>
<span data-ttu-id="ed984-154">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="ed984-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="ed984-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ed984-155">-LicenseType</span></span>
<span data-ttu-id="ed984-156">您要為 SSIS IR 選取的授權類型。</span><span class="sxs-lookup"><span data-stu-id="ed984-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="ed984-157">有兩種類型： LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="ed984-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="ed984-158">如果您符合 Azure 混合式使用優惠 (AHUB) 定價，請選取 [BasePrice]。</span><span class="sxs-lookup"><span data-stu-id="ed984-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="ed984-159">如果不是，請選取 [LicenseIncluded]。</span><span class="sxs-lookup"><span data-stu-id="ed984-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="ed984-160">-位置</span><span class="sxs-lookup"><span data-stu-id="ed984-160">-Location</span></span>
<span data-ttu-id="ed984-161">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="ed984-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="ed984-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="ed984-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="ed984-163">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="ed984-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="ed984-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed984-164">-Name</span></span>
<span data-ttu-id="ed984-165">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="ed984-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="ed984-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ed984-166">-NodeCount</span></span>
<span data-ttu-id="ed984-167">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="ed984-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="ed984-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="ed984-168">-NodeSize</span></span>
<span data-ttu-id="ed984-169">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="ed984-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="ed984-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="ed984-170">-PublicIP</span></span>
<span data-ttu-id="ed984-171">整合執行時間將使用的靜態公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ed984-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="ed984-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed984-172">-ResourceGroupName</span></span>
<span data-ttu-id="ed984-173">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ed984-173">Resource group name.</span></span>

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

### <span data-ttu-id="ed984-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed984-174">-ResourceId</span></span>
<span data-ttu-id="ed984-175">Synapse 整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed984-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ed984-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="ed984-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="ed984-177">包含自訂安裝程式腳本之 Azure blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="ed984-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="ed984-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="ed984-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="ed984-179">共用的自託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed984-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="ed984-180">-子網</span><span class="sxs-lookup"><span data-stu-id="ed984-180">-Subnet</span></span>
<span data-ttu-id="ed984-181">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed984-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="ed984-182">-類型</span><span class="sxs-lookup"><span data-stu-id="ed984-182">-Type</span></span>
<span data-ttu-id="ed984-183">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="ed984-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="ed984-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="ed984-184">-VNetId</span></span>
<span data-ttu-id="ed984-185">整合執行時間將加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="ed984-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="ed984-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ed984-186">-WorkspaceName</span></span>
<span data-ttu-id="ed984-187">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed984-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ed984-188">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ed984-188">-WorkspaceObject</span></span>
<span data-ttu-id="ed984-189">工作區輸入物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="ed984-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ed984-190">-確認</span><span class="sxs-lookup"><span data-stu-id="ed984-190">-Confirm</span></span>
<span data-ttu-id="ed984-191">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed984-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed984-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed984-192">-WhatIf</span></span>
<span data-ttu-id="ed984-193">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed984-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed984-194">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed984-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed984-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed984-195">CommonParameters</span></span>
<span data-ttu-id="ed984-196">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed984-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed984-197">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ed984-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed984-198">輸入</span><span class="sxs-lookup"><span data-stu-id="ed984-198">INPUTS</span></span>

### <span data-ttu-id="ed984-199">PSSynapseWorkspace 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ed984-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ed984-200">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ed984-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ed984-201">輸出</span><span class="sxs-lookup"><span data-stu-id="ed984-201">OUTPUTS</span></span>

### <span data-ttu-id="ed984-202">PSIntegrationRuntime 中的 Synapse。</span><span class="sxs-lookup"><span data-stu-id="ed984-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ed984-203">筆記</span><span class="sxs-lookup"><span data-stu-id="ed984-203">NOTES</span></span>

## <span data-ttu-id="ed984-204">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed984-204">RELATED LINKS</span></span>
