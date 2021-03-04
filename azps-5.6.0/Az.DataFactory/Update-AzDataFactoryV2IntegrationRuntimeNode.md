---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: ca0f14bf6940c9d81933c4a42703d828efdc5e51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914029"
---
# <span data-ttu-id="275e6-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="275e6-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="275e6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="275e6-102">SYNOPSIS</span></span>
<span data-ttu-id="275e6-103">更新自我託管的整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="275e6-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="275e6-104">語法</span><span class="sxs-lookup"><span data-stu-id="275e6-104">SYNTAX</span></span>

### <span data-ttu-id="275e6-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="275e6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275e6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="275e6-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275e6-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="275e6-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="275e6-108">描述</span><span class="sxs-lookup"><span data-stu-id="275e6-108">DESCRIPTION</span></span>
<span data-ttu-id="275e6-109">**Update-AzDataFactoryV2 RuntimeRuntimeNode** Cmdlet 會更新資料工廠中自我託管整合執行時間節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="275e6-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="275e6-110">目前僅支援更新 'ConcurrentJobsLimit'。</span><span class="sxs-lookup"><span data-stu-id="275e6-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="275e6-111">例子</span><span class="sxs-lookup"><span data-stu-id="275e6-111">EXAMPLES</span></span>

### <span data-ttu-id="275e6-112">範例 1：更新自我託管整合執行時間節點</span><span class="sxs-lookup"><span data-stu-id="275e6-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="275e6-113">Cmdlet 會針對自我託管整合執行時間 "test-selfhost-ir" 中的節點 "Node_1" 將 "ConcurrentJobsLimit" 更新為 3。</span><span class="sxs-lookup"><span data-stu-id="275e6-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="275e6-114">參數</span><span class="sxs-lookup"><span data-stu-id="275e6-114">PARAMETERS</span></span>

### <span data-ttu-id="275e6-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="275e6-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="275e6-116">在整合執行時間節點上允許執行並行工作的數量。</span><span class="sxs-lookup"><span data-stu-id="275e6-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="275e6-117">允許介於 1 到 maxConcurrentJobs 之間的值。</span><span class="sxs-lookup"><span data-stu-id="275e6-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275e6-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="275e6-118">-DataFactoryName</span></span>
<span data-ttu-id="275e6-119">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="275e6-119">The data factory name.</span></span>

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

### <span data-ttu-id="275e6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275e6-120">-DefaultProfile</span></span>
<span data-ttu-id="275e6-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="275e6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="275e6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="275e6-122">-InputObject</span></span>
<span data-ttu-id="275e6-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="275e6-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="275e6-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="275e6-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="275e6-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="275e6-125">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275e6-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="275e6-126">-Name</span></span>
<span data-ttu-id="275e6-127">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="275e6-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275e6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275e6-128">-ResourceGroupName</span></span>
<span data-ttu-id="275e6-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="275e6-129">The resource group name.</span></span>

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

### <span data-ttu-id="275e6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="275e6-130">-ResourceId</span></span>
<span data-ttu-id="275e6-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="275e6-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="275e6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="275e6-132">-Confirm</span></span>
<span data-ttu-id="275e6-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="275e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="275e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275e6-134">-WhatIf</span></span>
<span data-ttu-id="275e6-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="275e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275e6-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="275e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="275e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275e6-137">CommonParameters</span></span>
<span data-ttu-id="275e6-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="275e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275e6-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="275e6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275e6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="275e6-140">INPUTS</span></span>

### <span data-ttu-id="275e6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="275e6-141">System.String</span></span>

### <span data-ttu-id="275e6-142">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="275e6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="275e6-143">輸出</span><span class="sxs-lookup"><span data-stu-id="275e6-143">OUTPUTS</span></span>

### <span data-ttu-id="275e6-144">Microsoft.Azure.Commands.DataFactoryV2.models.PSSelfHosted方格RuntimeNode</span><span class="sxs-lookup"><span data-stu-id="275e6-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="275e6-145">筆記</span><span class="sxs-lookup"><span data-stu-id="275e6-145">NOTES</span></span>
<span data-ttu-id="275e6-146">關鍵字：azure、azurerm、arm、資源、管理、管理員、資料、專案、複製、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="275e6-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="275e6-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="275e6-147">RELATED LINKS</span></span>

<span data-ttu-id="275e6-148">[Set-AzDataFactoryV2FactoryRuntime]() 
[Get-AzDataFactoryV2FactoryRuntime]()</span><span class="sxs-lookup"><span data-stu-id="275e6-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

