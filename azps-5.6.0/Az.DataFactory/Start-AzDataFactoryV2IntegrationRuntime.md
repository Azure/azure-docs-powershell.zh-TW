---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: eeb0db5c9dd180d8194d0bd506296f269c6c5386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905146"
---
# <span data-ttu-id="63891-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63891-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="63891-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63891-102">SYNOPSIS</span></span>
<span data-ttu-id="63891-103">啟動受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="63891-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="63891-104">語法</span><span class="sxs-lookup"><span data-stu-id="63891-104">SYNTAX</span></span>

### <span data-ttu-id="63891-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="63891-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63891-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63891-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63891-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="63891-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63891-108">描述</span><span class="sxs-lookup"><span data-stu-id="63891-108">DESCRIPTION</span></span>
<span data-ttu-id="63891-109">**Start-AzDataFactoryV2 RuntimeRuntime** Cmdlet 會啟動受管理的專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="63891-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="63891-110">資源已配置完成，且作業之後的狀態為'開始」。</span><span class="sxs-lookup"><span data-stu-id="63891-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="63891-111">例子</span><span class="sxs-lookup"><span data-stu-id="63891-111">EXAMPLES</span></span>

### <span data-ttu-id="63891-112">範例 1：啟動整合執行時間</span><span class="sxs-lookup"><span data-stu-id="63891-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="63891-113">此 Cmdlet 會啟動名為"test-dedicated-ir"的受管理專用整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="63891-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="63891-114">參數</span><span class="sxs-lookup"><span data-stu-id="63891-114">PARAMETERS</span></span>

### <span data-ttu-id="63891-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63891-115">-DataFactoryName</span></span>
<span data-ttu-id="63891-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="63891-116">The data factory name.</span></span>

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

### <span data-ttu-id="63891-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63891-117">-DefaultProfile</span></span>
<span data-ttu-id="63891-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63891-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63891-119">-強制</span><span class="sxs-lookup"><span data-stu-id="63891-119">-Force</span></span>
<span data-ttu-id="63891-120">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="63891-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="63891-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63891-121">-InputObject</span></span>
<span data-ttu-id="63891-122">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="63891-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="63891-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="63891-123">-Name</span></span>
<span data-ttu-id="63891-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="63891-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="63891-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63891-125">-ResourceGroupName</span></span>
<span data-ttu-id="63891-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="63891-126">The resource group name.</span></span>

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

### <span data-ttu-id="63891-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63891-127">-ResourceId</span></span>
<span data-ttu-id="63891-128">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="63891-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="63891-129">-確認</span><span class="sxs-lookup"><span data-stu-id="63891-129">-Confirm</span></span>
<span data-ttu-id="63891-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63891-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63891-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63891-131">-WhatIf</span></span>
<span data-ttu-id="63891-132">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63891-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="63891-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63891-133">CommonParameters</span></span>
<span data-ttu-id="63891-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63891-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63891-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63891-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63891-136">輸入</span><span class="sxs-lookup"><span data-stu-id="63891-136">INPUTS</span></span>

### <span data-ttu-id="63891-137">System.String</span><span class="sxs-lookup"><span data-stu-id="63891-137">System.String</span></span>

### <span data-ttu-id="63891-138">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="63891-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63891-139">輸出</span><span class="sxs-lookup"><span data-stu-id="63891-139">OUTPUTS</span></span>

### <span data-ttu-id="63891-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSManagedFactorRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="63891-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="63891-141">筆記</span><span class="sxs-lookup"><span data-stu-id="63891-141">NOTES</span></span>

## <span data-ttu-id="63891-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="63891-142">RELATED LINKS</span></span>

[<span data-ttu-id="63891-143">Stop-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="63891-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
