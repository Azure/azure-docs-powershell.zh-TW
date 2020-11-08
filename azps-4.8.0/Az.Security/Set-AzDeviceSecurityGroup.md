---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126836"
---
# <span data-ttu-id="8c8cd-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c8cd-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="8c8cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c8cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8cd-103">建立或更新 device security 群組</span><span class="sxs-lookup"><span data-stu-id="8c8cd-103">Create or update device security group</span></span>

## <span data-ttu-id="8c8cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c8cd-104">SYNTAX</span></span>

### <span data-ttu-id="8c8cd-105">ResourceIdLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8c8cd-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c8cd-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8c8cd-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c8cd-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8cd-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c8cd-108">說明</span><span class="sxs-lookup"><span data-stu-id="8c8cd-108">DESCRIPTION</span></span>
<span data-ttu-id="8c8cd-109">Set-AzDeviceSecurityGroup Cmdlet 會建立或更新在 iot 安全解決方案中定義的裝置安全性群組。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="8c8cd-110">示例</span><span class="sxs-lookup"><span data-stu-id="8c8cd-110">EXAMPLES</span></span>

### <span data-ttu-id="8c8cd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8c8cd-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="8c8cd-112">從 IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 使用規則類型 "ActiveConnectionsNotInAllowedRange" 更新現有的裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="8c8cd-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="8c8cd-113">參數</span><span class="sxs-lookup"><span data-stu-id="8c8cd-113">PARAMETERS</span></span>

### <span data-ttu-id="8c8cd-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="8c8cd-114">-AllowlistRule</span></span>
<span data-ttu-id="8c8cd-115">允許清單規則。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8cd-116">-DefaultProfile</span></span>
<span data-ttu-id="8c8cd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c8cd-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="8c8cd-118">-DenylistRule</span></span>
<span data-ttu-id="8c8cd-119">拒絕清單規則。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8cd-120">-HubResourceId</span></span>
<span data-ttu-id="8c8cd-121">IoT 中心資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c8cd-122">-InputObject</span></span>
<span data-ttu-id="8c8cd-123">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c8cd-124">-Name</span></span>
<span data-ttu-id="8c8cd-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c8cd-126">-ResourceId</span></span>
<span data-ttu-id="8c8cd-127">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="8c8cd-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="8c8cd-128">-ThresholdRule</span></span>
<span data-ttu-id="8c8cd-129">閾值規則。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="8c8cd-130">-TimeWindowRule</span></span>
<span data-ttu-id="8c8cd-131">時間範圍規則。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c8cd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="8c8cd-132">-Confirm</span></span>
<span data-ttu-id="8c8cd-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c8cd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c8cd-134">-WhatIf</span></span>
<span data-ttu-id="8c8cd-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c8cd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c8cd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8cd-137">CommonParameters</span></span>
<span data-ttu-id="8c8cd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8cd-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c8cd-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8cd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="8c8cd-140">INPUTS</span></span>

### <span data-ttu-id="8c8cd-141">PSThresholdCustomAlertRule []. DeviceSecurityGroups. []</span><span class="sxs-lookup"><span data-stu-id="8c8cd-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="8c8cd-142">PSTimeWindowCustomAlertRule []. DeviceSecurityGroups. []</span><span class="sxs-lookup"><span data-stu-id="8c8cd-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="8c8cd-143">PSAllowlistCustomAlertRule []. DeviceSecurityGroups. []</span><span class="sxs-lookup"><span data-stu-id="8c8cd-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="8c8cd-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="8c8cd-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="8c8cd-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c8cd-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="8c8cd-146">System.object</span><span class="sxs-lookup"><span data-stu-id="8c8cd-146">System.String</span></span>

## <span data-ttu-id="8c8cd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="8c8cd-147">OUTPUTS</span></span>

### <span data-ttu-id="8c8cd-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8c8cd-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="8c8cd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="8c8cd-149">NOTES</span></span>

## <span data-ttu-id="8c8cd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c8cd-150">RELATED LINKS</span></span>
