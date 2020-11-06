---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613004"
---
# <span data-ttu-id="4be8f-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4be8f-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4be8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4be8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4be8f-103">取得有關整合執行時間資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="4be8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4be8f-104">SYNTAX</span></span>

### <span data-ttu-id="4be8f-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="4be8f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4be8f-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4be8f-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be8f-108">說明</span><span class="sxs-lookup"><span data-stu-id="4be8f-108">DESCRIPTION</span></span>
<span data-ttu-id="4be8f-109">Get-AzDataFactoryV2IntegrationRuntime Cmdlet 會在資料工廠中取得整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="4be8f-110">如果您指定整合執行時間的名稱，此 Cmdlet 會取得該整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="4be8f-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="4be8f-112">示例</span><span class="sxs-lookup"><span data-stu-id="4be8f-112">EXAMPLES</span></span>

### <span data-ttu-id="4be8f-113">範例1：列出資料工廠中的所有整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4be8f-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="4be8f-114">列出資料工廠中名為「test-eu2」的所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="4be8f-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4be8f-115">範例2：取得受管理的專用整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4be8f-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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

<span data-ttu-id="4be8f-116">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4be8f-117">範例3：取得詳細資訊的受管理專用集成執行時間</span><span class="sxs-lookup"><span data-stu-id="4be8f-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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

<span data-ttu-id="4be8f-118">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="4be8f-119">範例4：取得自託管的整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4be8f-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="4be8f-120">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4be8f-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="4be8f-121">參數</span><span class="sxs-lookup"><span data-stu-id="4be8f-121">PARAMETERS</span></span>

### <span data-ttu-id="4be8f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4be8f-122">-DataFactoryName</span></span>
<span data-ttu-id="4be8f-123">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="4be8f-123">The data factory name.</span></span>

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

### <span data-ttu-id="4be8f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be8f-124">-DefaultProfile</span></span>
<span data-ttu-id="4be8f-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4be8f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4be8f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4be8f-126">-InputObject</span></span>
<span data-ttu-id="4be8f-127">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="4be8f-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="4be8f-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="4be8f-128">-Name</span></span>
<span data-ttu-id="4be8f-129">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="4be8f-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4be8f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4be8f-130">-ResourceGroupName</span></span>
<span data-ttu-id="4be8f-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4be8f-131">The resource group name.</span></span>

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

### <span data-ttu-id="4be8f-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4be8f-132">-ResourceId</span></span>
<span data-ttu-id="4be8f-133">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4be8f-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4be8f-134">-狀態</span><span class="sxs-lookup"><span data-stu-id="4be8f-134">-Status</span></span>
<span data-ttu-id="4be8f-135">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="4be8f-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="4be8f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be8f-136">CommonParameters</span></span>
<span data-ttu-id="4be8f-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4be8f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be8f-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4be8f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be8f-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4be8f-139">INPUTS</span></span>

### <span data-ttu-id="4be8f-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4be8f-140">System.String</span></span>

### <span data-ttu-id="4be8f-141">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4be8f-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4be8f-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4be8f-142">OUTPUTS</span></span>

### <span data-ttu-id="4be8f-143">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4be8f-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="4be8f-144">PSManagedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4be8f-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="4be8f-145">PSSelfHostedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4be8f-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="4be8f-146">PSLinkedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="4be8f-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="4be8f-147">筆記</span><span class="sxs-lookup"><span data-stu-id="4be8f-147">NOTES</span></span>
<span data-ttu-id="4be8f-148">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="4be8f-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4be8f-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="4be8f-149">RELATED LINKS</span></span>

[<span data-ttu-id="4be8f-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4be8f-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4be8f-151">移除-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4be8f-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
