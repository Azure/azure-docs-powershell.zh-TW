---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788102"
---
# <span data-ttu-id="4d897-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d897-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4d897-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d897-102">SYNOPSIS</span></span>
<span data-ttu-id="4d897-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4d897-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="4d897-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d897-104">SYNTAX</span></span>

### <span data-ttu-id="4d897-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="4d897-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d897-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4d897-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d897-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="4d897-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d897-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="4d897-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d897-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d897-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d897-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4d897-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d897-111">說明</span><span class="sxs-lookup"><span data-stu-id="4d897-111">DESCRIPTION</span></span>
<span data-ttu-id="4d897-112">Set-AzDataFactoryV2IntegrationRuntime Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4d897-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="4d897-113">示例</span><span class="sxs-lookup"><span data-stu-id="4d897-113">EXAMPLES</span></span>

### <span data-ttu-id="4d897-114">範例1：更新整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="4d897-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="4d897-115">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="4d897-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="4d897-116">範例2：共用自託管的集成執行時間。</span><span class="sxs-lookup"><span data-stu-id="4d897-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="4d897-117">此 Cmdlet 會將 ADF 新增到使用共用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4d897-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="4d897-118">使用 `-SharedIntegrationRuntimeResourceId` 參數時， `-Type` 也必須包含。</span><span class="sxs-lookup"><span data-stu-id="4d897-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="4d897-119">請注意，在執行 Cmdlet 前，資料工廠需要獲得使用整合執行時間的許可權。</span><span class="sxs-lookup"><span data-stu-id="4d897-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="4d897-120">參數</span><span class="sxs-lookup"><span data-stu-id="4d897-120">PARAMETERS</span></span>

### <span data-ttu-id="4d897-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="4d897-121">-AuthKey</span></span>
<span data-ttu-id="4d897-122">自託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="4d897-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="4d897-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="4d897-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="4d897-124">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="4d897-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="4d897-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="4d897-125">-CatalogPricingTier</span></span>
<span data-ttu-id="4d897-126">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="4d897-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="4d897-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4d897-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="4d897-128">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="4d897-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="4d897-129">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4d897-129">-DataFactoryName</span></span>
<span data-ttu-id="4d897-130">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4d897-130">The data factory name.</span></span>

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

### <span data-ttu-id="4d897-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d897-131">-DefaultProfile</span></span>
<span data-ttu-id="4d897-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4d897-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d897-133">-描述</span><span class="sxs-lookup"><span data-stu-id="4d897-133">-Description</span></span>
<span data-ttu-id="4d897-134">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="4d897-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="4d897-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="4d897-135">-Edition</span></span>
<span data-ttu-id="4d897-136">可能是標準或企業的 SSIS 整合執行時間版本，預設為標準（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="4d897-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="4d897-137">-Force</span><span class="sxs-lookup"><span data-stu-id="4d897-137">-Force</span></span>
<span data-ttu-id="4d897-138">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d897-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4d897-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d897-139">-InputObject</span></span>
<span data-ttu-id="4d897-140">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="4d897-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="4d897-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4d897-141">-LicenseType</span></span>
<span data-ttu-id="4d897-142">您要為 SSIS IR 選取的授權類型。</span><span class="sxs-lookup"><span data-stu-id="4d897-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="4d897-143">有兩種類型： LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="4d897-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="4d897-144">如果您符合 Azure 混合式使用優惠 (AHUB) 定價，請選取 [BasePrice]。</span><span class="sxs-lookup"><span data-stu-id="4d897-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="4d897-145">如果不是，請選取 [LicenseIncluded]。</span><span class="sxs-lookup"><span data-stu-id="4d897-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="4d897-146">-位置</span><span class="sxs-lookup"><span data-stu-id="4d897-146">-Location</span></span>
<span data-ttu-id="4d897-147">整合執行時間的位置。</span><span class="sxs-lookup"><span data-stu-id="4d897-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="4d897-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="4d897-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="4d897-149">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="4d897-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="4d897-150">-名稱</span><span class="sxs-lookup"><span data-stu-id="4d897-150">-Name</span></span>
<span data-ttu-id="4d897-151">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="4d897-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="4d897-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="4d897-152">-NodeCount</span></span>
<span data-ttu-id="4d897-153">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="4d897-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="4d897-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="4d897-154">-NodeSize</span></span>
<span data-ttu-id="4d897-155">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="4d897-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="4d897-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d897-156">-ResourceGroupName</span></span>
<span data-ttu-id="4d897-157">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d897-157">The resource group name.</span></span>

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

### <span data-ttu-id="4d897-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d897-158">-ResourceId</span></span>
<span data-ttu-id="4d897-159">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d897-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4d897-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="4d897-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="4d897-161">包含自訂安裝程式腳本之 Azure blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="4d897-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="4d897-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="4d897-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="4d897-163">共用的自託管整合執行時間的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d897-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="4d897-164">-子網</span><span class="sxs-lookup"><span data-stu-id="4d897-164">-Subnet</span></span>
<span data-ttu-id="4d897-165">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d897-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="4d897-166">-類型</span><span class="sxs-lookup"><span data-stu-id="4d897-166">-Type</span></span>
<span data-ttu-id="4d897-167">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="4d897-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="4d897-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="4d897-168">-VNetId</span></span>
<span data-ttu-id="4d897-169">整合執行時間加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="4d897-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="4d897-170">-確認</span><span class="sxs-lookup"><span data-stu-id="4d897-170">-Confirm</span></span>
<span data-ttu-id="4d897-171">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4d897-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d897-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d897-172">-WhatIf</span></span>
<span data-ttu-id="4d897-173">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4d897-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4d897-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d897-174">CommonParameters</span></span>
<span data-ttu-id="4d897-175">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d897-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d897-176">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d897-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d897-177">輸入</span><span class="sxs-lookup"><span data-stu-id="4d897-177">INPUTS</span></span>

### <span data-ttu-id="4d897-178">System.object</span><span class="sxs-lookup"><span data-stu-id="4d897-178">System.String</span></span>

### <span data-ttu-id="4d897-179">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4d897-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d897-180">輸出</span><span class="sxs-lookup"><span data-stu-id="4d897-180">OUTPUTS</span></span>

### <span data-ttu-id="4d897-181">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4d897-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4d897-182">筆記</span><span class="sxs-lookup"><span data-stu-id="4d897-182">NOTES</span></span>

## <span data-ttu-id="4d897-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d897-183">RELATED LINKS</span></span>

[<span data-ttu-id="4d897-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4d897-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
