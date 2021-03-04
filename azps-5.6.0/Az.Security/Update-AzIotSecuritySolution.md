---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: aec6fb98b5894b075cea7cf9b087b9f9c042779a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915882"
---
# <span data-ttu-id="f9acd-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f9acd-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="f9acd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9acd-102">SYNOPSIS</span></span>
<span data-ttu-id="f9acd-103">在 IoT 安全性解決方案中更新下列一或多個屬性：標記、建議組配置、使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="f9acd-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="f9acd-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9acd-104">SYNTAX</span></span>

### <span data-ttu-id="f9acd-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f9acd-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9acd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9acd-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9acd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f9acd-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9acd-108">描述</span><span class="sxs-lookup"><span data-stu-id="f9acd-108">DESCRIPTION</span></span>
<span data-ttu-id="f9acd-109">Cmdlet Update-AzIotSecuritySolution特定 IoT 安全性解決方案中的一或多個屬性：標籤、建議群組原則、使用者定義資源。</span><span class="sxs-lookup"><span data-stu-id="f9acd-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="f9acd-110">只有指定的屬性會更新到 iot 安全性解決方案中。</span><span class="sxs-lookup"><span data-stu-id="f9acd-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="f9acd-111">IoT 安全性解決方案會收集 iot 裝置和 iot 中樞的安全性資料和事件，協助防範和偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="f9acd-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="f9acd-112">例子</span><span class="sxs-lookup"><span data-stu-id="f9acd-112">EXAMPLES</span></span>

### <span data-ttu-id="f9acd-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="f9acd-113">Example 1</span></span>
```powershell
PS C:\> $RecConfig = New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_OpenPorts" -Enabled $false
PS C:\> $UserDefinedResource = New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")   
PS C:\> Update-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -RecommendationsConfiguration @($RecConfig) -UserDefinedResource $UserDefinedResource

Id: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/IoTSecuritySolutions/MySample"
Name: "MySample"
Type: "Microsoft.Security/IoTSecuritySolutions"
Location: "westus"
DisplayName: "MySample"
status: "Enabled"
Export: ["RawEvents"]
DisabledDataSources: ["TwinData"]
Workspace: "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.operationalinsights/workspaces/MyLA"
AdditionalWorkspaces: null
IotHubs: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UserDefinedResources: {
    Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
    QuerySubscriptions: ["XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"]
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_OpenPorts"
    Name: "Device has open port"
    Status: "Disabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
}]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
```

<span data-ttu-id="f9acd-114">從資源群組 "MyResourceGroup" 更新 iot 安全性解決方案 「MySample」，並包含建議組和使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="f9acd-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="f9acd-115">參數</span><span class="sxs-lookup"><span data-stu-id="f9acd-115">PARAMETERS</span></span>

### <span data-ttu-id="f9acd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9acd-116">-DefaultProfile</span></span>
<span data-ttu-id="f9acd-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9acd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9acd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9acd-118">-InputObject</span></span>
<span data-ttu-id="f9acd-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="f9acd-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9acd-120">-Name</span></span>
<span data-ttu-id="f9acd-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f9acd-121">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9acd-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="f9acd-123">建議組配置。</span><span class="sxs-lookup"><span data-stu-id="f9acd-123">Recommendations configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9acd-124">-ResourceGroupName</span></span>
<span data-ttu-id="f9acd-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f9acd-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9acd-126">-ResourceId</span></span>
<span data-ttu-id="f9acd-127">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9acd-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-128">-標記</span><span class="sxs-lookup"><span data-stu-id="f9acd-128">-Tag</span></span>
<span data-ttu-id="f9acd-129">標籤。</span><span class="sxs-lookup"><span data-stu-id="f9acd-129">Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="f9acd-130">-UserDefinedResource</span></span>
<span data-ttu-id="f9acd-131">使用者定義的資源。</span><span class="sxs-lookup"><span data-stu-id="f9acd-131">User defined resources.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9acd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f9acd-132">-Confirm</span></span>
<span data-ttu-id="f9acd-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9acd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9acd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9acd-134">-WhatIf</span></span>
<span data-ttu-id="f9acd-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9acd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9acd-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9acd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9acd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9acd-137">CommonParameters</span></span>
<span data-ttu-id="f9acd-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9acd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9acd-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9acd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9acd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f9acd-140">INPUTS</span></span>

### <span data-ttu-id="f9acd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f9acd-141">System.String</span></span>

### <span data-ttu-id="f9acd-142">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f9acd-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="f9acd-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9acd-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f9acd-144">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="f9acd-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="f9acd-145">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="f9acd-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="f9acd-146">輸出</span><span class="sxs-lookup"><span data-stu-id="f9acd-146">OUTPUTS</span></span>

### <span data-ttu-id="f9acd-147">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f9acd-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="f9acd-148">筆記</span><span class="sxs-lookup"><span data-stu-id="f9acd-148">NOTES</span></span>

## <span data-ttu-id="f9acd-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9acd-149">RELATED LINKS</span></span>
