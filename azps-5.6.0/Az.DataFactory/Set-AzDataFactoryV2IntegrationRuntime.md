---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 09b0ac3083a0440b6c229da6f45bf6412817b7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905157"
---
# <span data-ttu-id="46374-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="46374-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="46374-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46374-102">SYNOPSIS</span></span>
<span data-ttu-id="46374-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46374-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="46374-104">語法</span><span class="sxs-lookup"><span data-stu-id="46374-104">SYNTAX</span></span>

### <span data-ttu-id="46374-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="46374-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46374-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="46374-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46374-107">ByLinked方能RuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="46374-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46374-108">ByLinked方會RuntimeName</span><span class="sxs-lookup"><span data-stu-id="46374-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46374-109">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="46374-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46374-110">ByLinked方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="46374-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46374-111">描述</span><span class="sxs-lookup"><span data-stu-id="46374-111">DESCRIPTION</span></span>
<span data-ttu-id="46374-112">Cmdlet Set-AzDataFactoryV2IntegrationRuntime更新具有特定參數的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46374-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="46374-113">例子</span><span class="sxs-lookup"><span data-stu-id="46374-113">EXAMPLES</span></span>

### <span data-ttu-id="46374-114">範例 1：更新整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="46374-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="46374-115">Cmdlet 會更新名為"test-selfhost-ir"的整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="46374-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="46374-116">範例 2：共用自我託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46374-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="46374-117">Cmdlet 會新增 ADF 以使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="46374-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="46374-118">使用 `-SharedIntegrationRuntimeResourceId` 參數時 `-Type` ，也必須包含。</span><span class="sxs-lookup"><span data-stu-id="46374-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="46374-119">請注意，執行 Cmdlet 之前，必須授予資料工廠使用整合執行時間的許可權。</span><span class="sxs-lookup"><span data-stu-id="46374-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="46374-120">範例 3：將 Self-Hosted IR 設定為 ADF 中 Azure-SSIS IR 的 Proxy。</span><span class="sxs-lookup"><span data-stu-id="46374-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    PublicIPs                         : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="46374-121">Cmdlet 會更新 Azure-SSIS 整合執行時間，以使用自我託管整合執行時間做為資料 Proxy。</span><span class="sxs-lookup"><span data-stu-id="46374-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="46374-122">參數</span><span class="sxs-lookup"><span data-stu-id="46374-122">PARAMETERS</span></span>

