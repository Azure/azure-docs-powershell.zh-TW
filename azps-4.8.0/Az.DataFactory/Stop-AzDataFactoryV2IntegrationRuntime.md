---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128778"
---
# <span data-ttu-id="f645f-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f645f-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="f645f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f645f-102">SYNOPSIS</span></span>
<span data-ttu-id="f645f-103">停止受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="f645f-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="f645f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f645f-104">SYNTAX</span></span>

### <span data-ttu-id="f645f-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="f645f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f645f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f645f-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f645f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="f645f-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f645f-108">說明</span><span class="sxs-lookup"><span data-stu-id="f645f-108">DESCRIPTION</span></span>
<span data-ttu-id="f645f-109">**AzDataFactoryV2IntegrationRuntime** Cmdlet 會在「已啟動」狀態中停止受管理的專用整合執行時間，該作業是由 Start-AzDataFactoryV2IntegrationRuntime Cmdlet 啟動。</span><span class="sxs-lookup"><span data-stu-id="f645f-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="f645f-110">隨即會釋放資源，並將狀態傳輸到 [已停止]。</span><span class="sxs-lookup"><span data-stu-id="f645f-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="f645f-111">示例</span><span class="sxs-lookup"><span data-stu-id="f645f-111">EXAMPLES</span></span>

### <span data-ttu-id="f645f-112">範例1：停止處於「已啟動」狀態的 managed 整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="f645f-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="f645f-113">Managed 整合執行時間 "test-reserlved-ir" 處於「已啟動」狀態。</span><span class="sxs-lookup"><span data-stu-id="f645f-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="f645f-114">在執行 Stop-AzDataFactoryV2IntegrationRuntime Cmdlet 之後，會釋放資源，並將狀態傳輸到「已停止」。</span><span class="sxs-lookup"><span data-stu-id="f645f-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="f645f-115">參數</span><span class="sxs-lookup"><span data-stu-id="f645f-115">PARAMETERS</span></span>

### <span data-ttu-id="f645f-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f645f-116">-DataFactoryName</span></span>
<span data-ttu-id="f645f-117">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="f645f-117">The data factory name.</span></span>

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

### <span data-ttu-id="f645f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f645f-118">-DefaultProfile</span></span>
<span data-ttu-id="f645f-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f645f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f645f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f645f-120">-Force</span></span>
<span data-ttu-id="f645f-121">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f645f-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="f645f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f645f-122">-InputObject</span></span>
<span data-ttu-id="f645f-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="f645f-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="f645f-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f645f-124">-Name</span></span>
<span data-ttu-id="f645f-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="f645f-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="f645f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f645f-126">-ResourceGroupName</span></span>
<span data-ttu-id="f645f-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f645f-127">The resource group name.</span></span>

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

### <span data-ttu-id="f645f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f645f-128">-ResourceId</span></span>
<span data-ttu-id="f645f-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f645f-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f645f-130">-確認</span><span class="sxs-lookup"><span data-stu-id="f645f-130">-Confirm</span></span>
<span data-ttu-id="f645f-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f645f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f645f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f645f-132">-WhatIf</span></span>
<span data-ttu-id="f645f-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f645f-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="f645f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f645f-134">CommonParameters</span></span>
<span data-ttu-id="f645f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f645f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f645f-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f645f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f645f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f645f-137">INPUTS</span></span>

### <span data-ttu-id="f645f-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f645f-138">System.String</span></span>

### <span data-ttu-id="f645f-139">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="f645f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="f645f-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f645f-140">OUTPUTS</span></span>

### <span data-ttu-id="f645f-141">System.void</span><span class="sxs-lookup"><span data-stu-id="f645f-141">System.Void</span></span>

## <span data-ttu-id="f645f-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f645f-142">NOTES</span></span>
<span data-ttu-id="f645f-143">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="f645f-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="f645f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f645f-144">RELATED LINKS</span></span>

[<span data-ttu-id="f645f-145">開始-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="f645f-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
