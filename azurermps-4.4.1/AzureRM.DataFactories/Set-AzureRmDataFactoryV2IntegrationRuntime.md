---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626321"
---
# <span data-ttu-id="33b0f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33b0f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="33b0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="33b0f-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="33b0f-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33b0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="33b0f-104">SYNTAX</span></span>

### <span data-ttu-id="33b0f-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="33b0f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33b0f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="33b0f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33b0f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="33b0f-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33b0f-108">說明</span><span class="sxs-lookup"><span data-stu-id="33b0f-108">DESCRIPTION</span></span>
<span data-ttu-id="33b0f-109">Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="33b0f-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="33b0f-110">示例</span><span class="sxs-lookup"><span data-stu-id="33b0f-110">EXAMPLES</span></span>

### <span data-ttu-id="33b0f-111">範例1：更新整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="33b0f-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="33b0f-112">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="33b0f-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="33b0f-113">參數</span><span class="sxs-lookup"><span data-stu-id="33b0f-113">PARAMETERS</span></span>

### <span data-ttu-id="33b0f-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="33b0f-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="33b0f-115">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="33b0f-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="33b0f-116">-CatalogPricingTier</span></span>
<span data-ttu-id="33b0f-117">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="33b0f-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="33b0f-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33b0f-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="33b0f-119">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="33b0f-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="33b0f-120">-確認</span><span class="sxs-lookup"><span data-stu-id="33b0f-120">-Confirm</span></span>
<span data-ttu-id="33b0f-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="33b0f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b0f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="33b0f-122">-DataFactoryName</span></span>
<span data-ttu-id="33b0f-123">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="33b0f-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-124">-描述</span><span class="sxs-lookup"><span data-stu-id="33b0f-124">-Description</span></span>
<span data-ttu-id="33b0f-125">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="33b0f-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="33b0f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="33b0f-126">-Force</span></span>
<span data-ttu-id="33b0f-127">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="33b0f-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="33b0f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33b0f-128">-InputObject</span></span>
<span data-ttu-id="33b0f-129">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="33b0f-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-130">-位置</span><span class="sxs-lookup"><span data-stu-id="33b0f-130">-Location</span></span>
<span data-ttu-id="33b0f-131">整合執行時間的位置。</span><span class="sxs-lookup"><span data-stu-id="33b0f-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="33b0f-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="33b0f-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="33b0f-133">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="33b0f-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="33b0f-134">-Name</span></span>
<span data-ttu-id="33b0f-135">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="33b0f-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="33b0f-136">-NodeCount</span></span>
<span data-ttu-id="33b0f-137">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="33b0f-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="33b0f-138">-NodeSize</span></span>
<span data-ttu-id="33b0f-139">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="33b0f-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="33b0f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33b0f-140">-ResourceGroupName</span></span>
<span data-ttu-id="33b0f-141">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="33b0f-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33b0f-142">-ResourceId</span></span>
<span data-ttu-id="33b0f-143">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="33b0f-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-144">-子網</span><span class="sxs-lookup"><span data-stu-id="33b0f-144">-Subnet</span></span>
<span data-ttu-id="33b0f-145">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="33b0f-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-146">-類型</span><span class="sxs-lookup"><span data-stu-id="33b0f-146">-Type</span></span>
<span data-ttu-id="33b0f-147">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="33b0f-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="33b0f-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="33b0f-148">-VNetId</span></span>
<span data-ttu-id="33b0f-149">整合執行時間加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="33b0f-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="33b0f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b0f-150">-WhatIf</span></span>
<span data-ttu-id="33b0f-151">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="33b0f-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="33b0f-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b0f-152">-DefaultProfile</span></span>
<span data-ttu-id="33b0f-153">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="33b0f-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b0f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b0f-154">CommonParameters</span></span>
<span data-ttu-id="33b0f-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33b0f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b0f-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33b0f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b0f-157">輸入</span><span class="sxs-lookup"><span data-stu-id="33b0f-157">INPUTS</span></span>

### <span data-ttu-id="33b0f-158">System.object</span><span class="sxs-lookup"><span data-stu-id="33b0f-158">System.String</span></span>
<span data-ttu-id="33b0f-159">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="33b0f-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33b0f-160">輸出</span><span class="sxs-lookup"><span data-stu-id="33b0f-160">OUTPUTS</span></span>

### <span data-ttu-id="33b0f-161">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="33b0f-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="33b0f-162">筆記</span><span class="sxs-lookup"><span data-stu-id="33b0f-162">NOTES</span></span>

## <span data-ttu-id="33b0f-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="33b0f-163">RELATED LINKS</span></span>

[<span data-ttu-id="33b0f-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="33b0f-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