### <span data-ttu-id="46374-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="46374-123">-AuthKey</span></span>
<span data-ttu-id="46374-124">自我託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="46374-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="46374-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="46374-126">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="46374-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="46374-127">-CatalogPricingTier</span></span>
<span data-ttu-id="46374-128">整合執行時間的目錄資料庫定價層級。</span><span class="sxs-lookup"><span data-stu-id="46374-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="46374-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="46374-130">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="46374-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="46374-131">-DataFactoryName</span></span>
<span data-ttu-id="46374-132">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="46374-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46374-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="46374-133">-DataFlowComputeType</span></span>
<span data-ttu-id="46374-134">會執行資料流程工作之資料流程組的計算類型。</span><span class="sxs-lookup"><span data-stu-id="46374-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="46374-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="46374-136">會執行資料流程工作之資料流程組的核心計數。</span><span class="sxs-lookup"><span data-stu-id="46374-136">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="46374-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="46374-138">若要即時 (，) 資料流程組設定 ，即可執行資料流程工作。</span><span class="sxs-lookup"><span data-stu-id="46374-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-139">-DataProxy一起使用RuntimeName</span><span class="sxs-lookup"><span data-stu-id="46374-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="46374-140">用來Self-Hosted Proxy 的整合執行時間名稱</span><span class="sxs-lookup"><span data-stu-id="46374-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="46374-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="46374-142">在 Self-Hosted 與 Azure-SSIS 整合執行時間之間移動資料時，參照暫存資料存放區之 Azure Blob 儲存連結服務名稱</span><span class="sxs-lookup"><span data-stu-id="46374-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="46374-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="46374-144">在 Self-Hosted 和 Azure-SSIS 整合執行時間之間移動資料時，要用於暫存資料存放區的路徑，未指定時，會使用預設容器</span><span class="sxs-lookup"><span data-stu-id="46374-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46374-145">-DefaultProfile</span></span>
<span data-ttu-id="46374-146">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="46374-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46374-147">-描述</span><span class="sxs-lookup"><span data-stu-id="46374-147">-Description</span></span>
<span data-ttu-id="46374-148">整合執行時間描述。</span><span class="sxs-lookup"><span data-stu-id="46374-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="46374-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="46374-149">-Edition</span></span>
<span data-ttu-id="46374-150">SSIS 整合執行時間的版本可能是標準版或企業版，如果未指定，預設值為 Standard。</span><span class="sxs-lookup"><span data-stu-id="46374-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-151">-強制</span><span class="sxs-lookup"><span data-stu-id="46374-151">-Force</span></span>
<span data-ttu-id="46374-152">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="46374-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="46374-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46374-153">-InputObject</span></span>
<span data-ttu-id="46374-154">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="46374-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46374-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="46374-155">-LicenseType</span></span>
<span data-ttu-id="46374-156">您想要為 SSIS IR 選取授權類型。</span><span class="sxs-lookup"><span data-stu-id="46374-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="46374-157">有兩種類型：LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="46374-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="46374-158">如果您符合 Azure 混合式使用權益 (AHUB) ，請選取 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="46374-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="46374-159">如果沒有，請選取 LicenseIncluded。</span><span class="sxs-lookup"><span data-stu-id="46374-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-160">-位置</span><span class="sxs-lookup"><span data-stu-id="46374-160">-Location</span></span>
<span data-ttu-id="46374-161">整合執行時間位置。</span><span class="sxs-lookup"><span data-stu-id="46374-161">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="46374-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="46374-163">受管理的專用整合執行時間每個節點的並存執行計數上限。</span><span class="sxs-lookup"><span data-stu-id="46374-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-164">-名稱</span><span class="sxs-lookup"><span data-stu-id="46374-164">-Name</span></span>
<span data-ttu-id="46374-165">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="46374-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46374-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="46374-166">-NodeCount</span></span>
<span data-ttu-id="46374-167">整合執行時間的目標節點計數。</span><span class="sxs-lookup"><span data-stu-id="46374-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="46374-168">-NodeSize</span></span>
<span data-ttu-id="46374-169">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="46374-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-170">-公用 IP</span><span class="sxs-lookup"><span data-stu-id="46374-170">-PublicIPs</span></span>
<span data-ttu-id="46374-171">整合執行時間將使用的靜態公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="46374-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46374-172">-ResourceGroupName</span></span>
<span data-ttu-id="46374-173">資源組名。</span><span class="sxs-lookup"><span data-stu-id="46374-173">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46374-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46374-174">-ResourceId</span></span>
<span data-ttu-id="46374-175">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46374-175">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46374-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="46374-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="46374-177">包含自訂設定腳本的 Azure Blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="46374-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-178">-SharedSourceRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="46374-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="46374-179">共用自我託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="46374-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-180">-子網</span><span class="sxs-lookup"><span data-stu-id="46374-180">-Subnet</span></span>
<span data-ttu-id="46374-181">VNet 中的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="46374-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-182">-類型</span><span class="sxs-lookup"><span data-stu-id="46374-182">-Type</span></span>
<span data-ttu-id="46374-183">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="46374-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="46374-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="46374-184">-VNetId</span></span>
<span data-ttu-id="46374-185">整合執行時間加入的 VNet 識別碼。</span><span class="sxs-lookup"><span data-stu-id="46374-185">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46374-186">-確認</span><span class="sxs-lookup"><span data-stu-id="46374-186">-Confirm</span></span>
<span data-ttu-id="46374-187">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="46374-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46374-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46374-188">-WhatIf</span></span>
<span data-ttu-id="46374-189">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46374-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="46374-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46374-190">CommonParameters</span></span>
<span data-ttu-id="46374-191">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46374-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46374-192">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="46374-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46374-193">輸入</span><span class="sxs-lookup"><span data-stu-id="46374-193">INPUTS</span></span>

### <span data-ttu-id="46374-194">System.String</span><span class="sxs-lookup"><span data-stu-id="46374-194">System.String</span></span>

### <span data-ttu-id="46374-195">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="46374-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="46374-196">輸出</span><span class="sxs-lookup"><span data-stu-id="46374-196">OUTPUTS</span></span>

### <span data-ttu-id="46374-197">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="46374-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="46374-198">筆記</span><span class="sxs-lookup"><span data-stu-id="46374-198">NOTES</span></span>

## <span data-ttu-id="46374-199">相關連結</span><span class="sxs-lookup"><span data-stu-id="46374-199">RELATED LINKS</span></span>

[<span data-ttu-id="46374-200">Set-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="46374-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
