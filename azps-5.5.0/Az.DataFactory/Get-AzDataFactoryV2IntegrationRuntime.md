---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141075"
---
# <span data-ttu-id="39624-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39624-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="39624-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39624-102">SYNOPSIS</span></span>
<span data-ttu-id="39624-103">取得有關整合執行時間資源的資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="39624-104">句法</span><span class="sxs-lookup"><span data-stu-id="39624-104">SYNTAX</span></span>

### <span data-ttu-id="39624-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="39624-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39624-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="39624-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39624-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="39624-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39624-108">說明</span><span class="sxs-lookup"><span data-stu-id="39624-108">DESCRIPTION</span></span>
<span data-ttu-id="39624-109">Get-AzDataFactoryV2IntegrationRuntime Cmdlet 會在資料工廠中取得整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="39624-110">如果您指定整合執行時間的名稱，此 Cmdlet 會取得該整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="39624-111">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="39624-112">示例</span><span class="sxs-lookup"><span data-stu-id="39624-112">EXAMPLES</span></span>

### <span data-ttu-id="39624-113">範例1：列出資料工廠中的所有整合執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="39624-114">列出資料工廠中名為「test-eu2」的所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="39624-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="39624-115">範例2：取得受管理的專用整合執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-115">Example 2: Get managed dedicated integration runtime</span></span>
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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="39624-116">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="39624-117">範例3：取得詳細資訊的受管理專用集成執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="39624-118">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="39624-119">範例4：取得自託管的整合執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="39624-120">這個命令會在名為「rg-test-dfv2」的資源群組或名為「test-eu2」的資料工廠的訂閱中，顯示名為「測試專用-ir」的整合執行時間的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="39624-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="39624-121">範例5：取得含詳細資料狀態的自託管集成執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="39624-122">參數</span><span class="sxs-lookup"><span data-stu-id="39624-122">PARAMETERS</span></span>

### <span data-ttu-id="39624-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="39624-123">-DataFactoryName</span></span>
<span data-ttu-id="39624-124">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="39624-124">The data factory name.</span></span>

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

### <span data-ttu-id="39624-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39624-125">-DefaultProfile</span></span>
<span data-ttu-id="39624-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39624-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39624-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39624-127">-InputObject</span></span>
<span data-ttu-id="39624-128">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="39624-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="39624-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="39624-129">-Name</span></span>
<span data-ttu-id="39624-130">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="39624-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="39624-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39624-131">-ResourceGroupName</span></span>
<span data-ttu-id="39624-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39624-132">The resource group name.</span></span>

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

### <span data-ttu-id="39624-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39624-133">-ResourceId</span></span>
<span data-ttu-id="39624-134">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="39624-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="39624-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="39624-135">-Status</span></span>
<span data-ttu-id="39624-136">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="39624-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="39624-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39624-137">CommonParameters</span></span>
<span data-ttu-id="39624-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39624-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39624-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39624-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39624-140">輸入</span><span class="sxs-lookup"><span data-stu-id="39624-140">INPUTS</span></span>

### <span data-ttu-id="39624-141">System.object</span><span class="sxs-lookup"><span data-stu-id="39624-141">System.String</span></span>

### <span data-ttu-id="39624-142">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="39624-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="39624-143">輸出</span><span class="sxs-lookup"><span data-stu-id="39624-143">OUTPUTS</span></span>

### <span data-ttu-id="39624-144">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="39624-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="39624-145">PSManagedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="39624-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="39624-146">PSSelfHostedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="39624-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="39624-147">PSLinkedIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="39624-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="39624-148">筆記</span><span class="sxs-lookup"><span data-stu-id="39624-148">NOTES</span></span>
<span data-ttu-id="39624-149">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="39624-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="39624-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="39624-150">RELATED LINKS</span></span>

[<span data-ttu-id="39624-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39624-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="39624-152">移除-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="39624-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
