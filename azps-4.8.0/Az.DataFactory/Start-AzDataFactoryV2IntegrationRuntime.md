---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128779"
---
# <span data-ttu-id="ad46f-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ad46f-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="ad46f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad46f-102">SYNOPSIS</span></span>
<span data-ttu-id="ad46f-103">啟動受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ad46f-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="ad46f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad46f-104">SYNTAX</span></span>

### <span data-ttu-id="ad46f-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="ad46f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad46f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad46f-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad46f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="ad46f-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad46f-108">說明</span><span class="sxs-lookup"><span data-stu-id="ad46f-108">DESCRIPTION</span></span>
<span data-ttu-id="ad46f-109">**AzDataFactoryV2IntegrationRuntime** Cmdlet 會啟動受管理的專用整合式執行時間。</span><span class="sxs-lookup"><span data-stu-id="ad46f-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="ad46f-110">資源已在作業狀態為「已啟動」的情況下進行預配。</span><span class="sxs-lookup"><span data-stu-id="ad46f-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="ad46f-111">示例</span><span class="sxs-lookup"><span data-stu-id="ad46f-111">EXAMPLES</span></span>

### <span data-ttu-id="ad46f-112">範例1：啟動整合執行時間</span><span class="sxs-lookup"><span data-stu-id="ad46f-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

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
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="ad46f-113">這個 Cmdlet 會啟動一個名為「測試專用-ir」的 managed 專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="ad46f-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="ad46f-114">參數</span><span class="sxs-lookup"><span data-stu-id="ad46f-114">PARAMETERS</span></span>

### <span data-ttu-id="ad46f-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ad46f-115">-DataFactoryName</span></span>
<span data-ttu-id="ad46f-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="ad46f-116">The data factory name.</span></span>

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

### <span data-ttu-id="ad46f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad46f-117">-DefaultProfile</span></span>
<span data-ttu-id="ad46f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad46f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad46f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ad46f-119">-Force</span></span>
<span data-ttu-id="ad46f-120">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad46f-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ad46f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad46f-121">-InputObject</span></span>
<span data-ttu-id="ad46f-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="ad46f-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="ad46f-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad46f-123">-Name</span></span>
<span data-ttu-id="ad46f-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="ad46f-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="ad46f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad46f-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad46f-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad46f-126">The resource group name.</span></span>

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

### <span data-ttu-id="ad46f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad46f-127">-ResourceId</span></span>
<span data-ttu-id="ad46f-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ad46f-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ad46f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ad46f-129">-Confirm</span></span>
<span data-ttu-id="ad46f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ad46f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad46f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad46f-131">-WhatIf</span></span>
<span data-ttu-id="ad46f-132">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ad46f-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ad46f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad46f-133">CommonParameters</span></span>
<span data-ttu-id="ad46f-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad46f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad46f-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad46f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad46f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ad46f-136">INPUTS</span></span>

### <span data-ttu-id="ad46f-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ad46f-137">System.String</span></span>

### <span data-ttu-id="ad46f-138">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="ad46f-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ad46f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ad46f-139">OUTPUTS</span></span>

### <span data-ttu-id="ad46f-140">PSManagedIntegrationRuntimeStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="ad46f-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="ad46f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ad46f-141">NOTES</span></span>

## <span data-ttu-id="ad46f-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad46f-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad46f-143">停止 AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ad46f-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
