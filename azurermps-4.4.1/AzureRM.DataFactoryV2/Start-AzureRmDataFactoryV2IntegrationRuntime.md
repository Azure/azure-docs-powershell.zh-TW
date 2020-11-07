---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 2b5f01047bf0b86fc885a01f0c58a9ab094f7698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626631"
---
# <span data-ttu-id="2c1b9-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c1b9-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="2c1b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1b9-103">啟動受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c1b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c1b9-104">SYNTAX</span></span>

### <span data-ttu-id="2c1b9-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c1b9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2c1b9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c1b9-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="2c1b9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="2c1b9-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="2c1b9-108">說明</span><span class="sxs-lookup"><span data-stu-id="2c1b9-108">DESCRIPTION</span></span>
<span data-ttu-id="2c1b9-109">**AzureRmDataFactoryV2IntegrationRuntime** Cmdlet 會啟動受管理的專用整合式執行時間。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="2c1b9-110">資源已在作業狀態為「已啟動」的情況下進行預配。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="2c1b9-111">示例</span><span class="sxs-lookup"><span data-stu-id="2c1b9-111">EXAMPLES</span></span>

### <span data-ttu-id="2c1b9-112">範例1：啟動整合執行時間</span><span class="sxs-lookup"><span data-stu-id="2c1b9-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="2c1b9-113">這個 Cmdlet 會啟動一個名為「測試專用-ir」的 managed 專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="2c1b9-114">參數</span><span class="sxs-lookup"><span data-stu-id="2c1b9-114">PARAMETERS</span></span>

### <span data-ttu-id="2c1b9-115">-確認</span><span class="sxs-lookup"><span data-stu-id="2c1b9-115">-Confirm</span></span>
<span data-ttu-id="2c1b9-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c1b9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2c1b9-117">-DataFactoryName</span></span>
<span data-ttu-id="2c1b9-118">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-118">The data factory name.</span></span>

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

### <span data-ttu-id="2c1b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="2c1b9-119">-Force</span></span>
<span data-ttu-id="2c1b9-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2c1b9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c1b9-121">-InputObject</span></span>
<span data-ttu-id="2c1b9-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="2c1b9-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c1b9-123">-Name</span></span>
<span data-ttu-id="2c1b9-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="2c1b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="2c1b9-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-126">The resource group name.</span></span>

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

### <span data-ttu-id="2c1b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c1b9-127">-ResourceId</span></span>
<span data-ttu-id="2c1b9-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2c1b9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1b9-129">-WhatIf</span></span>
<span data-ttu-id="2c1b9-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="2c1b9-131">輸入</span><span class="sxs-lookup"><span data-stu-id="2c1b9-131">INPUTS</span></span>

### <span data-ttu-id="2c1b9-132">System.object</span><span class="sxs-lookup"><span data-stu-id="2c1b9-132">System.String</span></span>
<span data-ttu-id="2c1b9-133">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="2c1b9-134">輸出</span><span class="sxs-lookup"><span data-stu-id="2c1b9-134">OUTPUTS</span></span>

### <span data-ttu-id="2c1b9-135">PSManagedIntegrationRuntimeStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="2c1b9-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="2c1b9-136">筆記</span><span class="sxs-lookup"><span data-stu-id="2c1b9-136">NOTES</span></span>

## <span data-ttu-id="2c1b9-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c1b9-137">RELATED LINKS</span></span>
[<span data-ttu-id="2c1b9-138">停止 AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c1b9-138">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
