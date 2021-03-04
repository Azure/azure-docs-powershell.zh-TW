---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: a0a3b4c27d3ed2f73efacade6136e8407764b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904109"
---
# <span data-ttu-id="62c77-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c77-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="62c77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="62c77-102">SYNOPSIS</span></span>
<span data-ttu-id="62c77-103">更新組組註冊的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="62c77-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="62c77-104">語法</span><span class="sxs-lookup"><span data-stu-id="62c77-104">SYNTAX</span></span>

### <span data-ttu-id="62c77-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62c77-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c77-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62c77-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62c77-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62c77-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62c77-108">描述</span><span class="sxs-lookup"><span data-stu-id="62c77-108">DESCRIPTION</span></span>
<span data-ttu-id="62c77-109">更新 IoT 自動裝置管理配置的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="62c77-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="62c77-110">注意：可更新組式內容。</span><span class="sxs-lookup"><span data-stu-id="62c77-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="62c77-111">可更新的組組屬性為'labels'、'metrics'、'priority' 和 'targetCondition'。</span><span class="sxs-lookup"><span data-stu-id="62c77-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="62c77-112">請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="62c77-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="62c77-113">例子</span><span class="sxs-lookup"><span data-stu-id="62c77-113">EXAMPLES</span></span>

### <span data-ttu-id="62c77-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="62c77-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="62c77-115">變更裝置配置的優先順序並更新其目標條件</span><span class="sxs-lookup"><span data-stu-id="62c77-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="62c77-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="62c77-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="62c77-117">更新裝置配置的度量和標籤</span><span class="sxs-lookup"><span data-stu-id="62c77-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="62c77-118">參數</span><span class="sxs-lookup"><span data-stu-id="62c77-118">PARAMETERS</span></span>

### <span data-ttu-id="62c77-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c77-119">-DefaultProfile</span></span>
<span data-ttu-id="62c77-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="62c77-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62c77-121">-強制</span><span class="sxs-lookup"><span data-stu-id="62c77-121">-Force</span></span>
<span data-ttu-id="62c77-122">允許取代群組原則物件，即使自上次取回之後已更新。</span><span class="sxs-lookup"><span data-stu-id="62c77-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="62c77-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62c77-123">-InputObject</span></span>
<span data-ttu-id="62c77-124">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="62c77-124">IotHub object</span></span>

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

### <span data-ttu-id="62c77-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62c77-125">-IotHubName</span></span>
<span data-ttu-id="62c77-126">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="62c77-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62c77-127">-標籤</span><span class="sxs-lookup"><span data-stu-id="62c77-127">-Label</span></span>
<span data-ttu-id="62c77-128">要用於目標群組配置的標號地圖。</span><span class="sxs-lookup"><span data-stu-id="62c77-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="62c77-129">-公制</span><span class="sxs-lookup"><span data-stu-id="62c77-129">-Metric</span></span>
<span data-ttu-id="62c77-130">設定檔計量定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="62c77-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="62c77-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="62c77-131">-Name</span></span>
<span data-ttu-id="62c77-132">組配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="62c77-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="62c77-133">-優先順序</span><span class="sxs-lookup"><span data-stu-id="62c77-133">-Priority</span></span>
<span data-ttu-id="62c77-134">在相互比對的規則中，裝置組 (優先) 。</span><span class="sxs-lookup"><span data-stu-id="62c77-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="62c77-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c77-135">-ResourceGroupName</span></span>
<span data-ttu-id="62c77-136">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="62c77-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62c77-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62c77-137">-ResourceId</span></span>
<span data-ttu-id="62c77-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="62c77-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62c77-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="62c77-139">-TargetCondition</span></span>
<span data-ttu-id="62c77-140">裝置組態適用的目標條件。</span><span class="sxs-lookup"><span data-stu-id="62c77-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="62c77-141">-確認</span><span class="sxs-lookup"><span data-stu-id="62c77-141">-Confirm</span></span>
<span data-ttu-id="62c77-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="62c77-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c77-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c77-143">-WhatIf</span></span>
<span data-ttu-id="62c77-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62c77-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c77-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62c77-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c77-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c77-146">CommonParameters</span></span>
<span data-ttu-id="62c77-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="62c77-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c77-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="62c77-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c77-149">輸入</span><span class="sxs-lookup"><span data-stu-id="62c77-149">INPUTS</span></span>

### <span data-ttu-id="62c77-150">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="62c77-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62c77-151">System.String</span><span class="sxs-lookup"><span data-stu-id="62c77-151">System.String</span></span>

## <span data-ttu-id="62c77-152">輸出</span><span class="sxs-lookup"><span data-stu-id="62c77-152">OUTPUTS</span></span>

### <span data-ttu-id="62c77-153">Microsoft.Azure.Commands.management.IotHub.models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c77-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="62c77-154">筆記</span><span class="sxs-lookup"><span data-stu-id="62c77-154">NOTES</span></span>

## <span data-ttu-id="62c77-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="62c77-155">RELATED LINKS</span></span>
