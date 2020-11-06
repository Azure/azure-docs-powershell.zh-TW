---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457628"
---
# <span data-ttu-id="d8749-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d8749-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="d8749-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8749-102">SYNOPSIS</span></span>
<span data-ttu-id="d8749-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d8749-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8749-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8749-104">SYNTAX</span></span>

### <span data-ttu-id="d8749-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="d8749-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d8749-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d8749-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d8749-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d8749-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="d8749-108">說明</span><span class="sxs-lookup"><span data-stu-id="d8749-108">DESCRIPTION</span></span>
<span data-ttu-id="d8749-109">Set-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 會使用特定參數更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="d8749-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="d8749-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8749-110">EXAMPLES</span></span>

### <span data-ttu-id="d8749-111">範例1：更新整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="d8749-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="d8749-112">此 Cmdlet 會更新名為「test-selfhost-ir」的整合執行時間說明。</span><span class="sxs-lookup"><span data-stu-id="d8749-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d8749-113">參數</span><span class="sxs-lookup"><span data-stu-id="d8749-113">PARAMETERS</span></span>

### <span data-ttu-id="d8749-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="d8749-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="d8749-115">整合執行時間的目錄資料庫系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="d8749-115">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="d8749-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="d8749-116">-CatalogPricingTier</span></span>
<span data-ttu-id="d8749-117">整合執行時間的 [目錄資料庫] 定價層級。</span><span class="sxs-lookup"><span data-stu-id="d8749-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="d8749-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d8749-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="d8749-119">整合執行時間的目錄資料庫伺服器端點。</span><span class="sxs-lookup"><span data-stu-id="d8749-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="d8749-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d8749-120">-Confirm</span></span>
<span data-ttu-id="d8749-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d8749-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8749-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d8749-122">-DataFactoryName</span></span>
<span data-ttu-id="d8749-123">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d8749-123">The data factory name.</span></span>

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

### <span data-ttu-id="d8749-124">-描述</span><span class="sxs-lookup"><span data-stu-id="d8749-124">-Description</span></span>
<span data-ttu-id="d8749-125">整合執行時間的描述。</span><span class="sxs-lookup"><span data-stu-id="d8749-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="d8749-126">-Force</span><span class="sxs-lookup"><span data-stu-id="d8749-126">-Force</span></span>
<span data-ttu-id="d8749-127">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d8749-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d8749-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8749-128">-InputObject</span></span>
<span data-ttu-id="d8749-129">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="d8749-129">The integration runtime object.</span></span>

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

### <span data-ttu-id="d8749-130">-位置</span><span class="sxs-lookup"><span data-stu-id="d8749-130">-Location</span></span>
<span data-ttu-id="d8749-131">整合執行時間的位置。</span><span class="sxs-lookup"><span data-stu-id="d8749-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="d8749-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="d8749-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="d8749-133">受管理的專用整合執行時間每個節點的最大並存執行次數。</span><span class="sxs-lookup"><span data-stu-id="d8749-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="d8749-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8749-134">-Name</span></span>
<span data-ttu-id="d8749-135">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="d8749-135">The integration runtime name.</span></span>

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

### <span data-ttu-id="d8749-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d8749-136">-NodeCount</span></span>
<span data-ttu-id="d8749-137">整合執行時間的目標節點數。</span><span class="sxs-lookup"><span data-stu-id="d8749-137">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="d8749-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="d8749-138">-NodeSize</span></span>
<span data-ttu-id="d8749-139">整合執行時間節點大小。</span><span class="sxs-lookup"><span data-stu-id="d8749-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="d8749-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8749-140">-ResourceGroupName</span></span>
<span data-ttu-id="d8749-141">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8749-141">The resource group name.</span></span>

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

### <span data-ttu-id="d8749-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8749-142">-ResourceId</span></span>
<span data-ttu-id="d8749-143">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8749-143">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d8749-144">-子網</span><span class="sxs-lookup"><span data-stu-id="d8749-144">-Subnet</span></span>
<span data-ttu-id="d8749-145">VNet 中子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8749-145">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="d8749-146">-類型</span><span class="sxs-lookup"><span data-stu-id="d8749-146">-Type</span></span>
<span data-ttu-id="d8749-147">整合執行時間類型。</span><span class="sxs-lookup"><span data-stu-id="d8749-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="d8749-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="d8749-148">-VNetId</span></span>
<span data-ttu-id="d8749-149">整合執行時間加入的 VNet ID。</span><span class="sxs-lookup"><span data-stu-id="d8749-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="d8749-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8749-150">-WhatIf</span></span>
<span data-ttu-id="d8749-151">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d8749-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="d8749-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d8749-152">INPUTS</span></span>

### <span data-ttu-id="d8749-153">System.object</span><span class="sxs-lookup"><span data-stu-id="d8749-153">System.String</span></span>
<span data-ttu-id="d8749-154">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d8749-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d8749-155">輸出</span><span class="sxs-lookup"><span data-stu-id="d8749-155">OUTPUTS</span></span>

### <span data-ttu-id="d8749-156">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d8749-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d8749-157">筆記</span><span class="sxs-lookup"><span data-stu-id="d8749-157">NOTES</span></span>

## <span data-ttu-id="d8749-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8749-158">RELATED LINKS</span></span>
[<span data-ttu-id="d8749-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="d8749-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
