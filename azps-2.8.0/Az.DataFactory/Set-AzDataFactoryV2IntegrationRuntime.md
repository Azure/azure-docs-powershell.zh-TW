---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612908"
---
# <span data-ttu-id="d4e70-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4e70-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d4e70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4e70-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e70-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d4e70-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="d4e70-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4e70-104">SYNTAX</span></span>

### <span data-ttu-id="d4e70-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="d4e70-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e70-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e70-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e70-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e70-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d4e70-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e70-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d4e70-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e70-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d4e70-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e70-111">說明</span><span class="sxs-lookup"><span data-stu-id="d4e70-111">DESCRIPTION</span></span>
<span data-ttu-id="d4e70-112">Set-AzDataFactoryV2IntegrationRuntime Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d4e70-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="d4e70-113">示例</span><span class="sxs-lookup"><span data-stu-id="d4e70-113">EXAMPLES</span></span>

### <span data-ttu-id="d4e70-114">範例1：更新整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="d4e70-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="d4e70-115">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="d4e70-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="d4e70-116">範例2：共用自託管的集成執行時間。</span><span class="sxs-lookup"><span data-stu-id="d4e70-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="d4e70-117">此 Cmdlet 會將 ADF 新增到使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d4e70-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="d4e70-118">使用 `-SharedIntegrationRuntimeResourceId` 參數時， `-Type` 也必須包含。</span><span class="sxs-lookup"><span data-stu-id="d4e70-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="d4e70-119">請注意，在執行 Cmdlet 前，資料工廠需要獲得使用整合執行時間的許可權。</span><span class="sxs-lookup"><span data-stu-id="d4e70-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="d4e70-120">範例3：將 Self-Hosted 紅外設定為在 ADF 中使用 Azure-SSIS 紅外的 proxy。</span><span class="sxs-lookup"><span data-stu-id="d4e70-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="d4e70-121">Cmdlet 會更新 Azure SSIS 整合執行時間，以使用自託管整合執行時間作為資料 proxy。</span><span class="sxs-lookup"><span data-stu-id="d4e70-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="d4e70-122">參數</span><span class="sxs-lookup"><span data-stu-id="d4e70-122">PARAMETERS</span></span>

### <span data-ttu-id="d4e70-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="d4e70-123">-AuthKey</span></span>
<span data-ttu-id="d4e70-124">自託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="d4e70-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="d4e70-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="d4e70-126">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="d4e70-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="d4e70-127">-CatalogPricingTier</span></span>
<span data-ttu-id="d4e70-128">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="d4e70-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4e70-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="d4e70-130">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="d4e70-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d4e70-131">-DataFactoryName</span></span>
<span data-ttu-id="d4e70-132">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e70-132">The data factory name.</span></span>

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

### <span data-ttu-id="d4e70-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="d4e70-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="d4e70-134">用作 proxy 的 Self-Hosted 整合執行時間名稱</span><span class="sxs-lookup"><span data-stu-id="d4e70-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="d4e70-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="d4e70-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="d4e70-136">Azure Blob 儲存連結的服務名稱，參照要在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時使用的暫存資料存放區</span><span class="sxs-lookup"><span data-stu-id="d4e70-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="d4e70-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="d4e70-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="d4e70-138">在 Self-Hosted 與 Azure SSIS 整合執行時間之間移動資料時，要使用的暫存資料存放區中的路徑（如果未指定，則會使用預設容器）</span><span class="sxs-lookup"><span data-stu-id="d4e70-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="d4e70-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e70-139">-DefaultProfile</span></span>
<span data-ttu-id="d4e70-140">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4e70-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4e70-141">-描述</span><span class="sxs-lookup"><span data-stu-id="d4e70-141">-Description</span></span>
<span data-ttu-id="d4e70-142">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="d4e70-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="d4e70-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="d4e70-143">-Edition</span></span>
<span data-ttu-id="d4e70-144">可能是標準或企業的 SSIS 整合執行時間版本，預設為標準（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="d4e70-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="d4e70-145">-Force</span><span class="sxs-lookup"><span data-stu-id="d4e70-145">-Force</span></span>
<span data-ttu-id="d4e70-146">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4e70-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d4e70-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4e70-147">-InputObject</span></span>
<span data-ttu-id="d4e70-148">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="d4e70-148">The integration runtime object.</span></span>

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

