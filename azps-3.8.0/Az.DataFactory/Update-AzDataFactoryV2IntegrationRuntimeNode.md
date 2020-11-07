---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 0487794381e40db486df17cb9611191ac5d924d9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958510"
---
# <span data-ttu-id="b4cff-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="b4cff-101">Update-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="b4cff-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b4cff-102">SYNOPSIS</span></span>
<span data-ttu-id="b4cff-103">更新自託管的整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="b4cff-103">Updates self-hosted integration runtime node.</span></span>

## <span data-ttu-id="b4cff-104">句法</span><span class="sxs-lookup"><span data-stu-id="b4cff-104">SYNTAX</span></span>

### <span data-ttu-id="b4cff-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="b4cff-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b4cff-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4cff-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b4cff-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b4cff-108">說明</span><span class="sxs-lookup"><span data-stu-id="b4cff-108">DESCRIPTION</span></span>
<span data-ttu-id="b4cff-109">**AzDataFactoryV2IntegrationRuntimeNode** Cmdlet 會更新資料工廠中自行託管整合執行時間節點的屬性。</span><span class="sxs-lookup"><span data-stu-id="b4cff-109">The **Update-AzDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="b4cff-110">目前僅支援更新 ' ConcurrentJobsLimit」。</span><span class="sxs-lookup"><span data-stu-id="b4cff-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="b4cff-111">示例</span><span class="sxs-lookup"><span data-stu-id="b4cff-111">EXAMPLES</span></span>

### <span data-ttu-id="b4cff-112">範例1：更新自託管整合執行時間節點</span><span class="sxs-lookup"><span data-stu-id="b4cff-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="b4cff-113">在自行託管整合執行時間 "test-selfhost-ir" 中，Cmdlet 會將節點 "Node_1" 的 [ConcurrentJobsLimit "更新為3。</span><span class="sxs-lookup"><span data-stu-id="b4cff-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="b4cff-114">參數</span><span class="sxs-lookup"><span data-stu-id="b4cff-114">PARAMETERS</span></span>

### <span data-ttu-id="b4cff-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="b4cff-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="b4cff-116">允許在整合執行時間節點上執行的併發作業數目。</span><span class="sxs-lookup"><span data-stu-id="b4cff-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="b4cff-117">允許介於1和 maxConcurrentJobs 之間的值。</span><span class="sxs-lookup"><span data-stu-id="b4cff-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

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

### <span data-ttu-id="b4cff-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b4cff-118">-DataFactoryName</span></span>
<span data-ttu-id="b4cff-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cff-119">The data factory name.</span></span>

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

### <span data-ttu-id="b4cff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4cff-120">-DefaultProfile</span></span>
<span data-ttu-id="b4cff-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4cff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4cff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b4cff-122">-InputObject</span></span>
<span data-ttu-id="b4cff-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="b4cff-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="b4cff-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b4cff-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b4cff-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cff-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="b4cff-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4cff-126">-Name</span></span>
<span data-ttu-id="b4cff-127">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cff-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="b4cff-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4cff-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4cff-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4cff-129">The resource group name.</span></span>

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

### <span data-ttu-id="b4cff-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4cff-130">-ResourceId</span></span>
<span data-ttu-id="b4cff-131">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4cff-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b4cff-132">-確認</span><span class="sxs-lookup"><span data-stu-id="b4cff-132">-Confirm</span></span>
<span data-ttu-id="b4cff-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b4cff-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4cff-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4cff-134">-WhatIf</span></span>
<span data-ttu-id="b4cff-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4cff-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4cff-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4cff-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4cff-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4cff-137">CommonParameters</span></span>
<span data-ttu-id="b4cff-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b4cff-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4cff-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b4cff-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4cff-140">輸入</span><span class="sxs-lookup"><span data-stu-id="b4cff-140">INPUTS</span></span>

### <span data-ttu-id="b4cff-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b4cff-141">System.String</span></span>

### <span data-ttu-id="b4cff-142">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b4cff-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="b4cff-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b4cff-143">OUTPUTS</span></span>

### <span data-ttu-id="b4cff-144">PSSelfHostedIntegrationRuntimeNode 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="b4cff-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="b4cff-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b4cff-145">NOTES</span></span>
<span data-ttu-id="b4cff-146">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="b4cff-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b4cff-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4cff-147">RELATED LINKS</span></span>

<span data-ttu-id="b4cff-148">[Set-AzDataFactoryV2IntegrationRuntime]() 
[AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="b4cff-148">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

