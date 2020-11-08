---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127916"
---
# <span data-ttu-id="893e5-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="893e5-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="893e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="893e5-102">SYNOPSIS</span></span>
<span data-ttu-id="893e5-103">在目標 IoT 中樞中新增 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="893e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="893e5-104">SYNTAX</span></span>

### <span data-ttu-id="893e5-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="893e5-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="893e5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="893e5-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="893e5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="893e5-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="893e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="893e5-108">DESCRIPTION</span></span>
<span data-ttu-id="893e5-109">您可以根據需求評估，使用使用者定義的量度來建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="893e5-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 。</span><span class="sxs-lookup"><span data-stu-id="893e5-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="893e5-111">示例</span><span class="sxs-lookup"><span data-stu-id="893e5-111">EXAMPLES</span></span>

### <span data-ttu-id="893e5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="893e5-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="893e5-113">使用預設中繼資料建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="893e5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="893e5-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="893e5-115">建立具有優先順序3的邊緣部署，當裝置在建築物9中加上標籤且環境為「test」時，就會套用條件3。</span><span class="sxs-lookup"><span data-stu-id="893e5-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="893e5-116">範例2</span><span class="sxs-lookup"><span data-stu-id="893e5-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="893e5-117">使用使用者規格建立邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="893e5-118">範例3</span><span class="sxs-lookup"><span data-stu-id="893e5-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="893e5-119">建立有標籤的邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="893e5-120">範例4</span><span class="sxs-lookup"><span data-stu-id="893e5-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="893e5-121">建立包含內容的邊緣部署。</span><span class="sxs-lookup"><span data-stu-id="893e5-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="893e5-122">參數</span><span class="sxs-lookup"><span data-stu-id="893e5-122">PARAMETERS</span></span>

### <span data-ttu-id="893e5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893e5-123">-DefaultProfile</span></span>
<span data-ttu-id="893e5-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="893e5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="893e5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="893e5-125">-InputObject</span></span>
<span data-ttu-id="893e5-126">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="893e5-126">IotHub object</span></span>

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

### <span data-ttu-id="893e5-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="893e5-127">-IotHubName</span></span>
<span data-ttu-id="893e5-128">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="893e5-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="893e5-129">-標籤</span><span class="sxs-lookup"><span data-stu-id="893e5-129">-Label</span></span>
<span data-ttu-id="893e5-130">要套用至目標部署的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="893e5-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="893e5-131">-公制</span><span class="sxs-lookup"><span data-stu-id="893e5-131">-Metric</span></span>
<span data-ttu-id="893e5-132">IoT Edge 部署指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="893e5-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="893e5-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="893e5-133">-ModulesContent</span></span>
<span data-ttu-id="893e5-134">IoT Edge 裝置的模組部署內容。</span><span class="sxs-lookup"><span data-stu-id="893e5-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="893e5-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="893e5-135">-Name</span></span>
<span data-ttu-id="893e5-136">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="893e5-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="893e5-137">-優先順序</span><span class="sxs-lookup"><span data-stu-id="893e5-137">-Priority</span></span>
<span data-ttu-id="893e5-138">在爭用規則情況下，部署的體重 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="893e5-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="893e5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893e5-139">-ResourceGroupName</span></span>
<span data-ttu-id="893e5-140">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="893e5-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="893e5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="893e5-141">-ResourceId</span></span>
<span data-ttu-id="893e5-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="893e5-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="893e5-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="893e5-143">-TargetCondition</span></span>
<span data-ttu-id="893e5-144">將邊緣部署套用至其中的目標條件。</span><span class="sxs-lookup"><span data-stu-id="893e5-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="893e5-145">-確認</span><span class="sxs-lookup"><span data-stu-id="893e5-145">-Confirm</span></span>
<span data-ttu-id="893e5-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="893e5-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="893e5-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="893e5-147">-WhatIf</span></span>
<span data-ttu-id="893e5-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="893e5-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="893e5-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="893e5-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="893e5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893e5-150">CommonParameters</span></span>
<span data-ttu-id="893e5-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="893e5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893e5-152">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="893e5-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893e5-153">輸入</span><span class="sxs-lookup"><span data-stu-id="893e5-153">INPUTS</span></span>

### <span data-ttu-id="893e5-154">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="893e5-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="893e5-155">System.object</span><span class="sxs-lookup"><span data-stu-id="893e5-155">System.String</span></span>

## <span data-ttu-id="893e5-156">輸出</span><span class="sxs-lookup"><span data-stu-id="893e5-156">OUTPUTS</span></span>

### <span data-ttu-id="893e5-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="893e5-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="893e5-158">筆記</span><span class="sxs-lookup"><span data-stu-id="893e5-158">NOTES</span></span>

## <span data-ttu-id="893e5-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="893e5-159">RELATED LINKS</span></span>
