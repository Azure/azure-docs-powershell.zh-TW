---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448723"
---
# <span data-ttu-id="fb360-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fb360-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="fb360-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb360-102">SYNOPSIS</span></span>
<span data-ttu-id="fb360-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="fb360-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb360-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb360-104">SYNTAX</span></span>

### <span data-ttu-id="fb360-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="fb360-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb360-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb360-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb360-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="fb360-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb360-108">說明</span><span class="sxs-lookup"><span data-stu-id="fb360-108">DESCRIPTION</span></span>
<span data-ttu-id="fb360-109">Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="fb360-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="fb360-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb360-110">EXAMPLES</span></span>

### <span data-ttu-id="fb360-111">範例1：更新整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="fb360-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="fb360-112">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="fb360-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="fb360-113">參數</span><span class="sxs-lookup"><span data-stu-id="fb360-113">PARAMETERS</span></span>

### <span data-ttu-id="fb360-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="fb360-114">-AuthKey</span></span>
<span data-ttu-id="fb360-115">自託管整合執行時間的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fb360-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="fb360-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="fb360-117">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="fb360-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="fb360-118">-CatalogPricingTier</span></span>
<span data-ttu-id="fb360-119">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="fb360-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="fb360-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="fb360-121">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="fb360-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fb360-122">-DataFactoryName</span></span>
<span data-ttu-id="fb360-123">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fb360-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb360-124">-DefaultProfile</span></span>
<span data-ttu-id="fb360-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb360-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-126">-描述</span><span class="sxs-lookup"><span data-stu-id="fb360-126">-Description</span></span>
<span data-ttu-id="fb360-127">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="fb360-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="fb360-128">-Edition</span></span>
<span data-ttu-id="fb360-129">可能是標準或企業的 SSIS 整合執行時間版本，預設為標準（如果未指定）。</span><span class="sxs-lookup"><span data-stu-id="fb360-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-130">-Force</span><span class="sxs-lookup"><span data-stu-id="fb360-130">-Force</span></span>
<span data-ttu-id="fb360-131">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb360-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb360-132">-InputObject</span></span>
<span data-ttu-id="fb360-133">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="fb360-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fb360-134">-LicenseType</span></span>
<span data-ttu-id="fb360-135">您要為 SSIS IR 選取的授權類型。</span><span class="sxs-lookup"><span data-stu-id="fb360-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="fb360-136">有兩種類型： LicenseIncluded 或 BasePrice。</span><span class="sxs-lookup"><span data-stu-id="fb360-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="fb360-137">如果您符合 Azure 混合式使用優惠 (AHUB) 定價，請選取 [BasePrice]。</span><span class="sxs-lookup"><span data-stu-id="fb360-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="fb360-138">如果不是，請選取 [LicenseIncluded]。</span><span class="sxs-lookup"><span data-stu-id="fb360-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-139">-位置</span><span class="sxs-lookup"><span data-stu-id="fb360-139">-Location</span></span>
<span data-ttu-id="fb360-140">整合執行時間的位置。</span><span class="sxs-lookup"><span data-stu-id="fb360-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="fb360-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="fb360-142">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="fb360-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-143">-名稱</span><span class="sxs-lookup"><span data-stu-id="fb360-143">-Name</span></span>
<span data-ttu-id="fb360-144">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="fb360-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="fb360-145">-NodeCount</span></span>
<span data-ttu-id="fb360-146">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="fb360-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="fb360-147">-NodeSize</span></span>
<span data-ttu-id="fb360-148">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="fb360-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb360-149">-ResourceGroupName</span></span>
<span data-ttu-id="fb360-150">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb360-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb360-151">-ResourceId</span></span>
<span data-ttu-id="fb360-152">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fb360-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="fb360-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="fb360-154">包含自訂安裝程式腳本之 Azure blob 容器的 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="fb360-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-155">-子網</span><span class="sxs-lookup"><span data-stu-id="fb360-155">-Subnet</span></span>
<span data-ttu-id="fb360-156">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="fb360-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-157">-類型</span><span class="sxs-lookup"><span data-stu-id="fb360-157">-Type</span></span>
<span data-ttu-id="fb360-158">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="fb360-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="fb360-159">-VNetId</span></span>
<span data-ttu-id="fb360-160">整合執行時間加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="fb360-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-161">-確認</span><span class="sxs-lookup"><span data-stu-id="fb360-161">-Confirm</span></span>
<span data-ttu-id="fb360-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fb360-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb360-163">-WhatIf</span></span>
<span data-ttu-id="fb360-164">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fb360-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb360-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb360-165">CommonParameters</span></span>
<span data-ttu-id="fb360-166">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb360-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb360-167">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb360-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb360-168">輸入</span><span class="sxs-lookup"><span data-stu-id="fb360-168">INPUTS</span></span>

### <span data-ttu-id="fb360-169">System.object</span><span class="sxs-lookup"><span data-stu-id="fb360-169">System.String</span></span>
<span data-ttu-id="fb360-170">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fb360-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fb360-171">輸出</span><span class="sxs-lookup"><span data-stu-id="fb360-171">OUTPUTS</span></span>

### <span data-ttu-id="fb360-172">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="fb360-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="fb360-173">筆記</span><span class="sxs-lookup"><span data-stu-id="fb360-173">NOTES</span></span>

## <span data-ttu-id="fb360-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb360-174">RELATED LINKS</span></span>

[<span data-ttu-id="fb360-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="fb360-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
