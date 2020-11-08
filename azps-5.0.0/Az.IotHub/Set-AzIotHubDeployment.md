---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141697"
---
# <span data-ttu-id="df24e-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="df24e-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="df24e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df24e-102">SYNOPSIS</span></span>
<span data-ttu-id="df24e-103">更新 IoT Edge 部署的可變欄位。</span><span class="sxs-lookup"><span data-stu-id="df24e-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="df24e-104">句法</span><span class="sxs-lookup"><span data-stu-id="df24e-104">SYNTAX</span></span>

### <span data-ttu-id="df24e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="df24e-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df24e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df24e-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df24e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df24e-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df24e-108">說明</span><span class="sxs-lookup"><span data-stu-id="df24e-108">DESCRIPTION</span></span>
<span data-ttu-id="df24e-109">更新 IoT Edge 部署的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="df24e-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="df24e-110">注意：配置內容是不可變的。</span><span class="sxs-lookup"><span data-stu-id="df24e-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="df24e-111">可以更新的設定屬性為「標籤」、「公制」、「priority」和「targetCondition」。</span><span class="sxs-lookup"><span data-stu-id="df24e-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="df24e-112">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  。</span><span class="sxs-lookup"><span data-stu-id="df24e-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="df24e-113">示例</span><span class="sxs-lookup"><span data-stu-id="df24e-113">EXAMPLES</span></span>

### <span data-ttu-id="df24e-114">範例1</span><span class="sxs-lookup"><span data-stu-id="df24e-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="df24e-115">變更 IoT Edge 部署的優先順序並更新其目標條件。</span><span class="sxs-lookup"><span data-stu-id="df24e-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="df24e-116">參數</span><span class="sxs-lookup"><span data-stu-id="df24e-116">PARAMETERS</span></span>

### <span data-ttu-id="df24e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df24e-117">-DefaultProfile</span></span>
<span data-ttu-id="df24e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df24e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df24e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="df24e-119">-Force</span></span>
<span data-ttu-id="df24e-120">允許取代部署物件，即使在上次檢索之後，仍會進行更新。</span><span class="sxs-lookup"><span data-stu-id="df24e-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="df24e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df24e-121">-InputObject</span></span>
<span data-ttu-id="df24e-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="df24e-122">IotHub object</span></span>

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

### <span data-ttu-id="df24e-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="df24e-123">-IotHubName</span></span>
<span data-ttu-id="df24e-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="df24e-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="df24e-125">-標籤</span><span class="sxs-lookup"><span data-stu-id="df24e-125">-Label</span></span>
<span data-ttu-id="df24e-126">要套用至目標部署的標籤地圖。</span><span class="sxs-lookup"><span data-stu-id="df24e-126">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="df24e-127">-公制</span><span class="sxs-lookup"><span data-stu-id="df24e-127">-Metric</span></span>
<span data-ttu-id="df24e-128">IoT Edge 部署指標定義的查詢集合。</span><span class="sxs-lookup"><span data-stu-id="df24e-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="df24e-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="df24e-129">-Name</span></span>
<span data-ttu-id="df24e-130">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="df24e-130">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="df24e-131">-優先順序</span><span class="sxs-lookup"><span data-stu-id="df24e-131">-Priority</span></span>
<span data-ttu-id="df24e-132">在爭用規則情況下，部署的體重 (最高的 wins) 。</span><span class="sxs-lookup"><span data-stu-id="df24e-132">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="df24e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df24e-133">-ResourceGroupName</span></span>
<span data-ttu-id="df24e-134">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="df24e-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df24e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df24e-135">-ResourceId</span></span>
<span data-ttu-id="df24e-136">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="df24e-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="df24e-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="df24e-137">-TargetCondition</span></span>
<span data-ttu-id="df24e-138">將邊緣部署套用至其中的目標條件。</span><span class="sxs-lookup"><span data-stu-id="df24e-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="df24e-139">-確認</span><span class="sxs-lookup"><span data-stu-id="df24e-139">-Confirm</span></span>
<span data-ttu-id="df24e-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="df24e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df24e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df24e-141">-WhatIf</span></span>
<span data-ttu-id="df24e-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df24e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df24e-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df24e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df24e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df24e-144">CommonParameters</span></span>
<span data-ttu-id="df24e-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df24e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df24e-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df24e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df24e-147">輸入</span><span class="sxs-lookup"><span data-stu-id="df24e-147">INPUTS</span></span>

### <span data-ttu-id="df24e-148">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="df24e-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="df24e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="df24e-149">System.String</span></span>

## <span data-ttu-id="df24e-150">輸出</span><span class="sxs-lookup"><span data-stu-id="df24e-150">OUTPUTS</span></span>

### <span data-ttu-id="df24e-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="df24e-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="df24e-152">筆記</span><span class="sxs-lookup"><span data-stu-id="df24e-152">NOTES</span></span>

## <span data-ttu-id="df24e-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="df24e-153">RELATED LINKS</span></span>
