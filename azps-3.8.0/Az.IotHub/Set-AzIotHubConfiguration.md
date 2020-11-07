---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 9b6c9b77ae29214c7d998e3d2c859e4ac7521db1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957356"
---
# <span data-ttu-id="0001e-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="0001e-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="0001e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0001e-102">SYNOPSIS</span></span>
<span data-ttu-id="0001e-103">更新配置註冊的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="0001e-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="0001e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0001e-104">SYNTAX</span></span>

### <span data-ttu-id="0001e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0001e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0001e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0001e-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0001e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0001e-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0001e-108">說明</span><span class="sxs-lookup"><span data-stu-id="0001e-108">DESCRIPTION</span></span>
<span data-ttu-id="0001e-109">更新 IoT 自動裝置管理設定的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="0001e-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="0001e-110">注意：配置內容是不可變的。</span><span class="sxs-lookup"><span data-stu-id="0001e-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="0001e-111">可以更新的設定屬性為「標籤」、「公制」、「priority」和「targetCondition」。</span><span class="sxs-lookup"><span data-stu-id="0001e-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="0001e-112">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 。</span><span class="sxs-lookup"><span data-stu-id="0001e-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="0001e-113">示例</span><span class="sxs-lookup"><span data-stu-id="0001e-113">EXAMPLES</span></span>

### <span data-ttu-id="0001e-114">範例1</span><span class="sxs-lookup"><span data-stu-id="0001e-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="0001e-115">變更裝置配置的優先順序並更新其目標條件</span><span class="sxs-lookup"><span data-stu-id="0001e-115">Alter the priority of a device configuration and update its target condition</span></span>

## <span data-ttu-id="0001e-116">參數</span><span class="sxs-lookup"><span data-stu-id="0001e-116">PARAMETERS</span></span>

### <span data-ttu-id="0001e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0001e-117">-DefaultProfile</span></span>
<span data-ttu-id="0001e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0001e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0001e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0001e-119">-Force</span></span>
<span data-ttu-id="0001e-120">允許即使在上次檢索之後才進行過更新，也能取代 configuration 物件。</span><span class="sxs-lookup"><span data-stu-id="0001e-120">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="0001e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0001e-121">-InputObject</span></span>
<span data-ttu-id="0001e-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="0001e-122">IotHub object</span></span>

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

### <span data-ttu-id="0001e-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0001e-123">-IotHubName</span></span>
<span data-ttu-id="0001e-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="0001e-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0001e-125">-標籤</span><span class="sxs-lookup"><span data-stu-id="0001e-125">-Label</span></span>
<span data-ttu-id="0001e-126">要套用至目標設定的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="0001e-126">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="0001e-127">-公制</span><span class="sxs-lookup"><span data-stu-id="0001e-127">-Metric</span></span>
<span data-ttu-id="0001e-128">配置指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="0001e-128">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="0001e-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0001e-129">-Name</span></span>
<span data-ttu-id="0001e-130">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0001e-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="0001e-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="0001e-131">-Priority</span></span>
<span data-ttu-id="0001e-132">在爭用規則時，裝置設定的重量 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="0001e-132">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="0001e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0001e-133">-ResourceGroupName</span></span>
<span data-ttu-id="0001e-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="0001e-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0001e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0001e-135">-ResourceId</span></span>
<span data-ttu-id="0001e-136">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="0001e-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0001e-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="0001e-137">-TargetCondition</span></span>
<span data-ttu-id="0001e-138">裝置設定適用的目標條件。</span><span class="sxs-lookup"><span data-stu-id="0001e-138">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="0001e-139">-確認</span><span class="sxs-lookup"><span data-stu-id="0001e-139">-Confirm</span></span>
<span data-ttu-id="0001e-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0001e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0001e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0001e-141">-WhatIf</span></span>
<span data-ttu-id="0001e-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0001e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0001e-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0001e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0001e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0001e-144">CommonParameters</span></span>
<span data-ttu-id="0001e-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0001e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0001e-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0001e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0001e-147">輸入</span><span class="sxs-lookup"><span data-stu-id="0001e-147">INPUTS</span></span>

### <span data-ttu-id="0001e-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0001e-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0001e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="0001e-149">System.String</span></span>

## <span data-ttu-id="0001e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="0001e-150">OUTPUTS</span></span>

### <span data-ttu-id="0001e-151">PSConfiguration （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="0001e-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="0001e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="0001e-152">NOTES</span></span>

## <span data-ttu-id="0001e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="0001e-153">RELATED LINKS</span></span>
