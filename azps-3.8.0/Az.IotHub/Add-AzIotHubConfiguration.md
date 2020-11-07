---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: 6b4068056607de76380e5ec8457f7a8242a1a0b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965693"
---
# <span data-ttu-id="10d1c-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="10d1c-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="10d1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="10d1c-102">SYNOPSIS</span></span>
<span data-ttu-id="10d1c-103">在目標 IoT 中樞中新增 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="10d1c-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="10d1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="10d1c-104">SYNTAX</span></span>

### <span data-ttu-id="10d1c-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10d1c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10d1c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10d1c-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10d1c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10d1c-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10d1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="10d1c-108">DESCRIPTION</span></span>
<span data-ttu-id="10d1c-109">配置內容是 json，而且 slighty 會根據裝置或模組的用途而有所不同。</span><span class="sxs-lookup"><span data-stu-id="10d1c-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="10d1c-110">裝置設定的形式為 {"deviceContent"： {...}}</span><span class="sxs-lookup"><span data-stu-id="10d1c-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="10d1c-111">模組配置的形式為 {"moduleContent"： {...}}</span><span class="sxs-lookup"><span data-stu-id="10d1c-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="10d1c-112">您可以使用使用者提供的 [針對需求評估] 配置來定義設定。</span><span class="sxs-lookup"><span data-stu-id="10d1c-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="10d1c-113">使用者度量值為 json，且形式為 {"查詢"： {...}}</span><span class="sxs-lookup"><span data-stu-id="10d1c-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="10d1c-114">或 {"公制"： {"查詢"： {...}}}。</span><span class="sxs-lookup"><span data-stu-id="10d1c-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="10d1c-115">注意：模組的目標條件必須以 "from devices.] 開頭。</span><span class="sxs-lookup"><span data-stu-id="10d1c-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="10d1c-116">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 。</span><span class="sxs-lookup"><span data-stu-id="10d1c-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="10d1c-117">示例</span><span class="sxs-lookup"><span data-stu-id="10d1c-117">EXAMPLES</span></span>

### <span data-ttu-id="10d1c-118">範例1</span><span class="sxs-lookup"><span data-stu-id="10d1c-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="10d1c-119">建立含預設中繼資料的裝置配置。</span><span class="sxs-lookup"><span data-stu-id="10d1c-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="10d1c-120">範例2</span><span class="sxs-lookup"><span data-stu-id="10d1c-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="10d1c-121">建立一個優先順序為3的裝置設定，當裝置在建築物9中標記且環境為「test」時，就會套用到條件。</span><span class="sxs-lookup"><span data-stu-id="10d1c-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="10d1c-122">範例2</span><span class="sxs-lookup"><span data-stu-id="10d1c-122">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="10d1c-123">建立具有使用者規格的裝置配置。</span><span class="sxs-lookup"><span data-stu-id="10d1c-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="10d1c-124">範例3</span><span class="sxs-lookup"><span data-stu-id="10d1c-124">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="10d1c-125">建立含標籤的裝置設定。</span><span class="sxs-lookup"><span data-stu-id="10d1c-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="10d1c-126">範例4</span><span class="sxs-lookup"><span data-stu-id="10d1c-126">Example 4</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="10d1c-127">建立含有內容的裝置配置。</span><span class="sxs-lookup"><span data-stu-id="10d1c-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="10d1c-128">參數</span><span class="sxs-lookup"><span data-stu-id="10d1c-128">PARAMETERS</span></span>

### <span data-ttu-id="10d1c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d1c-129">-DefaultProfile</span></span>
<span data-ttu-id="10d1c-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="10d1c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d1c-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="10d1c-131">-DeviceContent</span></span>
<span data-ttu-id="10d1c-132">IotHub 裝置的配置。</span><span class="sxs-lookup"><span data-stu-id="10d1c-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="10d1c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10d1c-133">-InputObject</span></span>
<span data-ttu-id="10d1c-134">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="10d1c-134">IotHub object</span></span>

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

### <span data-ttu-id="10d1c-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="10d1c-135">-IotHubName</span></span>
<span data-ttu-id="10d1c-136">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="10d1c-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="10d1c-137">-標籤</span><span class="sxs-lookup"><span data-stu-id="10d1c-137">-Label</span></span>
<span data-ttu-id="10d1c-138">要套用至目標設定的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="10d1c-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="10d1c-139">-公制</span><span class="sxs-lookup"><span data-stu-id="10d1c-139">-Metric</span></span>
<span data-ttu-id="10d1c-140">配置指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="10d1c-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="10d1c-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="10d1c-141">-Name</span></span>
<span data-ttu-id="10d1c-142">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="10d1c-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="10d1c-143">-優先順序</span><span class="sxs-lookup"><span data-stu-id="10d1c-143">-Priority</span></span>
<span data-ttu-id="10d1c-144">在爭用規則時，裝置設定的重量 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="10d1c-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="10d1c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d1c-145">-ResourceGroupName</span></span>
<span data-ttu-id="10d1c-146">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="10d1c-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="10d1c-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10d1c-147">-ResourceId</span></span>
<span data-ttu-id="10d1c-148">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="10d1c-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="10d1c-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="10d1c-149">-TargetCondition</span></span>
<span data-ttu-id="10d1c-150">裝置設定適用的目標條件。</span><span class="sxs-lookup"><span data-stu-id="10d1c-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="10d1c-151">-確認</span><span class="sxs-lookup"><span data-stu-id="10d1c-151">-Confirm</span></span>
<span data-ttu-id="10d1c-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="10d1c-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d1c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d1c-153">-WhatIf</span></span>
<span data-ttu-id="10d1c-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="10d1c-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d1c-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="10d1c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d1c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d1c-156">CommonParameters</span></span>
<span data-ttu-id="10d1c-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="10d1c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d1c-158">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="10d1c-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d1c-159">輸入</span><span class="sxs-lookup"><span data-stu-id="10d1c-159">INPUTS</span></span>

### <span data-ttu-id="10d1c-160">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="10d1c-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="10d1c-161">System.object</span><span class="sxs-lookup"><span data-stu-id="10d1c-161">System.String</span></span>

## <span data-ttu-id="10d1c-162">輸出</span><span class="sxs-lookup"><span data-stu-id="10d1c-162">OUTPUTS</span></span>

### <span data-ttu-id="10d1c-163">PSConfiguration （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="10d1c-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="10d1c-164">筆記</span><span class="sxs-lookup"><span data-stu-id="10d1c-164">NOTES</span></span>

## <span data-ttu-id="10d1c-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="10d1c-165">RELATED LINKS</span></span>
