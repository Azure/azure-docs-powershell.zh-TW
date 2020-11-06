---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fd6e979b753bd5fea21af050492b194326122a1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455456"
---
# <span data-ttu-id="bf6e9-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf6e9-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="bf6e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="bf6e9-103">取得有關整合執行時間資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf6e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf6e9-104">SYNTAX</span></span>

### <span data-ttu-id="bf6e9-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="bf6e9-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf6e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bf6e9-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf6e9-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="bf6e9-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf6e9-108">說明</span><span class="sxs-lookup"><span data-stu-id="bf6e9-108">DESCRIPTION</span></span>
<span data-ttu-id="bf6e9-109">Get-AzureRmDataFactoryV2IntegrationRuntime Cmdlet 會在資料工廠中取得整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="bf6e9-110">如果您指定整合執行時間的名稱，此 Cmdlet 會取得該整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="bf6e9-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="bf6e9-112">示例</span><span class="sxs-lookup"><span data-stu-id="bf6e9-112">EXAMPLES</span></span>

### <span data-ttu-id="bf6e9-113">範例1：列出資料工廠中的所有整合執行時間</span><span class="sxs-lookup"><span data-stu-id="bf6e9-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="bf6e9-114">列出資料工廠中名為「test-eu2」的所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf6e9-115">範例2：取得受管理的專用整合執行時間</span><span class="sxs-lookup"><span data-stu-id="bf6e9-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="bf6e9-116">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf6e9-117">範例3：取得詳細資訊的受管理專用集成執行時間</span><span class="sxs-lookup"><span data-stu-id="bf6e9-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="bf6e9-118">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="bf6e9-119">範例4：取得自託管的整合執行時間</span><span class="sxs-lookup"><span data-stu-id="bf6e9-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="bf6e9-120">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="bf6e9-121">參數</span><span class="sxs-lookup"><span data-stu-id="bf6e9-121">PARAMETERS</span></span>

### <span data-ttu-id="bf6e9-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf6e9-122">-DataFactoryName</span></span>
<span data-ttu-id="bf6e9-123">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-123">The data factory name.</span></span>

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

### <span data-ttu-id="bf6e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf6e9-124">-DefaultProfile</span></span>
<span data-ttu-id="bf6e9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf6e9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf6e9-126">-InputObject</span></span>
<span data-ttu-id="bf6e9-127">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="bf6e9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="bf6e9-128">-Name</span></span>
<span data-ttu-id="bf6e9-129">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-129">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf6e9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf6e9-130">-ResourceGroupName</span></span>
<span data-ttu-id="bf6e9-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-131">The resource group name.</span></span>

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

### <span data-ttu-id="bf6e9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf6e9-132">-ResourceId</span></span>
<span data-ttu-id="bf6e9-133">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="bf6e9-134">-狀態</span><span class="sxs-lookup"><span data-stu-id="bf6e9-134">-Status</span></span>
<span data-ttu-id="bf6e9-135">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="bf6e9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf6e9-136">CommonParameters</span></span>
<span data-ttu-id="bf6e9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf6e9-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf6e9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bf6e9-139">INPUTS</span></span>

### <span data-ttu-id="bf6e9-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bf6e9-140">System.String</span></span>
<span data-ttu-id="bf6e9-141">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="bf6e9-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="bf6e9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bf6e9-142">OUTPUTS</span></span>

### <span data-ttu-id="bf6e9-143">[System.object]。清單 ' 1 [DataFactoryV2. PSIntegrationRuntime，DataFactoryV2，版本 = 0.1.9.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="bf6e9-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="bf6e9-144">DataFactoryV2 PSManagedIntegrationRuntime DataFactoryV2..... PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf6e9-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

## <span data-ttu-id="bf6e9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="bf6e9-145">NOTES</span></span>
<span data-ttu-id="bf6e9-146">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="bf6e9-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="bf6e9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf6e9-147">RELATED LINKS</span></span>

[<span data-ttu-id="bf6e9-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf6e9-148">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="bf6e9-149">移除-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="bf6e9-149">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
