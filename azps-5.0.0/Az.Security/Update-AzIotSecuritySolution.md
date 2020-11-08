---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Update-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Update-AzIotSecuritySolution.md
ms.openlocfilehash: ba84bccc92b58b7f8a21812e2f1599bbc9679d38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137626"
---
# <span data-ttu-id="62c53-101">Update-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="62c53-101">Update-AzIotSecuritySolution</span></span>

## <span data-ttu-id="62c53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62c53-102">SYNOPSIS</span></span>
<span data-ttu-id="62c53-103">在 IoT 安全解決方案中更新下列一或多個屬性：標記、建議配置、使用者定義的資源</span><span class="sxs-lookup"><span data-stu-id="62c53-103">Update one or more of the following properties in IoT security solution: tags, recommendation configuration, user defined resources</span></span>

## <span data-ttu-id="62c53-104">句法</span><span class="sxs-lookup"><span data-stu-id="62c53-104">SYNTAX</span></span>

### <span data-ttu-id="62c53-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="62c53-105">ResourceGroupLevelResource (Default)</span></span>
```
Update-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c53-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c53-106">ResourceId</span></span>
```
Update-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c53-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="62c53-107">InputObject</span></span>
```
Update-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>]
 [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c53-108">說明</span><span class="sxs-lookup"><span data-stu-id="62c53-108">DESCRIPTION</span></span>
<span data-ttu-id="62c53-109">Update-AzIotSecuritySolution Cmdlet 在特定的 IoT 安全解決方案中 updayes 下列一或多個屬性：標記、建議配置、使用者定義資源。</span><span class="sxs-lookup"><span data-stu-id="62c53-109">The Update-AzIotSecuritySolution cmdlet updayes one or more of the following properties in a specific IoT security solution: tags, recommendation configuration, user defined resources.</span></span>
<span data-ttu-id="62c53-110">只有在 iot security 方案內，才會更新指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="62c53-110">Only the specified properties will be updated inside the iot security solution.</span></span>
<span data-ttu-id="62c53-111">IoT 安全解決方案會從 IoT 裝置和 IoT 中樞收集安全性資料和事件，以協助防範及偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="62c53-111">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="62c53-112">示例</span><span class="sxs-lookup"><span data-stu-id="62c53-112">EXAMPLES</span></span>

### <span data-ttu-id="62c53-113">範例1</span><span class="sxs-lookup"><span data-stu-id="62c53-113">Example 1</span></span>
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

<span data-ttu-id="62c53-114">使用建議設定和使用者定義的資源，更新來自資源群組 "MyResourceGroup" 的 iot 安全解決方案 "MySample"</span><span class="sxs-lookup"><span data-stu-id="62c53-114">Update iot security solution "MySample" from resource group "MyResourceGroup" with recommendation configuration and user defined resources</span></span>

## <span data-ttu-id="62c53-115">參數</span><span class="sxs-lookup"><span data-stu-id="62c53-115">PARAMETERS</span></span>

### <span data-ttu-id="62c53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c53-116">-DefaultProfile</span></span>
<span data-ttu-id="62c53-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62c53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c53-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c53-118">-InputObject</span></span>
<span data-ttu-id="62c53-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="62c53-119">Input Object.</span></span>

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

### <span data-ttu-id="62c53-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="62c53-120">-Name</span></span>
<span data-ttu-id="62c53-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="62c53-121">Resource name.</span></span>

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

### <span data-ttu-id="62c53-122">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c53-122">-RecommendationsConfiguration</span></span>
<span data-ttu-id="62c53-123">建議配置。</span><span class="sxs-lookup"><span data-stu-id="62c53-123">Recommendations configuration.</span></span>

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

### <span data-ttu-id="62c53-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c53-124">-ResourceGroupName</span></span>
<span data-ttu-id="62c53-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="62c53-125">Resource group name.</span></span>

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

### <span data-ttu-id="62c53-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c53-126">-ResourceId</span></span>
<span data-ttu-id="62c53-127">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="62c53-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="62c53-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="62c53-128">-Tag</span></span>
<span data-ttu-id="62c53-129">間.</span><span class="sxs-lookup"><span data-stu-id="62c53-129">Tags.</span></span>

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

### <span data-ttu-id="62c53-130">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="62c53-130">-UserDefinedResource</span></span>
<span data-ttu-id="62c53-131">使用者定義的資源。</span><span class="sxs-lookup"><span data-stu-id="62c53-131">User defined resources.</span></span>

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

### <span data-ttu-id="62c53-132">-確認</span><span class="sxs-lookup"><span data-stu-id="62c53-132">-Confirm</span></span>
<span data-ttu-id="62c53-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62c53-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c53-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c53-134">-WhatIf</span></span>
<span data-ttu-id="62c53-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62c53-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c53-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62c53-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c53-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c53-137">CommonParameters</span></span>
<span data-ttu-id="62c53-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62c53-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c53-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="62c53-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c53-140">輸入</span><span class="sxs-lookup"><span data-stu-id="62c53-140">INPUTS</span></span>

### <span data-ttu-id="62c53-141">System.object</span><span class="sxs-lookup"><span data-stu-id="62c53-141">System.String</span></span>

### <span data-ttu-id="62c53-142">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="62c53-142">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="62c53-143">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="62c53-143">System.Collections.Hashtable</span></span>

### <span data-ttu-id="62c53-144">PSUserDefinedResources 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="62c53-144">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="62c53-145">PSRecommendationConfiguration []. IotSecuritySolutions. []</span><span class="sxs-lookup"><span data-stu-id="62c53-145">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="62c53-146">輸出</span><span class="sxs-lookup"><span data-stu-id="62c53-146">OUTPUTS</span></span>

### <span data-ttu-id="62c53-147">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="62c53-147">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="62c53-148">筆記</span><span class="sxs-lookup"><span data-stu-id="62c53-148">NOTES</span></span>

## <span data-ttu-id="62c53-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="62c53-149">RELATED LINKS</span></span>
