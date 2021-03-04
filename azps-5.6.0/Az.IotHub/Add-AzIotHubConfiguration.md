---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 2521d73d26b281e2dbc242e860869e4e31c78208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913890"
---
# <span data-ttu-id="b6f5e-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f5e-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="b6f5e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f5e-103">在目標 IoT 中心新增 IoT 自動裝置管理組式。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="b6f5e-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6f5e-104">SYNTAX</span></span>

### <span data-ttu-id="b6f5e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b6f5e-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6f5e-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6f5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6f5e-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6f5e-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="b6f5e-109">組組內容為 json，並且會依據裝置或模組意圖而稍有不同。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="b6f5e-110">裝置組配置的形式為 {"deviceContent"：{...}}</span><span class="sxs-lookup"><span data-stu-id="b6f5e-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="b6f5e-111">模組組式是 {"moduleContent"：{...}}</span><span class="sxs-lookup"><span data-stu-id="b6f5e-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="b6f5e-112">您可使用使用者提供的隨需評估度量來定義群組原則。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="b6f5e-113">使用者計量為 json 且為 {"queries"：{...}}</span><span class="sxs-lookup"><span data-stu-id="b6f5e-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="b6f5e-114">或 {"metrics"：{"queries"：{...}}}。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="b6f5e-115">注意：模組的目標條件必須以「從 devices.modules where」開始。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="b6f5e-116">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="b6f5e-117">例子</span><span class="sxs-lookup"><span data-stu-id="b6f5e-117">EXAMPLES</span></span>

### <span data-ttu-id="b6f5e-118">範例 1</span><span class="sxs-lookup"><span data-stu-id="b6f5e-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="b6f5e-119">使用預設中繼資料建立裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="b6f5e-120">範例 2</span><span class="sxs-lookup"><span data-stu-id="b6f5e-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="b6f5e-121">建立優先順序為 3 的裝置組態，此為在建築物 9 中標記裝置且環境為'測試'的條件。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="b6f5e-122">範例 3</span><span class="sxs-lookup"><span data-stu-id="b6f5e-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="b6f5e-123">使用使用者計量建立裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="b6f5e-124">範例 4</span><span class="sxs-lookup"><span data-stu-id="b6f5e-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="b6f5e-125">使用標籤建立裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="b6f5e-126">範例 5</span><span class="sxs-lookup"><span data-stu-id="b6f5e-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="b6f5e-127">建立包含內容的裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="b6f5e-128">參數</span><span class="sxs-lookup"><span data-stu-id="b6f5e-128">PARAMETERS</span></span>

### <span data-ttu-id="b6f5e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f5e-129">-DefaultProfile</span></span>
<span data-ttu-id="b6f5e-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6f5e-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="b6f5e-131">-DeviceContent</span></span>
<span data-ttu-id="b6f5e-132">IotHub 裝置組配置。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-132">Configuration for IotHub devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6f5e-133">-InputObject</span></span>
<span data-ttu-id="b6f5e-134">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b6f5e-134">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b6f5e-135">-IotHubName</span></span>
<span data-ttu-id="b6f5e-136">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="b6f5e-136">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-137">-標籤</span><span class="sxs-lookup"><span data-stu-id="b6f5e-137">-Label</span></span>
<span data-ttu-id="b6f5e-138">要用於目標群組配置的標號地圖。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-138">Map of labels to be applied to target configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-139">-公制</span><span class="sxs-lookup"><span data-stu-id="b6f5e-139">-Metric</span></span>
<span data-ttu-id="b6f5e-140">設定檔計量定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-140">Queries collection for configuration metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6f5e-141">-Name</span></span>
<span data-ttu-id="b6f5e-142">組配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-142">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-143">-優先順序</span><span class="sxs-lookup"><span data-stu-id="b6f5e-143">-Priority</span></span>
<span data-ttu-id="b6f5e-144">在相互比對的規則中，裝置組 (優先) 。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f5e-145">-ResourceGroupName</span></span>
<span data-ttu-id="b6f5e-146">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b6f5e-146">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6f5e-147">-ResourceId</span></span>
<span data-ttu-id="b6f5e-148">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b6f5e-148">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="b6f5e-149">-TargetCondition</span></span>
<span data-ttu-id="b6f5e-150">裝置組態適用的目標條件。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-150">Target condition in which a device configuration applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f5e-151">-確認</span><span class="sxs-lookup"><span data-stu-id="b6f5e-151">-Confirm</span></span>
<span data-ttu-id="b6f5e-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6f5e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6f5e-153">-WhatIf</span></span>
<span data-ttu-id="b6f5e-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6f5e-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6f5e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f5e-156">CommonParameters</span></span>
<span data-ttu-id="b6f5e-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f5e-158">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b6f5e-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f5e-159">輸入</span><span class="sxs-lookup"><span data-stu-id="b6f5e-159">INPUTS</span></span>

### <span data-ttu-id="b6f5e-160">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b6f5e-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b6f5e-161">System.String</span><span class="sxs-lookup"><span data-stu-id="b6f5e-161">System.String</span></span>

## <span data-ttu-id="b6f5e-162">輸出</span><span class="sxs-lookup"><span data-stu-id="b6f5e-162">OUTPUTS</span></span>

### <span data-ttu-id="b6f5e-163">Microsoft.Azure.Commands.management.IotHub.models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6f5e-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="b6f5e-164">筆記</span><span class="sxs-lookup"><span data-stu-id="b6f5e-164">NOTES</span></span>

## <span data-ttu-id="b6f5e-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6f5e-165">RELATED LINKS</span></span>
