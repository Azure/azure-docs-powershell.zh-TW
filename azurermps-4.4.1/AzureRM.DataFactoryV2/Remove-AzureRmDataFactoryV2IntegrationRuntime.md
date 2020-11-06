---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456736"
---
# <span data-ttu-id="931dc-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="931dc-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="931dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="931dc-102">SYNOPSIS</span></span>
<span data-ttu-id="931dc-103">移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="931dc-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="931dc-104">SYNTAX</span></span>

### <span data-ttu-id="931dc-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="931dc-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="931dc-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="931dc-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="931dc-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="931dc-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="931dc-108">說明</span><span class="sxs-lookup"><span data-stu-id="931dc-108">DESCRIPTION</span></span>
<span data-ttu-id="931dc-109">Remove-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 會移除整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="931dc-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="931dc-110">示例</span><span class="sxs-lookup"><span data-stu-id="931dc-110">EXAMPLES</span></span>

### <span data-ttu-id="931dc-111">範例1：移除整合執行時間</span><span class="sxs-lookup"><span data-stu-id="931dc-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="931dc-112">這個命令會從名為「test-df」的資料工廠中，移除名為「test reserved-ir」的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="931dc-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="931dc-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="931dc-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="931dc-114">參數</span><span class="sxs-lookup"><span data-stu-id="931dc-114">PARAMETERS</span></span>

### <span data-ttu-id="931dc-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="931dc-115">-DataFactoryName</span></span>
<span data-ttu-id="931dc-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="931dc-116">The data factory name.</span></span>

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

### <span data-ttu-id="931dc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="931dc-117">-Force</span></span>
<span data-ttu-id="931dc-118">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="931dc-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="931dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="931dc-119">-InputObject</span></span>
<span data-ttu-id="931dc-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="931dc-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="931dc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="931dc-121">-Name</span></span>
<span data-ttu-id="931dc-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="931dc-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="931dc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931dc-123">-ResourceGroupName</span></span>
<span data-ttu-id="931dc-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="931dc-124">The resource group name.</span></span>

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

### <span data-ttu-id="931dc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="931dc-125">-ResourceId</span></span>
<span data-ttu-id="931dc-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="931dc-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="931dc-127">-確認</span><span class="sxs-lookup"><span data-stu-id="931dc-127">-Confirm</span></span>
<span data-ttu-id="931dc-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="931dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931dc-129">-WhatIf</span></span>
<span data-ttu-id="931dc-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="931dc-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="931dc-131">輸入</span><span class="sxs-lookup"><span data-stu-id="931dc-131">INPUTS</span></span>

### <span data-ttu-id="931dc-132">System.object</span><span class="sxs-lookup"><span data-stu-id="931dc-132">System.String</span></span>
<span data-ttu-id="931dc-133">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="931dc-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="931dc-134">輸出</span><span class="sxs-lookup"><span data-stu-id="931dc-134">OUTPUTS</span></span>

### <span data-ttu-id="931dc-135">System.object</span><span class="sxs-lookup"><span data-stu-id="931dc-135">System.Object</span></span>

## <span data-ttu-id="931dc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="931dc-136">NOTES</span></span>
<span data-ttu-id="931dc-137">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="931dc-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="931dc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="931dc-138">RELATED LINKS</span></span>
[<span data-ttu-id="931dc-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="931dc-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="931dc-140">AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="931dc-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

