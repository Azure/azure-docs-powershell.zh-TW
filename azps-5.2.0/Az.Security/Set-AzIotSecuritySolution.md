---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 30b6979be7f3aae23bec5d1ca45d48d4dd2290f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277064"
---
# <span data-ttu-id="98ac9-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="98ac9-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="98ac9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="98ac9-103">建立或更新 IoT 安全解決方案</span><span class="sxs-lookup"><span data-stu-id="98ac9-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="98ac9-104">句法</span><span class="sxs-lookup"><span data-stu-id="98ac9-104">SYNTAX</span></span>

### <span data-ttu-id="98ac9-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="98ac9-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ac9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98ac9-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ac9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ac9-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ac9-108">說明</span><span class="sxs-lookup"><span data-stu-id="98ac9-108">DESCRIPTION</span></span>
<span data-ttu-id="98ac9-109">Set-AzIotSecuritySolution Cmdlet 會建立或更新特定的 iot 安全方案。</span><span class="sxs-lookup"><span data-stu-id="98ac9-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="98ac9-110">IoT 安全解決方案會從 IoT 裝置和 IoT 中樞收集安全性資料和事件，以協助防範及偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="98ac9-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="98ac9-111">Iot 安全解決方案的名稱應該與 iot 中樞的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="98ac9-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="98ac9-112">示例</span><span class="sxs-lookup"><span data-stu-id="98ac9-112">EXAMPLES</span></span>

### <span data-ttu-id="98ac9-113">範例1</span><span class="sxs-lookup"><span data-stu-id="98ac9-113">Example 1</span></span>
```powershell
PS C:\> $Workspace = "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.OperationalInsights/workspaces/IoTHubWorkspace"
PS C:\> $IotHubs = @("/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample")
PS C:\> Set-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup" -Location "West US" 
-Workspace $Workspace -DisplayName "MySample" -Enabled $true -IotHub $IotHubs

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
    Query: "" 
    QuerySubscriptions: []
}
RecommendationsConfiguration: [
{
    RecommendationType: "IoT_ACRAuthentication"
    Name: "Service prinicpal not used with ACR repository"
    Status: "Enabled"
}
{
    RecommendationType: "IoT_AgentSendsUnutilizedMessages"
    Name: "Agent sending underutilized messages"
    Status: "Enabled"
    }]
AutoDiscoveredResources: ["/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/MyResourceGroup/providers/microsoft.devices/iothubs/MySample"]
UnmaskedIpLoggingStatus: "Enabled"
Tags: {}
```

<span data-ttu-id="98ac9-114">建立新的 iot 安全解決方案 "MySample" （含資源 id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" 的 IoT 中樞） (方案的名稱應該與 IoT 中樞的名稱相同) </span><span class="sxs-lookup"><span data-stu-id="98ac9-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="98ac9-115">參數</span><span class="sxs-lookup"><span data-stu-id="98ac9-115">PARAMETERS</span></span>

### <span data-ttu-id="98ac9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ac9-116">-DefaultProfile</span></span>
<span data-ttu-id="98ac9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98ac9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ac9-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="98ac9-118">-DisabledDataSource</span></span>
<span data-ttu-id="98ac9-119">已停用的資料來源。</span><span class="sxs-lookup"><span data-stu-id="98ac9-119">Disabled data sources.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="98ac9-120">-DisplayName</span></span>
<span data-ttu-id="98ac9-121">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="98ac9-121">Display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-122">-啟用</span><span class="sxs-lookup"><span data-stu-id="98ac9-122">-Enabled</span></span>
<span data-ttu-id="98ac9-123">狀態值.</span><span class="sxs-lookup"><span data-stu-id="98ac9-123">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-124">-匯出</span><span class="sxs-lookup"><span data-stu-id="98ac9-124">-Export</span></span>
<span data-ttu-id="98ac9-125">匯出資料。</span><span class="sxs-lookup"><span data-stu-id="98ac9-125">Export data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98ac9-126">-InputObject</span></span>
<span data-ttu-id="98ac9-127">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="98ac9-127">Input Object.</span></span>

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

### <span data-ttu-id="98ac9-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="98ac9-128">-IotHub</span></span>
<span data-ttu-id="98ac9-129">Iot 中樞。</span><span class="sxs-lookup"><span data-stu-id="98ac9-129">Iot hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-130">-位置</span><span class="sxs-lookup"><span data-stu-id="98ac9-130">-Location</span></span>
<span data-ttu-id="98ac9-131">位於.</span><span class="sxs-lookup"><span data-stu-id="98ac9-131">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="98ac9-132">-Name</span></span>
<span data-ttu-id="98ac9-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="98ac9-133">Resource name.</span></span>

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

### <span data-ttu-id="98ac9-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="98ac9-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="98ac9-135">建議配置。</span><span class="sxs-lookup"><span data-stu-id="98ac9-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="98ac9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ac9-136">-ResourceGroupName</span></span>
<span data-ttu-id="98ac9-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="98ac9-137">Resource group name.</span></span>

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

### <span data-ttu-id="98ac9-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ac9-138">-ResourceId</span></span>
<span data-ttu-id="98ac9-139">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="98ac9-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="98ac9-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="98ac9-140">-Tag</span></span>
<span data-ttu-id="98ac9-141">間.</span><span class="sxs-lookup"><span data-stu-id="98ac9-141">Tags.</span></span>

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

### <span data-ttu-id="98ac9-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="98ac9-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="98ac9-143">未遮罩的 ip 記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="98ac9-143">Unmasked ip logging status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="98ac9-144">-UserDefinedResource</span></span>
<span data-ttu-id="98ac9-145">使用者定義的資源。</span><span class="sxs-lookup"><span data-stu-id="98ac9-145">User defined resources.</span></span>

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

### <span data-ttu-id="98ac9-146">-工作區</span><span class="sxs-lookup"><span data-stu-id="98ac9-146">-Workspace</span></span>
<span data-ttu-id="98ac9-147">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="98ac9-147">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98ac9-148">-確認</span><span class="sxs-lookup"><span data-stu-id="98ac9-148">-Confirm</span></span>
<span data-ttu-id="98ac9-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98ac9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ac9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ac9-150">-WhatIf</span></span>
<span data-ttu-id="98ac9-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98ac9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ac9-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98ac9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ac9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ac9-153">CommonParameters</span></span>
<span data-ttu-id="98ac9-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98ac9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ac9-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98ac9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ac9-156">輸入</span><span class="sxs-lookup"><span data-stu-id="98ac9-156">INPUTS</span></span>

### <span data-ttu-id="98ac9-157">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="98ac9-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="98ac9-158">System.object</span><span class="sxs-lookup"><span data-stu-id="98ac9-158">System.String</span></span>

### <span data-ttu-id="98ac9-159">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="98ac9-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="98ac9-160">System.object []</span><span class="sxs-lookup"><span data-stu-id="98ac9-160">System.String[]</span></span>

### <span data-ttu-id="98ac9-161">PSUserDefinedResources 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="98ac9-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="98ac9-162">PSRecommendationConfiguration []. IotSecuritySolutions. []</span><span class="sxs-lookup"><span data-stu-id="98ac9-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="98ac9-163">輸出</span><span class="sxs-lookup"><span data-stu-id="98ac9-163">OUTPUTS</span></span>

### <span data-ttu-id="98ac9-164">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="98ac9-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="98ac9-165">筆記</span><span class="sxs-lookup"><span data-stu-id="98ac9-165">NOTES</span></span>

## <span data-ttu-id="98ac9-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="98ac9-166">RELATED LINKS</span></span>
