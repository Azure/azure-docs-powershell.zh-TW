---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 5a0c56a946e9f81163a94a092e646acbc99fb6cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902958"
---
# <span data-ttu-id="c06cd-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c06cd-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="c06cd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c06cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c06cd-103">更新 IoT Edge 部署的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="c06cd-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="c06cd-104">語法</span><span class="sxs-lookup"><span data-stu-id="c06cd-104">SYNTAX</span></span>

### <span data-ttu-id="c06cd-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c06cd-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06cd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c06cd-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c06cd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c06cd-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c06cd-108">描述</span><span class="sxs-lookup"><span data-stu-id="c06cd-108">DESCRIPTION</span></span>
<span data-ttu-id="c06cd-109">更新 IoT Edge 部署的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="c06cd-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="c06cd-110">注意：可更新組式內容。</span><span class="sxs-lookup"><span data-stu-id="c06cd-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="c06cd-111">可更新的組組屬性為'labels'、'metrics'、'priority' 和 'targetCondition'。</span><span class="sxs-lookup"><span data-stu-id="c06cd-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="c06cd-112">請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="c06cd-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="c06cd-113">例子</span><span class="sxs-lookup"><span data-stu-id="c06cd-113">EXAMPLES</span></span>

### <span data-ttu-id="c06cd-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="c06cd-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="c06cd-115">變更 IoT Edge 部署的優先順序並更新其目標條件。</span><span class="sxs-lookup"><span data-stu-id="c06cd-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="c06cd-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="c06cd-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="c06cd-117">更新 IoT Edge 部署的度量和標籤。</span><span class="sxs-lookup"><span data-stu-id="c06cd-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="c06cd-118">參數</span><span class="sxs-lookup"><span data-stu-id="c06cd-118">PARAMETERS</span></span>

### <span data-ttu-id="c06cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c06cd-119">-DefaultProfile</span></span>
<span data-ttu-id="c06cd-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c06cd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c06cd-121">-強制</span><span class="sxs-lookup"><span data-stu-id="c06cd-121">-Force</span></span>
<span data-ttu-id="c06cd-122">允許取代部署物件，即使該物件自上次取回之後已經更新。</span><span class="sxs-lookup"><span data-stu-id="c06cd-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="c06cd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c06cd-123">-InputObject</span></span>
<span data-ttu-id="c06cd-124">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c06cd-124">IotHub object</span></span>

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

### <span data-ttu-id="c06cd-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c06cd-125">-IotHubName</span></span>
<span data-ttu-id="c06cd-126">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c06cd-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c06cd-127">-標籤</span><span class="sxs-lookup"><span data-stu-id="c06cd-127">-Label</span></span>
<span data-ttu-id="c06cd-128">要用於目標部署的標號地圖。</span><span class="sxs-lookup"><span data-stu-id="c06cd-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="c06cd-129">-公制</span><span class="sxs-lookup"><span data-stu-id="c06cd-129">-Metric</span></span>
<span data-ttu-id="c06cd-130">IoT Edge 部署計量定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="c06cd-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="c06cd-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="c06cd-131">-Name</span></span>
<span data-ttu-id="c06cd-132">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c06cd-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="c06cd-133">-優先順序</span><span class="sxs-lookup"><span data-stu-id="c06cd-133">-Priority</span></span>
<span data-ttu-id="c06cd-134">在有相互衝突規則的情況下，部署 (優先) 。</span><span class="sxs-lookup"><span data-stu-id="c06cd-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="c06cd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c06cd-135">-ResourceGroupName</span></span>
<span data-ttu-id="c06cd-136">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="c06cd-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c06cd-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c06cd-137">-ResourceId</span></span>
<span data-ttu-id="c06cd-138">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c06cd-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c06cd-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="c06cd-139">-TargetCondition</span></span>
<span data-ttu-id="c06cd-140">適用于 Edge 部署的目標條件。</span><span class="sxs-lookup"><span data-stu-id="c06cd-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="c06cd-141">-確認</span><span class="sxs-lookup"><span data-stu-id="c06cd-141">-Confirm</span></span>
<span data-ttu-id="c06cd-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c06cd-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c06cd-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c06cd-143">-WhatIf</span></span>
<span data-ttu-id="c06cd-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c06cd-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c06cd-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c06cd-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c06cd-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c06cd-146">CommonParameters</span></span>
<span data-ttu-id="c06cd-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c06cd-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c06cd-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c06cd-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c06cd-149">輸入</span><span class="sxs-lookup"><span data-stu-id="c06cd-149">INPUTS</span></span>

### <span data-ttu-id="c06cd-150">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c06cd-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c06cd-151">System.String</span><span class="sxs-lookup"><span data-stu-id="c06cd-151">System.String</span></span>

## <span data-ttu-id="c06cd-152">輸出</span><span class="sxs-lookup"><span data-stu-id="c06cd-152">OUTPUTS</span></span>

### <span data-ttu-id="c06cd-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c06cd-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="c06cd-154">筆記</span><span class="sxs-lookup"><span data-stu-id="c06cd-154">NOTES</span></span>

## <span data-ttu-id="c06cd-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="c06cd-155">RELATED LINKS</span></span>
