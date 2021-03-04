---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzIotSecuritySolution.md
ms.openlocfilehash: 965aaeaba9d77b28389c4493e4a891b9e01aa2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916709"
---
# <span data-ttu-id="1f9a0-101">Set-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1f9a0-101">Set-AzIotSecuritySolution</span></span>

## <span data-ttu-id="1f9a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1f9a0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f9a0-103">建立或更新 IoT 安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="1f9a0-103">Create or update IoT security solution</span></span>

## <span data-ttu-id="1f9a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="1f9a0-104">SYNTAX</span></span>

### <span data-ttu-id="1f9a0-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="1f9a0-105">ResourceGroupLevelResource (Default)</span></span>
```
Set-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9a0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="1f9a0-106">InputObject</span></span>
```
Set-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-Tag <Hashtable>] -Location <String>
 -Workspace <String> -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>]
 [-DisabledDataSource <String[]>] -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f9a0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a0-107">ResourceId</span></span>
```
Set-AzIotSecuritySolution -ResourceId <String> [-Tag <Hashtable>] -Location <String> -Workspace <String>
 -DisplayName <String> [-Enabled <Boolean>] [-Export <String[]>] [-DisabledDataSource <String[]>]
 -IotHub <String[]> [-UserDefinedResource <PSUserDefinedResources>]
 [-RecommendationsConfiguration <PSRecommendationConfiguration[]>] [-UnmaskedIpLoggingStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f9a0-108">描述</span><span class="sxs-lookup"><span data-stu-id="1f9a0-108">DESCRIPTION</span></span>
<span data-ttu-id="1f9a0-109">Cmdlet Set-AzIotSecuritySolution或更新特定的 iot 安全性解決方案。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-109">The Set-AzIotSecuritySolution cmdlet creates or updates a specific iot security solution.</span></span> <span data-ttu-id="1f9a0-110">IoT 安全性解決方案會收集 iot 裝置和 iot 中樞的安全性資料和事件，協助防範和偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>
<span data-ttu-id="1f9a0-111">iot 安全性解決方案的名稱應該與 iot 中心的名稱相同。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-111">The name of iot security solution should be identical to the name of the iot hub.</span></span>

## <span data-ttu-id="1f9a0-112">例子</span><span class="sxs-lookup"><span data-stu-id="1f9a0-112">EXAMPLES</span></span>

### <span data-ttu-id="1f9a0-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="1f9a0-113">Example 1</span></span>
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

<span data-ttu-id="1f9a0-114">使用資源識別碼 "/subscriptions/XXXXXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" 為 IoT 中樞建立新的 iot 安全性解決方案 "MySample" (解決方案的名稱應該與 IoT 中心的名稱相同) </span><span class="sxs-lookup"><span data-stu-id="1f9a0-114">Create new iot security solution "MySample" for IoT hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MichalResourceGroup/providers/Microsoft.Devices/IotHubs/MySample" (the name of the solution should be identical to the name of the IoT hub)</span></span>

## <span data-ttu-id="1f9a0-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f9a0-115">PARAMETERS</span></span>

### <span data-ttu-id="1f9a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f9a0-116">-DefaultProfile</span></span>
<span data-ttu-id="1f9a0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f9a0-118">-DisabledDataSource</span><span class="sxs-lookup"><span data-stu-id="1f9a0-118">-DisabledDataSource</span></span>
<span data-ttu-id="1f9a0-119">已停用資料來源。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-119">Disabled data sources.</span></span>

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

### <span data-ttu-id="1f9a0-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1f9a0-120">-DisplayName</span></span>
<span data-ttu-id="1f9a0-121">顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-121">Display name.</span></span>

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

### <span data-ttu-id="1f9a0-122">-已啟用</span><span class="sxs-lookup"><span data-stu-id="1f9a0-122">-Enabled</span></span>
<span data-ttu-id="1f9a0-123">地位。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-123">Status .</span></span>

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

### <span data-ttu-id="1f9a0-124">-匯出</span><span class="sxs-lookup"><span data-stu-id="1f9a0-124">-Export</span></span>
<span data-ttu-id="1f9a0-125">匯出資料。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-125">Export data.</span></span>

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

### <span data-ttu-id="1f9a0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f9a0-126">-InputObject</span></span>
<span data-ttu-id="1f9a0-127">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-127">Input Object.</span></span>

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

### <span data-ttu-id="1f9a0-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="1f9a0-128">-IotHub</span></span>
<span data-ttu-id="1f9a0-129">Iot hubs.</span><span class="sxs-lookup"><span data-stu-id="1f9a0-129">Iot hubs.</span></span>

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

### <span data-ttu-id="1f9a0-130">-位置</span><span class="sxs-lookup"><span data-stu-id="1f9a0-130">-Location</span></span>
<span data-ttu-id="1f9a0-131">位置。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-131">Location.</span></span>

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

### <span data-ttu-id="1f9a0-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f9a0-132">-Name</span></span>
<span data-ttu-id="1f9a0-133">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-133">Resource name.</span></span>

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

### <span data-ttu-id="1f9a0-134">-RecommendationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f9a0-134">-RecommendationsConfiguration</span></span>
<span data-ttu-id="1f9a0-135">建議組配置。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-135">Recommendations configuration.</span></span>

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

### <span data-ttu-id="1f9a0-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f9a0-136">-ResourceGroupName</span></span>
<span data-ttu-id="1f9a0-137">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-137">Resource group name.</span></span>

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

### <span data-ttu-id="1f9a0-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f9a0-138">-ResourceId</span></span>
<span data-ttu-id="1f9a0-139">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-139">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="1f9a0-140">-標記</span><span class="sxs-lookup"><span data-stu-id="1f9a0-140">-Tag</span></span>
<span data-ttu-id="1f9a0-141">標籤。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-141">Tags.</span></span>

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

### <span data-ttu-id="1f9a0-142">-UnmaskedIpLoggingStatus</span><span class="sxs-lookup"><span data-stu-id="1f9a0-142">-UnmaskedIpLoggingStatus</span></span>
<span data-ttu-id="1f9a0-143">未遮罩的 IP 記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-143">Unmasked ip logging status.</span></span>

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

### <span data-ttu-id="1f9a0-144">-UserDefinedResource</span><span class="sxs-lookup"><span data-stu-id="1f9a0-144">-UserDefinedResource</span></span>
<span data-ttu-id="1f9a0-145">使用者定義的資源。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-145">User defined resources.</span></span>

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

### <span data-ttu-id="1f9a0-146">-工作區</span><span class="sxs-lookup"><span data-stu-id="1f9a0-146">-Workspace</span></span>
<span data-ttu-id="1f9a0-147">工作區識別碼。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-147">Workspace ID.</span></span>

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

### <span data-ttu-id="1f9a0-148">-確認</span><span class="sxs-lookup"><span data-stu-id="1f9a0-148">-Confirm</span></span>
<span data-ttu-id="1f9a0-149">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f9a0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f9a0-150">-WhatIf</span></span>
<span data-ttu-id="1f9a0-151">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f9a0-152">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f9a0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f9a0-153">CommonParameters</span></span>
<span data-ttu-id="1f9a0-154">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1f9a0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f9a0-155">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f9a0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f9a0-156">輸入</span><span class="sxs-lookup"><span data-stu-id="1f9a0-156">INPUTS</span></span>

### <span data-ttu-id="1f9a0-157">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1f9a0-157">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

### <span data-ttu-id="1f9a0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="1f9a0-158">System.String</span></span>

### <span data-ttu-id="1f9a0-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f9a0-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1f9a0-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="1f9a0-160">System.String[]</span></span>

### <span data-ttu-id="1f9a0-161">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="1f9a0-161">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

### <span data-ttu-id="1f9a0-162">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSRecommendationConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="1f9a0-162">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration[]</span></span>

## <span data-ttu-id="1f9a0-163">輸出</span><span class="sxs-lookup"><span data-stu-id="1f9a0-163">OUTPUTS</span></span>

### <span data-ttu-id="1f9a0-164">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="1f9a0-164">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="1f9a0-165">筆記</span><span class="sxs-lookup"><span data-stu-id="1f9a0-165">NOTES</span></span>

## <span data-ttu-id="1f9a0-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f9a0-166">RELATED LINKS</span></span>