### <span data-ttu-id="d4e70-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d4e70-149">-LicenseType</span></span>
<span data-ttu-id="d4e70-150">您要為 SSIS IR 選取的授權類型。</span><span class="sxs-lookup"><span data-stu-id="d4e70-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="d4e70-151">有兩種類型： LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="d4e70-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="d4e70-152">如果您符合 Azure 混合式使用優惠 (AHUB) 定價，請選取 [BasePrice]。</span><span class="sxs-lookup"><span data-stu-id="d4e70-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="d4e70-153">如果不是，請選取 [LicenseIncluded]。</span><span class="sxs-lookup"><span data-stu-id="d4e70-153">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="d4e70-154">-位置</span><span class="sxs-lookup"><span data-stu-id="d4e70-154">-Location</span></span>
<span data-ttu-id="d4e70-155">整合執行時間的位置。</span><span class="sxs-lookup"><span data-stu-id="d4e70-155">The integration runtime location.</span></span>

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

### <span data-ttu-id="d4e70-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="d4e70-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="d4e70-157">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="d4e70-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-158">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4e70-158">-Name</span></span>
<span data-ttu-id="d4e70-159">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e70-159">The integration runtime name.</span></span>

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

### <span data-ttu-id="d4e70-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d4e70-160">-NodeCount</span></span>
<span data-ttu-id="d4e70-161">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="d4e70-161">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="d4e70-162">-NodeSize</span></span>
<span data-ttu-id="d4e70-163">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="d4e70-163">The integration runtime node size.</span></span>

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

### <span data-ttu-id="d4e70-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e70-164">-ResourceGroupName</span></span>
<span data-ttu-id="d4e70-165">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e70-165">The resource group name.</span></span>

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

### <span data-ttu-id="d4e70-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e70-166">-ResourceId</span></span>
<span data-ttu-id="d4e70-167">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4e70-167">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d4e70-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="d4e70-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="d4e70-169">包含自訂安裝程式腳本之 Azure blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="d4e70-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="d4e70-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="d4e70-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="d4e70-171">共用的自託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4e70-171">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="d4e70-172">-子網</span><span class="sxs-lookup"><span data-stu-id="d4e70-172">-Subnet</span></span>
<span data-ttu-id="d4e70-173">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4e70-173">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="d4e70-174">-類型</span><span class="sxs-lookup"><span data-stu-id="d4e70-174">-Type</span></span>
<span data-ttu-id="d4e70-175">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="d4e70-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="d4e70-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="d4e70-176">-VNetId</span></span>
<span data-ttu-id="d4e70-177">整合執行時間加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="d4e70-177">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="d4e70-178">-確認</span><span class="sxs-lookup"><span data-stu-id="d4e70-178">-Confirm</span></span>
<span data-ttu-id="d4e70-179">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4e70-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e70-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e70-180">-WhatIf</span></span>
<span data-ttu-id="d4e70-181">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4e70-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d4e70-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e70-182">CommonParameters</span></span>
<span data-ttu-id="d4e70-183">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4e70-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e70-184">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4e70-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e70-185">輸入</span><span class="sxs-lookup"><span data-stu-id="d4e70-185">INPUTS</span></span>

### <span data-ttu-id="d4e70-186">System.object</span><span class="sxs-lookup"><span data-stu-id="d4e70-186">System.String</span></span>

### <span data-ttu-id="d4e70-187">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d4e70-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d4e70-188">輸出</span><span class="sxs-lookup"><span data-stu-id="d4e70-188">OUTPUTS</span></span>

### <span data-ttu-id="d4e70-189">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d4e70-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d4e70-190">筆記</span><span class="sxs-lookup"><span data-stu-id="d4e70-190">NOTES</span></span>

## <span data-ttu-id="d4e70-191">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4e70-191">RELATED LINKS</span></span>

[<span data-ttu-id="d4e70-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d4e70-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
