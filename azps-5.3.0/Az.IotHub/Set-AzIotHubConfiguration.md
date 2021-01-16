---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289035"
---
# <span data-ttu-id="7c867-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="7c867-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="7c867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c867-102">SYNOPSIS</span></span>
<span data-ttu-id="7c867-103">更新配置註冊的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="7c867-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="7c867-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c867-104">SYNTAX</span></span>

### <span data-ttu-id="7c867-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7c867-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c867-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c867-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c867-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c867-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c867-108">說明</span><span class="sxs-lookup"><span data-stu-id="7c867-108">DESCRIPTION</span></span>
<span data-ttu-id="7c867-109">更新 IoT 自動裝置管理設定的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="7c867-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="7c867-110">注意：配置內容是不可變的。</span><span class="sxs-lookup"><span data-stu-id="7c867-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="7c867-111">可以更新的設定屬性為「標籤」、「公制」、「priority」和「targetCondition」。</span><span class="sxs-lookup"><span data-stu-id="7c867-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="7c867-112">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 。</span><span class="sxs-lookup"><span data-stu-id="7c867-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="7c867-113">示例</span><span class="sxs-lookup"><span data-stu-id="7c867-113">EXAMPLES</span></span>

### <span data-ttu-id="7c867-114">範例1</span><span class="sxs-lookup"><span data-stu-id="7c867-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="7c867-115">變更裝置配置的優先順序並更新其目標條件</span><span class="sxs-lookup"><span data-stu-id="7c867-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="7c867-116">範例2</span><span class="sxs-lookup"><span data-stu-id="7c867-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="7c867-117">更新裝置設定的規格與標籤</span><span class="sxs-lookup"><span data-stu-id="7c867-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="7c867-118">參數</span><span class="sxs-lookup"><span data-stu-id="7c867-118">PARAMETERS</span></span>

### <span data-ttu-id="7c867-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c867-119">-DefaultProfile</span></span>
<span data-ttu-id="7c867-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c867-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c867-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7c867-121">-Force</span></span>
<span data-ttu-id="7c867-122">允許即使在上次檢索之後才進行過更新，也能取代 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="7c867-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c867-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c867-123">-InputObject</span></span>
<span data-ttu-id="7c867-124">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="7c867-124">IotHub object</span></span>

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

### <span data-ttu-id="7c867-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7c867-125">-IotHubName</span></span>
<span data-ttu-id="7c867-126">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="7c867-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7c867-127">-標籤</span><span class="sxs-lookup"><span data-stu-id="7c867-127">-Label</span></span>
<span data-ttu-id="7c867-128">要套用至目標設定的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="7c867-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="7c867-129">-公制</span><span class="sxs-lookup"><span data-stu-id="7c867-129">-Metric</span></span>
<span data-ttu-id="7c867-130">配置指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="7c867-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="7c867-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="7c867-131">-Name</span></span>
<span data-ttu-id="7c867-132">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7c867-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c867-133">-優先順序</span><span class="sxs-lookup"><span data-stu-id="7c867-133">-Priority</span></span>
<span data-ttu-id="7c867-134">在爭用規則時，裝置設定的重量 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="7c867-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="7c867-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c867-135">-ResourceGroupName</span></span>
<span data-ttu-id="7c867-136">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7c867-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c867-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c867-137">-ResourceId</span></span>
<span data-ttu-id="7c867-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7c867-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7c867-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7c867-139">-TargetCondition</span></span>
<span data-ttu-id="7c867-140">裝置設定適用的目標條件。</span><span class="sxs-lookup"><span data-stu-id="7c867-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="7c867-141">-確認</span><span class="sxs-lookup"><span data-stu-id="7c867-141">-Confirm</span></span>
<span data-ttu-id="7c867-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c867-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c867-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c867-143">-WhatIf</span></span>
<span data-ttu-id="7c867-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c867-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c867-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c867-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c867-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c867-146">CommonParameters</span></span>
<span data-ttu-id="7c867-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c867-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c867-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c867-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c867-149">輸入</span><span class="sxs-lookup"><span data-stu-id="7c867-149">INPUTS</span></span>

### <span data-ttu-id="7c867-150">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="7c867-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c867-151">System.object</span><span class="sxs-lookup"><span data-stu-id="7c867-151">System.String</span></span>

## <span data-ttu-id="7c867-152">輸出</span><span class="sxs-lookup"><span data-stu-id="7c867-152">OUTPUTS</span></span>

### <span data-ttu-id="7c867-153">PSConfiguration （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="7c867-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="7c867-154">筆記</span><span class="sxs-lookup"><span data-stu-id="7c867-154">NOTES</span></span>

## <span data-ttu-id="7c867-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c867-155">RELATED LINKS</span></span>
