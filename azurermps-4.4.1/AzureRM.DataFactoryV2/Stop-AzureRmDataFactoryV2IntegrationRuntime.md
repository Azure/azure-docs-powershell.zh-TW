---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 181d63a41853105b21826353fabfca83cddf1bd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457616"
---
# <span data-ttu-id="251a1-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="251a1-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="251a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="251a1-102">SYNOPSIS</span></span>
<span data-ttu-id="251a1-103">停止受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="251a1-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="251a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="251a1-104">SYNTAX</span></span>

### <span data-ttu-id="251a1-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="251a1-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="251a1-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="251a1-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="251a1-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="251a1-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="251a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="251a1-108">DESCRIPTION</span></span>
<span data-ttu-id="251a1-109">**AzureRmDataFactoryV2IntegrationRuntime** Cmdlet 會在「已啟動」狀態中停止受管理的專用整合執行時間，該作業是由 Start-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 啟動。</span><span class="sxs-lookup"><span data-stu-id="251a1-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="251a1-110">隨即會釋放資源，並將狀態傳輸到 [已停止]。</span><span class="sxs-lookup"><span data-stu-id="251a1-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="251a1-111">示例</span><span class="sxs-lookup"><span data-stu-id="251a1-111">EXAMPLES</span></span>

### <span data-ttu-id="251a1-112">範例1：停止處於「已啟動」狀態的 managed 整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="251a1-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="251a1-113">Managed 整合執行時間 "test-reserlved-ir" 處於「已啟動」狀態。</span><span class="sxs-lookup"><span data-stu-id="251a1-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="251a1-114">在執行 Stop-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 之後，會釋放資源，並將狀態傳輸到「已停止」。</span><span class="sxs-lookup"><span data-stu-id="251a1-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="251a1-115">參數</span><span class="sxs-lookup"><span data-stu-id="251a1-115">PARAMETERS</span></span>

### <span data-ttu-id="251a1-116">-確認</span><span class="sxs-lookup"><span data-stu-id="251a1-116">-Confirm</span></span>
<span data-ttu-id="251a1-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="251a1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251a1-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="251a1-118">-DataFactoryName</span></span>
<span data-ttu-id="251a1-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="251a1-119">The data factory name.</span></span>

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

### <span data-ttu-id="251a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="251a1-120">-Force</span></span>
<span data-ttu-id="251a1-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="251a1-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="251a1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="251a1-122">-InputObject</span></span>
<span data-ttu-id="251a1-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="251a1-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="251a1-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="251a1-124">-Name</span></span>
<span data-ttu-id="251a1-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="251a1-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="251a1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251a1-126">-ResourceGroupName</span></span>
<span data-ttu-id="251a1-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="251a1-127">The resource group name.</span></span>

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

### <span data-ttu-id="251a1-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="251a1-128">-ResourceId</span></span>
<span data-ttu-id="251a1-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="251a1-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="251a1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="251a1-130">-Confirm</span></span>
<span data-ttu-id="251a1-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="251a1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251a1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251a1-132">-WhatIf</span></span>
<span data-ttu-id="251a1-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="251a1-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="251a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251a1-134">CommonParameters</span></span>
<span data-ttu-id="251a1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="251a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251a1-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="251a1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251a1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="251a1-137">INPUTS</span></span>

### <span data-ttu-id="251a1-138">System.object</span><span class="sxs-lookup"><span data-stu-id="251a1-138">System.String</span></span>
<span data-ttu-id="251a1-139">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="251a1-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="251a1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="251a1-140">OUTPUTS</span></span>

### <span data-ttu-id="251a1-141">System.object</span><span class="sxs-lookup"><span data-stu-id="251a1-141">System.Boolean</span></span>

## <span data-ttu-id="251a1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="251a1-142">NOTES</span></span>
<span data-ttu-id="251a1-143">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="251a1-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="251a1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="251a1-144">RELATED LINKS</span></span>
[<span data-ttu-id="251a1-145">開始-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="251a1-145">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
