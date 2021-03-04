---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: fa9e9e0b2de02a320cb5140aac21e30f7c2b5bbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916181"
---
# <span data-ttu-id="63cb6-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63cb6-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="63cb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="63cb6-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="63cb6-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="63cb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="63cb6-104">SYNTAX</span></span>

### <span data-ttu-id="63cb6-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="63cb6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cb6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63cb6-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63cb6-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="63cb6-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63cb6-108">描述</span><span class="sxs-lookup"><span data-stu-id="63cb6-108">DESCRIPTION</span></span>
<span data-ttu-id="63cb6-109">**Update-AzDataFactoryV2 RuntimeRuntime** Cmdlet 會更新整合執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="63cb6-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="63cb6-110">目前，Cmdlet 僅支援更新自我託管整合執行時間的 'AutoUpdate' 和 'AutoUpdateDelayOffset'。</span><span class="sxs-lookup"><span data-stu-id="63cb6-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="63cb6-111">例子</span><span class="sxs-lookup"><span data-stu-id="63cb6-111">EXAMPLES</span></span>

### <span data-ttu-id="63cb6-112">範例 1：更新整合執行時間</span><span class="sxs-lookup"><span data-stu-id="63cb6-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzDataFactoryV2IntegrationRuntime `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -Name 'test-selfhost-ir' `
    -AutoUpdate Off `
    -AutoUpdateDelayOffset $ts

Nodes                     : {Node_1}
CreateTime                : 11/18/2017 2:45:38 PM
InternalChannelEncryption : 
Version                   : 3.2.6519.3
Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
ScheduledUpdateDate       : 
UpdateDelayOffset         : 
LocalTimeZoneOffset       : 
AutoUpdate                : Off
ServiceUrls               : {wu.frontend.int.clouddatahub-int.net, *.servicebus.windows.net}
State                     : Online
Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
Type                      : SelfHosted
ResourceGroupName         : rg-test-dfv2
DataFactoryName           : test-df-eu2
Name                      : test-selfhost-ir
Description               : New 2 description
```

<span data-ttu-id="63cb6-113">Cmdlet 會更新名為'test-selfhost-ir'的自我託管整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="63cb6-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="63cb6-114">參數</span><span class="sxs-lookup"><span data-stu-id="63cb6-114">PARAMETERS</span></span>

### <span data-ttu-id="63cb6-115">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="63cb6-115">-AutoUpdate</span></span>
<span data-ttu-id="63cb6-116">啟用或停用自行託管的整合執行時間自動更新。</span><span class="sxs-lookup"><span data-stu-id="63cb6-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: On, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63cb6-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="63cb6-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="63cb6-118">自我託管整合執行時間自動更新的一天中小時的時間。</span><span class="sxs-lookup"><span data-stu-id="63cb6-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63cb6-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63cb6-119">-DataFactoryName</span></span>
<span data-ttu-id="63cb6-120">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="63cb6-120">The data factory name.</span></span>

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

### <span data-ttu-id="63cb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63cb6-121">-DefaultProfile</span></span>
<span data-ttu-id="63cb6-122">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="63cb6-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63cb6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63cb6-123">-InputObject</span></span>
<span data-ttu-id="63cb6-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="63cb6-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="63cb6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="63cb6-125">-Name</span></span>
<span data-ttu-id="63cb6-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="63cb6-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="63cb6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63cb6-127">-ResourceGroupName</span></span>
<span data-ttu-id="63cb6-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="63cb6-128">The resource group name.</span></span>

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

### <span data-ttu-id="63cb6-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63cb6-129">-ResourceId</span></span>
<span data-ttu-id="63cb6-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="63cb6-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="63cb6-131">-確認</span><span class="sxs-lookup"><span data-stu-id="63cb6-131">-Confirm</span></span>
<span data-ttu-id="63cb6-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63cb6-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63cb6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63cb6-133">-WhatIf</span></span>
<span data-ttu-id="63cb6-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63cb6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63cb6-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63cb6-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63cb6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63cb6-136">CommonParameters</span></span>
<span data-ttu-id="63cb6-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63cb6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63cb6-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63cb6-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63cb6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="63cb6-139">INPUTS</span></span>

### <span data-ttu-id="63cb6-140">System.String</span><span class="sxs-lookup"><span data-stu-id="63cb6-140">System.String</span></span>

### <span data-ttu-id="63cb6-141">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="63cb6-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63cb6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="63cb6-142">OUTPUTS</span></span>

### <span data-ttu-id="63cb6-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHosted方格RuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="63cb6-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="63cb6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="63cb6-144">NOTES</span></span>
<span data-ttu-id="63cb6-145">關鍵字：azure、azurerm、arm、資源、管理、管理員、資料、專案、複製、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="63cb6-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="63cb6-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="63cb6-146">RELATED LINKS</span></span>

<span data-ttu-id="63cb6-147">[Set-AzDataFactoryV2FactoryRuntime]() 
[Get-AzDataFactoryV2FactoryRuntime]()</span><span class="sxs-lookup"><span data-stu-id="63cb6-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

