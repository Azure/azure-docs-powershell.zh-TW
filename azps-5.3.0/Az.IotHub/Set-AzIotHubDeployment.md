---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98289032"
---
# <span data-ttu-id="62881-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="62881-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="62881-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62881-102">SYNOPSIS</span></span>
<span data-ttu-id="62881-103">更新 IoT Edge 部署的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="62881-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="62881-104">句法</span><span class="sxs-lookup"><span data-stu-id="62881-104">SYNTAX</span></span>

### <span data-ttu-id="62881-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="62881-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62881-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62881-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62881-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="62881-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62881-108">說明</span><span class="sxs-lookup"><span data-stu-id="62881-108">DESCRIPTION</span></span>
<span data-ttu-id="62881-109">更新 IoT Edge 部署的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="62881-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="62881-110">注意：配置內容是不可變的。</span><span class="sxs-lookup"><span data-stu-id="62881-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="62881-111">可以更新的設定屬性為「標籤」、「公制」、「priority」和「targetCondition」。</span><span class="sxs-lookup"><span data-stu-id="62881-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="62881-112">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  。</span><span class="sxs-lookup"><span data-stu-id="62881-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="62881-113">示例</span><span class="sxs-lookup"><span data-stu-id="62881-113">EXAMPLES</span></span>

### <span data-ttu-id="62881-114">範例1</span><span class="sxs-lookup"><span data-stu-id="62881-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="62881-115">變更 IoT Edge 部署的優先順序並更新其目標條件。</span><span class="sxs-lookup"><span data-stu-id="62881-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="62881-116">範例2</span><span class="sxs-lookup"><span data-stu-id="62881-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="62881-117">更新 IoT Edge 部署的規格與標籤。</span><span class="sxs-lookup"><span data-stu-id="62881-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="62881-118">參數</span><span class="sxs-lookup"><span data-stu-id="62881-118">PARAMETERS</span></span>

### <span data-ttu-id="62881-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62881-119">-DefaultProfile</span></span>
<span data-ttu-id="62881-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62881-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62881-121">-Force</span><span class="sxs-lookup"><span data-stu-id="62881-121">-Force</span></span>
<span data-ttu-id="62881-122">允許取代部署物件，即使在上次檢索之後，仍會進行更新。</span><span class="sxs-lookup"><span data-stu-id="62881-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="62881-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62881-123">-InputObject</span></span>
<span data-ttu-id="62881-124">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="62881-124">IotHub object</span></span>

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

### <span data-ttu-id="62881-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="62881-125">-IotHubName</span></span>
<span data-ttu-id="62881-126">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="62881-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="62881-127">-標籤</span><span class="sxs-lookup"><span data-stu-id="62881-127">-Label</span></span>
<span data-ttu-id="62881-128">要套用至目標部署的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="62881-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="62881-129">-公制</span><span class="sxs-lookup"><span data-stu-id="62881-129">-Metric</span></span>
<span data-ttu-id="62881-130">IoT Edge 部署指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="62881-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="62881-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="62881-131">-Name</span></span>
<span data-ttu-id="62881-132">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="62881-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="62881-133">-優先順序</span><span class="sxs-lookup"><span data-stu-id="62881-133">-Priority</span></span>
<span data-ttu-id="62881-134">在爭用規則情況下，部署的體重 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="62881-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="62881-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62881-135">-ResourceGroupName</span></span>
<span data-ttu-id="62881-136">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="62881-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="62881-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62881-137">-ResourceId</span></span>
<span data-ttu-id="62881-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="62881-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="62881-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="62881-139">-TargetCondition</span></span>
<span data-ttu-id="62881-140">將邊緣部署套用至其中的目標條件。</span><span class="sxs-lookup"><span data-stu-id="62881-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="62881-141">-確認</span><span class="sxs-lookup"><span data-stu-id="62881-141">-Confirm</span></span>
<span data-ttu-id="62881-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62881-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62881-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62881-143">-WhatIf</span></span>
<span data-ttu-id="62881-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62881-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62881-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62881-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62881-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62881-146">CommonParameters</span></span>
<span data-ttu-id="62881-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62881-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62881-148">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62881-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62881-149">輸入</span><span class="sxs-lookup"><span data-stu-id="62881-149">INPUTS</span></span>

### <span data-ttu-id="62881-150">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="62881-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="62881-151">System.object</span><span class="sxs-lookup"><span data-stu-id="62881-151">System.String</span></span>

## <span data-ttu-id="62881-152">輸出</span><span class="sxs-lookup"><span data-stu-id="62881-152">OUTPUTS</span></span>

### <span data-ttu-id="62881-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="62881-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="62881-154">筆記</span><span class="sxs-lookup"><span data-stu-id="62881-154">NOTES</span></span>

## <span data-ttu-id="62881-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="62881-155">RELATED LINKS</span></span>
