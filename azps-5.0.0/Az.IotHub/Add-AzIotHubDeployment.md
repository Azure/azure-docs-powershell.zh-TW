---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139236"
---
# <span data-ttu-id="b8651-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="b8651-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="b8651-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b8651-102">SYNOPSIS</span></span>
<span data-ttu-id="b8651-103">在目標 IoT 中樞中新增 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="b8651-104">句法</span><span class="sxs-lookup"><span data-stu-id="b8651-104">SYNTAX</span></span>

### <span data-ttu-id="b8651-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b8651-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8651-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b8651-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8651-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b8651-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8651-108">說明</span><span class="sxs-lookup"><span data-stu-id="b8651-108">DESCRIPTION</span></span>
<span data-ttu-id="b8651-109">您可以根據需求評估，使用使用者定義的量度來建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="b8651-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 。</span><span class="sxs-lookup"><span data-stu-id="b8651-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="b8651-111">示例</span><span class="sxs-lookup"><span data-stu-id="b8651-111">EXAMPLES</span></span>

### <span data-ttu-id="b8651-112">範例1</span><span class="sxs-lookup"><span data-stu-id="b8651-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="b8651-113">使用預設中繼資料建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="b8651-114">範例2</span><span class="sxs-lookup"><span data-stu-id="b8651-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="b8651-115">建立具有優先順序3的邊緣部署，當裝置在建築物9中加上標籤且環境為「test」時，就會套用條件3。</span><span class="sxs-lookup"><span data-stu-id="b8651-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="b8651-116">範例2</span><span class="sxs-lookup"><span data-stu-id="b8651-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="b8651-117">使用使用者規格建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="b8651-118">範例3</span><span class="sxs-lookup"><span data-stu-id="b8651-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="b8651-119">建立有標籤的邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="b8651-120">範例4</span><span class="sxs-lookup"><span data-stu-id="b8651-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="b8651-121">建立包含內容的邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="b8651-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="b8651-122">參數</span><span class="sxs-lookup"><span data-stu-id="b8651-122">PARAMETERS</span></span>

### <span data-ttu-id="b8651-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8651-123">-DefaultProfile</span></span>
<span data-ttu-id="b8651-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8651-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8651-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8651-125">-InputObject</span></span>
<span data-ttu-id="b8651-126">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="b8651-126">IotHub object</span></span>

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

### <span data-ttu-id="b8651-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b8651-127">-IotHubName</span></span>
<span data-ttu-id="b8651-128">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="b8651-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b8651-129">-標籤</span><span class="sxs-lookup"><span data-stu-id="b8651-129">-Label</span></span>
<span data-ttu-id="b8651-130">要套用至目標部署的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="b8651-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="b8651-131">-公制</span><span class="sxs-lookup"><span data-stu-id="b8651-131">-Metric</span></span>
<span data-ttu-id="b8651-132">IoT Edge 部署指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="b8651-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="b8651-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="b8651-133">-ModulesContent</span></span>
<span data-ttu-id="b8651-134">IoT Edge 裝置的模組部署內容。</span><span class="sxs-lookup"><span data-stu-id="b8651-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="b8651-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8651-135">-Name</span></span>
<span data-ttu-id="b8651-136">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8651-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b8651-137">-優先順序</span><span class="sxs-lookup"><span data-stu-id="b8651-137">-Priority</span></span>
<span data-ttu-id="b8651-138">在爭用規則情況下，部署的體重 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="b8651-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="b8651-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8651-139">-ResourceGroupName</span></span>
<span data-ttu-id="b8651-140">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="b8651-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b8651-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8651-141">-ResourceId</span></span>
<span data-ttu-id="b8651-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b8651-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b8651-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="b8651-143">-TargetCondition</span></span>
<span data-ttu-id="b8651-144">將邊緣部署套用至其中的目標條件。</span><span class="sxs-lookup"><span data-stu-id="b8651-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="b8651-145">-確認</span><span class="sxs-lookup"><span data-stu-id="b8651-145">-Confirm</span></span>
<span data-ttu-id="b8651-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b8651-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8651-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8651-147">-WhatIf</span></span>
<span data-ttu-id="b8651-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8651-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8651-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8651-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8651-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8651-150">CommonParameters</span></span>
<span data-ttu-id="b8651-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b8651-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8651-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b8651-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8651-153">輸入</span><span class="sxs-lookup"><span data-stu-id="b8651-153">INPUTS</span></span>

### <span data-ttu-id="b8651-154">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="b8651-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b8651-155">System.object</span><span class="sxs-lookup"><span data-stu-id="b8651-155">System.String</span></span>

## <span data-ttu-id="b8651-156">輸出</span><span class="sxs-lookup"><span data-stu-id="b8651-156">OUTPUTS</span></span>

### <span data-ttu-id="b8651-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="b8651-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="b8651-158">筆記</span><span class="sxs-lookup"><span data-stu-id="b8651-158">NOTES</span></span>

## <span data-ttu-id="b8651-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8651-159">RELATED LINKS</span></span>
