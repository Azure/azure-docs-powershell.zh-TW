---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 19f610cb4b17e32e88ddb85b01d6de82926b7eba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912618"
---
# <span data-ttu-id="634a9-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="634a9-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="634a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="634a9-102">SYNOPSIS</span></span>
<span data-ttu-id="634a9-103">建立或更新裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="634a9-103">Create or update device security group</span></span>

## <span data-ttu-id="634a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="634a9-104">SYNTAX</span></span>

### <span data-ttu-id="634a9-105">ResourceIdLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="634a9-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="634a9-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="634a9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="634a9-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="634a9-108">描述</span><span class="sxs-lookup"><span data-stu-id="634a9-108">DESCRIPTION</span></span>
<span data-ttu-id="634a9-109">Cmdlet Set-AzDeviceSecurityGroup或更新 iot 安全性解決方案中定義的裝置安全性群組。</span><span class="sxs-lookup"><span data-stu-id="634a9-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="634a9-110">例子</span><span class="sxs-lookup"><span data-stu-id="634a9-110">EXAMPLES</span></span>

### <span data-ttu-id="634a9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="634a9-111">Example 1</span></span>
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

<span data-ttu-id="634a9-112">使用規則類型 「ActiveConnectionsNotInAllowedRange」更新 IoT Hub "/subscriptions/XXXXXXXX-XXXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 的現有裝置安全性群組</span><span class="sxs-lookup"><span data-stu-id="634a9-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="634a9-113">參數</span><span class="sxs-lookup"><span data-stu-id="634a9-113">PARAMETERS</span></span>

### <span data-ttu-id="634a9-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="634a9-114">-AllowlistRule</span></span>
<span data-ttu-id="634a9-115">允許清單規則。</span><span class="sxs-lookup"><span data-stu-id="634a9-115">Allow list rules.</span></span>

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

### <span data-ttu-id="634a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="634a9-116">-DefaultProfile</span></span>
<span data-ttu-id="634a9-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="634a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="634a9-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="634a9-118">-DenylistRule</span></span>
<span data-ttu-id="634a9-119">拒絕清單規則。</span><span class="sxs-lookup"><span data-stu-id="634a9-119">Deny list rules.</span></span>

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

### <span data-ttu-id="634a9-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="634a9-120">-HubResourceId</span></span>
<span data-ttu-id="634a9-121">IoT Hub 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="634a9-121">IoT Hub resource Id.</span></span>

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

### <span data-ttu-id="634a9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="634a9-122">-InputObject</span></span>
<span data-ttu-id="634a9-123">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="634a9-123">Input Object.</span></span>

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

### <span data-ttu-id="634a9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="634a9-124">-Name</span></span>
<span data-ttu-id="634a9-125">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="634a9-125">Resource name.</span></span>

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

### <span data-ttu-id="634a9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="634a9-126">-ResourceId</span></span>
<span data-ttu-id="634a9-127">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="634a9-127">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="634a9-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="634a9-128">-ThresholdRule</span></span>
<span data-ttu-id="634a9-129">閾值規則。</span><span class="sxs-lookup"><span data-stu-id="634a9-129">Threshold rules.</span></span>

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

### <span data-ttu-id="634a9-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="634a9-130">-TimeWindowRule</span></span>
<span data-ttu-id="634a9-131">時間視窗規則。</span><span class="sxs-lookup"><span data-stu-id="634a9-131">Time window rules.</span></span>

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

### <span data-ttu-id="634a9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="634a9-132">-Confirm</span></span>
<span data-ttu-id="634a9-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="634a9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="634a9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="634a9-134">-WhatIf</span></span>
<span data-ttu-id="634a9-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="634a9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="634a9-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="634a9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="634a9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="634a9-137">CommonParameters</span></span>
<span data-ttu-id="634a9-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="634a9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="634a9-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="634a9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="634a9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="634a9-140">INPUTS</span></span>

### <span data-ttu-id="634a9-141">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="634a9-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="634a9-142">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="634a9-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="634a9-143">Microsoft.Azure.Commands.security.models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="634a9-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="634a9-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span><span class="sxs-lookup"><span data-stu-id="634a9-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="634a9-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="634a9-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="634a9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="634a9-146">System.String</span></span>

## <span data-ttu-id="634a9-147">輸出</span><span class="sxs-lookup"><span data-stu-id="634a9-147">OUTPUTS</span></span>

### <span data-ttu-id="634a9-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="634a9-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="634a9-149">筆記</span><span class="sxs-lookup"><span data-stu-id="634a9-149">NOTES</span></span>

## <span data-ttu-id="634a9-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="634a9-150">RELATED LINKS</span></span>
