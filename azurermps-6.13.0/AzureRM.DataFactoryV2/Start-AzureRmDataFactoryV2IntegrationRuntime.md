---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a9254fbac7e0c98413f4367d9b5e62581f6cb64c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624064"
---
# <span data-ttu-id="3812a-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3812a-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3812a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3812a-102">SYNOPSIS</span></span>
<span data-ttu-id="3812a-103">啟動受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="3812a-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3812a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3812a-104">SYNTAX</span></span>

### <span data-ttu-id="3812a-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="3812a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3812a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3812a-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3812a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3812a-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3812a-108">說明</span><span class="sxs-lookup"><span data-stu-id="3812a-108">DESCRIPTION</span></span>
<span data-ttu-id="3812a-109">**AzureRmDataFactoryV2IntegrationRuntime** Cmdlet 會啟動受管理的專用整合式執行時間。</span><span class="sxs-lookup"><span data-stu-id="3812a-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="3812a-110">資源已在作業狀態為「已啟動」的情況下進行預配。</span><span class="sxs-lookup"><span data-stu-id="3812a-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="3812a-111">示例</span><span class="sxs-lookup"><span data-stu-id="3812a-111">EXAMPLES</span></span>

### <span data-ttu-id="3812a-112">範例1：啟動整合執行時間</span><span class="sxs-lookup"><span data-stu-id="3812a-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="3812a-113">這個 Cmdlet 會啟動一個名為「測試專用-ir」的 managed 專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="3812a-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="3812a-114">參數</span><span class="sxs-lookup"><span data-stu-id="3812a-114">PARAMETERS</span></span>

### <span data-ttu-id="3812a-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3812a-115">-DataFactoryName</span></span>
<span data-ttu-id="3812a-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="3812a-116">The data factory name.</span></span>

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

### <span data-ttu-id="3812a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3812a-117">-DefaultProfile</span></span>
<span data-ttu-id="3812a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3812a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3812a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3812a-119">-Force</span></span>
<span data-ttu-id="3812a-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3812a-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3812a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3812a-121">-InputObject</span></span>
<span data-ttu-id="3812a-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="3812a-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="3812a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3812a-123">-Name</span></span>
<span data-ttu-id="3812a-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="3812a-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="3812a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3812a-125">-ResourceGroupName</span></span>
<span data-ttu-id="3812a-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3812a-126">The resource group name.</span></span>

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

### <span data-ttu-id="3812a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3812a-127">-ResourceId</span></span>
<span data-ttu-id="3812a-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="3812a-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3812a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="3812a-129">-Confirm</span></span>
<span data-ttu-id="3812a-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3812a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3812a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3812a-131">-WhatIf</span></span>
<span data-ttu-id="3812a-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3812a-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3812a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3812a-133">CommonParameters</span></span>
<span data-ttu-id="3812a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3812a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3812a-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3812a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3812a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="3812a-136">INPUTS</span></span>

### <span data-ttu-id="3812a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="3812a-137">System.String</span></span>

### <span data-ttu-id="3812a-138">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="3812a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="3812a-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="3812a-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3812a-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3812a-140">OUTPUTS</span></span>

### <span data-ttu-id="3812a-141">PSManagedIntegrationRuntimeStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="3812a-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="3812a-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3812a-142">NOTES</span></span>

## <span data-ttu-id="3812a-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3812a-143">RELATED LINKS</span></span>

[<span data-ttu-id="3812a-144">停止 AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3812a-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
