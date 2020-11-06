---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 2c20752dd1e29962f128f687344b3b165f0a09ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449196"
---
# <span data-ttu-id="00126-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="00126-101">Update-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="00126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="00126-102">SYNOPSIS</span></span>
<span data-ttu-id="00126-103">更新整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="00126-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00126-104">句法</span><span class="sxs-lookup"><span data-stu-id="00126-104">SYNTAX</span></span>

### <span data-ttu-id="00126-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="00126-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00126-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00126-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00126-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="00126-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntime [-AutoUpdate <String>] [-AutoUpdateDelayOffset <TimeSpan>]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00126-108">說明</span><span class="sxs-lookup"><span data-stu-id="00126-108">DESCRIPTION</span></span>
<span data-ttu-id="00126-109">**更新-AzureRmDataFactoryV2IntegrationRuntime** Cmdlet 會更新整合執行時間屬性。</span><span class="sxs-lookup"><span data-stu-id="00126-109">The **Update-AzureRmDataFactoryV2IntegrationRuntime** cmdlet updates integration runtime properties.</span></span> <span data-ttu-id="00126-110">目前這個 Cmdlet 只支援針對自行託管的執行時間更新「自動更新」和「AutoUpdateDelayOffset」。</span><span class="sxs-lookup"><span data-stu-id="00126-110">Currently the cmdlet only supports updating 'AutoUpdate' and 'AutoUpdateDelayOffset' for self-hosted integration runtime.</span></span>

## <span data-ttu-id="00126-111">示例</span><span class="sxs-lookup"><span data-stu-id="00126-111">EXAMPLES</span></span>

### <span data-ttu-id="00126-112">範例1：更新整合執行時間</span><span class="sxs-lookup"><span data-stu-id="00126-112">Example 1: Updates an integration runtime</span></span>
```
PS C:\> $ts = New-TimeSpan -Hours 3
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntime `
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

<span data-ttu-id="00126-113">此 Cmdlet 會更新名為「test-selfhost-ir」的自託管集成執行時間。</span><span class="sxs-lookup"><span data-stu-id="00126-113">The cmdlet updates self-hosted integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="00126-114">參數</span><span class="sxs-lookup"><span data-stu-id="00126-114">PARAMETERS</span></span>

### <span data-ttu-id="00126-115">-自動更新</span><span class="sxs-lookup"><span data-stu-id="00126-115">-AutoUpdate</span></span>
<span data-ttu-id="00126-116">啟用或停用自託管的集成執行時間自動更新。</span><span class="sxs-lookup"><span data-stu-id="00126-116">Enable or disable the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="00126-117">-AutoUpdateDelayOffset</span><span class="sxs-lookup"><span data-stu-id="00126-117">-AutoUpdateDelayOffset</span></span>
<span data-ttu-id="00126-118">自託管整合執行時間自動更新之當天的時間（小時）。</span><span class="sxs-lookup"><span data-stu-id="00126-118">The time in hour of the day for the self-hosted integration runtime auto-update.</span></span>

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

### <span data-ttu-id="00126-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="00126-119">-DataFactoryName</span></span>
<span data-ttu-id="00126-120">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="00126-120">The data factory name.</span></span>

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

### <span data-ttu-id="00126-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00126-121">-DefaultProfile</span></span>
<span data-ttu-id="00126-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="00126-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00126-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00126-123">-InputObject</span></span>
<span data-ttu-id="00126-124">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="00126-124">The integration runtime object.</span></span>

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

### <span data-ttu-id="00126-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="00126-125">-Name</span></span>
<span data-ttu-id="00126-126">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="00126-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="00126-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00126-127">-ResourceGroupName</span></span>
<span data-ttu-id="00126-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="00126-128">The resource group name.</span></span>

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

### <span data-ttu-id="00126-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00126-129">-ResourceId</span></span>
<span data-ttu-id="00126-130">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="00126-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="00126-131">-確認</span><span class="sxs-lookup"><span data-stu-id="00126-131">-Confirm</span></span>
<span data-ttu-id="00126-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="00126-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00126-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00126-133">-WhatIf</span></span>
<span data-ttu-id="00126-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="00126-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00126-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="00126-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00126-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00126-136">CommonParameters</span></span>
<span data-ttu-id="00126-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="00126-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00126-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="00126-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00126-139">輸入</span><span class="sxs-lookup"><span data-stu-id="00126-139">INPUTS</span></span>

### <span data-ttu-id="00126-140">System.object</span><span class="sxs-lookup"><span data-stu-id="00126-140">System.String</span></span>

### <span data-ttu-id="00126-141">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="00126-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="00126-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="00126-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="00126-143">輸出</span><span class="sxs-lookup"><span data-stu-id="00126-143">OUTPUTS</span></span>

### <span data-ttu-id="00126-144">PSSelfHostedIntegrationRuntimeStatus 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="00126-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="00126-145">筆記</span><span class="sxs-lookup"><span data-stu-id="00126-145">NOTES</span></span>
<span data-ttu-id="00126-146">關鍵字： azure、azurerm、arm、資源、管理、管理員、資料、工廠、複本、活動、整合執行時間</span><span class="sxs-lookup"><span data-stu-id="00126-146">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="00126-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="00126-147">RELATED LINKS</span></span>

<span data-ttu-id="00126-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
[AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="00126-148">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

