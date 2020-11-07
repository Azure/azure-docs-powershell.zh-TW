---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: d2177e2ca7705f579921b9e2eb9fc64ab0e0c33a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788073"
---
# <span data-ttu-id="51b89-101">Update-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="51b89-101">Update-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="51b89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="51b89-102">SYNOPSIS</span></span>
<span data-ttu-id="51b89-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="51b89-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="51b89-104">句法</span><span class="sxs-lookup"><span data-stu-id="51b89-104">SYNTAX</span></span>

### <span data-ttu-id="51b89-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="51b89-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b89-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="51b89-106">ByResourceId</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51b89-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="51b89-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51b89-108">說明</span><span class="sxs-lookup"><span data-stu-id="51b89-108">DESCRIPTION</span></span>
<span data-ttu-id="51b89-109">**更新-AzDataFactoryV2IntegrationRuntime** Cmdlet 會更新整合執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="51b89-109">The **Update-AzDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="51b89-110">目前這個 Cmdlet 只支援針對自行託管的執行時間更新「自動更新」和「AutoUpdateDelayOffset」。</span><span class="sxs-lookup"><span data-stu-id="51b89-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="51b89-111">示例</span><span class="sxs-lookup"><span data-stu-id="51b89-111">EXAMPLES</span></span>

### <span data-ttu-id="51b89-112">範例1：更新整合執行時間</span><span class="sxs-lookup"><span data-stu-id="51b89-112">Example 1: Updates an integration runtime</span></span>
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

<span data-ttu-id="51b89-113">此 Cmdlet 會更新名為「test-selfhost-ir」的自託管集成執行時間。</span><span class="sxs-lookup"><span data-stu-id="51b89-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="51b89-114">參數</span><span class="sxs-lookup"><span data-stu-id="51b89-114">PARAMETERS</span></span>

### <span data-ttu-id="51b89-115">-自動更新</span><span class="sxs-lookup"><span data-stu-id="51b89-115">-AutoUpdate</span></span>
<span data-ttu-id="51b89-116">啟用或停用自託管的集成執行時間自動更新。</span><span class="sxs-lookup"><span data-stu-id="51b89-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="51b89-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="51b89-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="51b89-118">自託管整合執行時間自動更新之當天的時間（小時）。</span><span class="sxs-lookup"><span data-stu-id="51b89-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="51b89-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="51b89-119">-DataFactoryName</span></span>
<span data-ttu-id="51b89-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="51b89-120">The data factory name.</span></span>

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

### <span data-ttu-id="51b89-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51b89-121">-DefaultProfile</span></span>
<span data-ttu-id="51b89-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="51b89-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51b89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51b89-123">-InputObject</span></span>
<span data-ttu-id="51b89-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="51b89-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="51b89-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="51b89-125">-Name</span></span>
<span data-ttu-id="51b89-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="51b89-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="51b89-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51b89-127">-ResourceGroupName</span></span>
<span data-ttu-id="51b89-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="51b89-128">The resource group name.</span></span>

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

### <span data-ttu-id="51b89-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51b89-129">-ResourceId</span></span>
<span data-ttu-id="51b89-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="51b89-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="51b89-131">-確認</span><span class="sxs-lookup"><span data-stu-id="51b89-131">-Confirm</span></span>
<span data-ttu-id="51b89-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="51b89-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51b89-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51b89-133">-WhatIf</span></span>
<span data-ttu-id="51b89-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51b89-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51b89-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51b89-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51b89-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51b89-136">CommonParameters</span></span>
<span data-ttu-id="51b89-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="51b89-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51b89-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="51b89-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51b89-139">輸入</span><span class="sxs-lookup"><span data-stu-id="51b89-139">INPUTS</span></span>

### <span data-ttu-id="51b89-140">System.object</span><span class="sxs-lookup"><span data-stu-id="51b89-140">System.String</span></span>

### <span data-ttu-id="51b89-141">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="51b89-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="51b89-142">輸出</span><span class="sxs-lookup"><span data-stu-id="51b89-142">OUTPUTS</span></span>

### <span data-ttu-id="51b89-143">PSSelfHostedIntegrationRuntimeStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="51b89-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="51b89-144">筆記</span><span class="sxs-lookup"><span data-stu-id="51b89-144">NOTES</span></span>
<span data-ttu-id="51b89-145">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="51b89-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="51b89-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="51b89-146">RELATED LINKS</span></span>

<span data-ttu-id="51b89-147">[Set-AzDataFactoryV2IntegrationRuntime]() 
[AzDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="51b89-147">[Set-AzDataFactoryV2IntegrationRuntime]()
[Get-AzDataFactoryV2IntegrationRuntime]()</span></span>

