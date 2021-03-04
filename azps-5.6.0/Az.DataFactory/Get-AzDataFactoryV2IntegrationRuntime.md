---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5997ca072ae11407500ceb254dbd16be13382ac8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907738"
---
# <span data-ttu-id="0f096-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0f096-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f096-102">SYNOPSIS</span></span>
<span data-ttu-id="0f096-103">獲得整合執行時間資源相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="0f096-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f096-104">SYNTAX</span></span>

### <span data-ttu-id="0f096-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="0f096-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f096-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f096-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f096-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0f096-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f096-108">描述</span><span class="sxs-lookup"><span data-stu-id="0f096-108">DESCRIPTION</span></span>
<span data-ttu-id="0f096-109">Cmdlet Get-AzDataFactoryV2IntegrationRuntime一個資料工廠中的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="0f096-110">如果您指定整合執行時間的名稱，此 Cmdlet 會獲得該整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="0f096-111">如果您未指定名稱，此 Cmdlet 會獲得資料工廠中所有整合執行時間的資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="0f096-112">例子</span><span class="sxs-lookup"><span data-stu-id="0f096-112">EXAMPLES</span></span>

### <span data-ttu-id="0f096-113">範例 1：列出資料工廠中所有整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="0f096-114">列出資料工廠中名為'test-df-eu2'的所有整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="0f096-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0f096-115">範例 2：取得受管理的專用整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-115">Example 2: Get managed dedicated integration runtime</span></span>
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

<span data-ttu-id="0f096-116">此命令會在名為'rg-test-dfv2'及名為'test-df-eu2'的資料工廠訂閱中顯示名為"test-dedicated-ir"的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0f096-117">範例 3：取得具有詳細狀態之受管理的專用整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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

<span data-ttu-id="0f096-118">此命令會在名為'rg-test-dfv2'及名為'test-df-eu2'的資料工廠訂閱中顯示名為"test-dedicated-ir"的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0f096-119">範例 4：取得自我託管整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="0f096-120">此命令會在名為'rg-test-dfv2'及名為'test-df-eu2'的資料工廠訂閱中顯示名為"test-dedicated-ir"的整合執行時間相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0f096-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="0f096-121">範例 5：取得具有詳細狀態之自我託管整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
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

## <span data-ttu-id="0f096-122">參數</span><span class="sxs-lookup"><span data-stu-id="0f096-122">PARAMETERS</span></span>

### <span data-ttu-id="0f096-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f096-123">-DataFactoryName</span></span>
<span data-ttu-id="0f096-124">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="0f096-124">The data factory name.</span></span>

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

### <span data-ttu-id="0f096-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f096-125">-DefaultProfile</span></span>
<span data-ttu-id="0f096-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f096-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f096-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f096-127">-InputObject</span></span>
<span data-ttu-id="0f096-128">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="0f096-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="0f096-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0f096-129">-Name</span></span>
<span data-ttu-id="0f096-130">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0f096-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="0f096-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f096-131">-ResourceGroupName</span></span>
<span data-ttu-id="0f096-132">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0f096-132">The resource group name.</span></span>

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

### <span data-ttu-id="0f096-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f096-133">-ResourceId</span></span>
<span data-ttu-id="0f096-134">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f096-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0f096-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="0f096-135">-Status</span></span>
<span data-ttu-id="0f096-136">整合執行時間詳細資料狀態。</span><span class="sxs-lookup"><span data-stu-id="0f096-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="0f096-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f096-137">CommonParameters</span></span>
<span data-ttu-id="0f096-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f096-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f096-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0f096-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f096-140">輸入</span><span class="sxs-lookup"><span data-stu-id="0f096-140">INPUTS</span></span>

### <span data-ttu-id="0f096-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0f096-141">System.String</span></span>

### <span data-ttu-id="0f096-142">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0f096-143">輸出</span><span class="sxs-lookup"><span data-stu-id="0f096-143">OUTPUTS</span></span>

### <span data-ttu-id="0f096-144">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="0f096-145">Microsoft.Azure.Commands.DataFactoryV2.models.PSManaged方格Runtime</span><span class="sxs-lookup"><span data-stu-id="0f096-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="0f096-146">Microsoft.Azure.Commands.DataFactoryV2.models.PSSelfHosted方格Runtime</span><span class="sxs-lookup"><span data-stu-id="0f096-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="0f096-147">Microsoft.Azure.Commands.DataFactoryV2.models.PSLinkedAzRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="0f096-148">筆記</span><span class="sxs-lookup"><span data-stu-id="0f096-148">NOTES</span></span>
<span data-ttu-id="0f096-149">關鍵字：azure、azurerm、arm、資源、管理、管理員、資料、專案、複製、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="0f096-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0f096-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f096-150">RELATED LINKS</span></span>

[<span data-ttu-id="0f096-151">Set-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="0f096-152">Remove-AzDataFactoryV2FactoryRuntime</span><span class="sxs-lookup"><span data-stu-id="0f096-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
