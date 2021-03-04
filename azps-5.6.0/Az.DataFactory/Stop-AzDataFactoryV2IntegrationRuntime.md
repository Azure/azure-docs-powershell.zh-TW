---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 405754afec3ff62eb59d385646df43f699557d18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914049"
---
# <span data-ttu-id="39a12-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39a12-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="39a12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39a12-102">SYNOPSIS</span></span>
<span data-ttu-id="39a12-103">停止受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="39a12-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="39a12-104">語法</span><span class="sxs-lookup"><span data-stu-id="39a12-104">SYNTAX</span></span>

### <span data-ttu-id="39a12-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="39a12-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39a12-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39a12-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a12-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="39a12-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39a12-108">描述</span><span class="sxs-lookup"><span data-stu-id="39a12-108">DESCRIPTION</span></span>
<span data-ttu-id="39a12-109">**Stop-AzDataFactoryV2 RuntimeRuntime** Cmdlet 會以由 Start-AzDataFactoryV2IntegrationRuntime Cmdlet 啟動的受管理專用整合執行時間以 'Started' 狀態停止。</span><span class="sxs-lookup"><span data-stu-id="39a12-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="39a12-110">資源會釋出，而州會移轉為'已停止」。</span><span class="sxs-lookup"><span data-stu-id="39a12-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="39a12-111">例子</span><span class="sxs-lookup"><span data-stu-id="39a12-111">EXAMPLES</span></span>

### <span data-ttu-id="39a12-112">範例 1：停止位於 'Started' 狀態之受管理的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="39a12-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="39a12-113">受管理的整合執行時間 'test-reserlved-ir' 為 'Started' 狀態。</span><span class="sxs-lookup"><span data-stu-id="39a12-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="39a12-114">在 Cmdlet Stop-AzDataFactoryV2IntegrationRuntime之後，資源會釋出，而狀態會轉移到 '已停止'。</span><span class="sxs-lookup"><span data-stu-id="39a12-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="39a12-115">參數</span><span class="sxs-lookup"><span data-stu-id="39a12-115">PARAMETERS</span></span>

### <span data-ttu-id="39a12-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="39a12-116">-DataFactoryName</span></span>
<span data-ttu-id="39a12-117">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="39a12-117">The data factory name.</span></span>

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

### <span data-ttu-id="39a12-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a12-118">-DefaultProfile</span></span>
<span data-ttu-id="39a12-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39a12-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39a12-120">-強制</span><span class="sxs-lookup"><span data-stu-id="39a12-120">-Force</span></span>
<span data-ttu-id="39a12-121">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="39a12-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="39a12-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39a12-122">-InputObject</span></span>
<span data-ttu-id="39a12-123">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="39a12-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="39a12-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="39a12-124">-Name</span></span>
<span data-ttu-id="39a12-125">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="39a12-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="39a12-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a12-126">-ResourceGroupName</span></span>
<span data-ttu-id="39a12-127">資源組名。</span><span class="sxs-lookup"><span data-stu-id="39a12-127">The resource group name.</span></span>

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

### <span data-ttu-id="39a12-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39a12-128">-ResourceId</span></span>
<span data-ttu-id="39a12-129">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="39a12-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="39a12-130">-確認</span><span class="sxs-lookup"><span data-stu-id="39a12-130">-Confirm</span></span>
<span data-ttu-id="39a12-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39a12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a12-132">-WhatIf</span></span>
<span data-ttu-id="39a12-133">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39a12-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="39a12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a12-134">CommonParameters</span></span>
<span data-ttu-id="39a12-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39a12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a12-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="39a12-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a12-137">輸入</span><span class="sxs-lookup"><span data-stu-id="39a12-137">INPUTS</span></span>

### <span data-ttu-id="39a12-138">System.String</span><span class="sxs-lookup"><span data-stu-id="39a12-138">System.String</span></span>

### <span data-ttu-id="39a12-139">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="39a12-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="39a12-140">輸出</span><span class="sxs-lookup"><span data-stu-id="39a12-140">OUTPUTS</span></span>

### <span data-ttu-id="39a12-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="39a12-141">System.Void</span></span>

## <span data-ttu-id="39a12-142">筆記</span><span class="sxs-lookup"><span data-stu-id="39a12-142">NOTES</span></span>
<span data-ttu-id="39a12-143">關鍵字：azure、azurerm、arm、資源、管理、管理員、資料、專案、複製、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="39a12-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="39a12-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="39a12-144">RELATED LINKS</span></span>

[<span data-ttu-id="39a12-145">Start-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="39a12-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
