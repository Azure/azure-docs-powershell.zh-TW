---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 80494fd18216ce42883a962920ab78bbc2aa628b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913889"
---
# <span data-ttu-id="d68b4-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="d68b4-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="d68b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d68b4-102">SYNOPSIS</span></span>
<span data-ttu-id="d68b4-103">在目標 IoT 中心新增 IoT Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="d68b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="d68b4-104">SYNTAX</span></span>

### <span data-ttu-id="d68b4-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d68b4-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68b4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d68b4-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d68b4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d68b4-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d68b4-108">描述</span><span class="sxs-lookup"><span data-stu-id="d68b4-108">DESCRIPTION</span></span>
<span data-ttu-id="d68b4-109">您可以使用使用者定義的隨需評估度量來建立 Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="d68b4-110">請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring 詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="d68b4-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="d68b4-111">例子</span><span class="sxs-lookup"><span data-stu-id="d68b4-111">EXAMPLES</span></span>

### <span data-ttu-id="d68b4-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d68b4-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="d68b4-113">使用預設中繼資料建立 Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="d68b4-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="d68b4-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="d68b4-115">建立優先順序為 3 的 Edge 部署，此優先順序適用于在建築物 9 中標記裝置且環境為'測試'的條件。</span><span class="sxs-lookup"><span data-stu-id="d68b4-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="d68b4-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="d68b4-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="d68b4-117">使用使用者計量建立 Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="d68b4-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="d68b4-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="d68b4-119">使用標籤建立 Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="d68b4-120">範例 4</span><span class="sxs-lookup"><span data-stu-id="d68b4-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="d68b4-121">建立包含內容的 Edge 部署。</span><span class="sxs-lookup"><span data-stu-id="d68b4-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="d68b4-122">參數</span><span class="sxs-lookup"><span data-stu-id="d68b4-122">PARAMETERS</span></span>

### <span data-ttu-id="d68b4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68b4-123">-DefaultProfile</span></span>
<span data-ttu-id="d68b4-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d68b4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68b4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d68b4-125">-InputObject</span></span>
<span data-ttu-id="d68b4-126">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="d68b4-126">IotHub object</span></span>

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

### <span data-ttu-id="d68b4-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d68b4-127">-IotHubName</span></span>
<span data-ttu-id="d68b4-128">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="d68b4-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d68b4-129">-標籤</span><span class="sxs-lookup"><span data-stu-id="d68b4-129">-Label</span></span>
<span data-ttu-id="d68b4-130">要用於目標部署的標號地圖。</span><span class="sxs-lookup"><span data-stu-id="d68b4-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="d68b4-131">-公制</span><span class="sxs-lookup"><span data-stu-id="d68b4-131">-Metric</span></span>
<span data-ttu-id="d68b4-132">IoT Edge 部署計量定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="d68b4-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="d68b4-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="d68b4-133">-ModulesContent</span></span>
<span data-ttu-id="d68b4-134">IoT Edge 裝置模組的部署內容。</span><span class="sxs-lookup"><span data-stu-id="d68b4-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="d68b4-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="d68b4-135">-Name</span></span>
<span data-ttu-id="d68b4-136">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d68b4-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="d68b4-137">-優先順序</span><span class="sxs-lookup"><span data-stu-id="d68b4-137">-Priority</span></span>
<span data-ttu-id="d68b4-138">在有相互衝突規則的情況下，部署 (優先) 。</span><span class="sxs-lookup"><span data-stu-id="d68b4-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="d68b4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68b4-139">-ResourceGroupName</span></span>
<span data-ttu-id="d68b4-140">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="d68b4-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d68b4-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d68b4-141">-ResourceId</span></span>
<span data-ttu-id="d68b4-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d68b4-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d68b4-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d68b4-143">-TargetCondition</span></span>
<span data-ttu-id="d68b4-144">適用于 Edge 部署的目標條件。</span><span class="sxs-lookup"><span data-stu-id="d68b4-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="d68b4-145">-確認</span><span class="sxs-lookup"><span data-stu-id="d68b4-145">-Confirm</span></span>
<span data-ttu-id="d68b4-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d68b4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d68b4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d68b4-147">-WhatIf</span></span>
<span data-ttu-id="d68b4-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d68b4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d68b4-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d68b4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d68b4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68b4-150">CommonParameters</span></span>
<span data-ttu-id="d68b4-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d68b4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68b4-152">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d68b4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68b4-153">輸入</span><span class="sxs-lookup"><span data-stu-id="d68b4-153">INPUTS</span></span>

### <span data-ttu-id="d68b4-154">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d68b4-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d68b4-155">System.String</span><span class="sxs-lookup"><span data-stu-id="d68b4-155">System.String</span></span>

## <span data-ttu-id="d68b4-156">輸出</span><span class="sxs-lookup"><span data-stu-id="d68b4-156">OUTPUTS</span></span>

### <span data-ttu-id="d68b4-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d68b4-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="d68b4-158">筆記</span><span class="sxs-lookup"><span data-stu-id="d68b4-158">NOTES</span></span>

## <span data-ttu-id="d68b4-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="d68b4-159">RELATED LINKS</span></span>
