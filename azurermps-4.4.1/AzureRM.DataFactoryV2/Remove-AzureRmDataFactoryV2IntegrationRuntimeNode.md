---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454399"
---
# <span data-ttu-id="678fc-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="678fc-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="678fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="678fc-102">SYNOPSIS</span></span>
<span data-ttu-id="678fc-103">在整合執行時間中移除具有指定名稱的節點。</span><span class="sxs-lookup"><span data-stu-id="678fc-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="678fc-104">SYNTAX</span></span>

### <span data-ttu-id="678fc-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="678fc-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="678fc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="678fc-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="678fc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="678fc-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="678fc-108">說明</span><span class="sxs-lookup"><span data-stu-id="678fc-108">DESCRIPTION</span></span>
<span data-ttu-id="678fc-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode Cmdlet 會移除整合執行時間中的節點。</span><span class="sxs-lookup"><span data-stu-id="678fc-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="678fc-110">示例</span><span class="sxs-lookup"><span data-stu-id="678fc-110">EXAMPLES</span></span>

### <span data-ttu-id="678fc-111">範例1：從整合執行時間中移除節點</span><span class="sxs-lookup"><span data-stu-id="678fc-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="678fc-112">這個命令會移除名為「rg-test-dfv2」的整合執行時間中名為「Node_1」的節點，以及名為「test-eu2」的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="678fc-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="678fc-113">參數</span><span class="sxs-lookup"><span data-stu-id="678fc-113">PARAMETERS</span></span>

### <span data-ttu-id="678fc-114">-確認</span><span class="sxs-lookup"><span data-stu-id="678fc-114">-Confirm</span></span>
<span data-ttu-id="678fc-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="678fc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678fc-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="678fc-116">-DataFactoryName</span></span>
<span data-ttu-id="678fc-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="678fc-117">The data factory name.</span></span>

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

### <span data-ttu-id="678fc-118">-Force</span><span class="sxs-lookup"><span data-stu-id="678fc-118">-Force</span></span>
<span data-ttu-id="678fc-119">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="678fc-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="678fc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678fc-120">-InputObject</span></span>
<span data-ttu-id="678fc-121">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="678fc-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="678fc-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="678fc-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="678fc-123">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="678fc-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678fc-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="678fc-124">-NodeName</span></span>
<span data-ttu-id="678fc-125">整合執行時間節點名稱。</span><span class="sxs-lookup"><span data-stu-id="678fc-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="678fc-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="678fc-127">The resource group name.</span></span>

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

### <span data-ttu-id="678fc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="678fc-128">-ResourceId</span></span>
<span data-ttu-id="678fc-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="678fc-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="678fc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678fc-130">-WhatIf</span></span>
<span data-ttu-id="678fc-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="678fc-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="678fc-132">輸入</span><span class="sxs-lookup"><span data-stu-id="678fc-132">INPUTS</span></span>

### <span data-ttu-id="678fc-133">System.object</span><span class="sxs-lookup"><span data-stu-id="678fc-133">System.String</span></span>
<span data-ttu-id="678fc-134">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="678fc-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="678fc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="678fc-135">OUTPUTS</span></span>

### <span data-ttu-id="678fc-136">System.object</span><span class="sxs-lookup"><span data-stu-id="678fc-136">System.Object</span></span>

## <span data-ttu-id="678fc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="678fc-137">NOTES</span></span>

## <span data-ttu-id="678fc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="678fc-138">RELATED LINKS</span></span>

