---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139074"
---
# <span data-ttu-id="94279-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="94279-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="94279-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94279-102">SYNOPSIS</span></span>
<span data-ttu-id="94279-103">喚醒 [啟動 IoT Edge 部署規格] 查詢。</span><span class="sxs-lookup"><span data-stu-id="94279-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="94279-104">句法</span><span class="sxs-lookup"><span data-stu-id="94279-104">SYNTAX</span></span>

### <span data-ttu-id="94279-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94279-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94279-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94279-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94279-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="94279-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94279-108">說明</span><span class="sxs-lookup"><span data-stu-id="94279-108">DESCRIPTION</span></span>
<span data-ttu-id="94279-109">評估在 IoT Edge 部署中定義的目標自訂或系統規格。</span><span class="sxs-lookup"><span data-stu-id="94279-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="94279-110">預先定義的系統規格是由 Iot 中樞計算且無法自訂。</span><span class="sxs-lookup"><span data-stu-id="94279-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="94279-111">「目標」顯示與部署目標條件相符的 IoT 邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="94279-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="94279-112">「已套用」會顯示由另一個較高優先順序的部署所無法進行目標的目標 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="94279-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="94279-113">「報告成功」顯示已報告已成功部署模組的 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="94279-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="94279-114">「報告失敗」會顯示已報告已順利部署一個或多個模組的 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="94279-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="94279-115">若要進一步調查錯誤，請遠端連線到這些裝置並查看記錄檔。</span><span class="sxs-lookup"><span data-stu-id="94279-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="94279-116">示例</span><span class="sxs-lookup"><span data-stu-id="94279-116">EXAMPLES</span></span>

### <span data-ttu-id="94279-117">範例1</span><span class="sxs-lookup"><span data-stu-id="94279-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="94279-118">評估自訂的「warningLimit」指標。</span><span class="sxs-lookup"><span data-stu-id="94279-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="94279-119">範例2</span><span class="sxs-lookup"><span data-stu-id="94279-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="94279-120">評估系統「報告成功」的指標。</span><span class="sxs-lookup"><span data-stu-id="94279-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="94279-121">參數</span><span class="sxs-lookup"><span data-stu-id="94279-121">PARAMETERS</span></span>

### <span data-ttu-id="94279-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94279-122">-DefaultProfile</span></span>
<span data-ttu-id="94279-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94279-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94279-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94279-124">-InputObject</span></span>
<span data-ttu-id="94279-125">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="94279-125">IotHub object</span></span>

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

### <span data-ttu-id="94279-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="94279-126">-IotHubName</span></span>
<span data-ttu-id="94279-127">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="94279-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="94279-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="94279-128">-MetricName</span></span>
<span data-ttu-id="94279-129">評估的目標度量。</span><span class="sxs-lookup"><span data-stu-id="94279-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="94279-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="94279-130">-MetricType</span></span>
<span data-ttu-id="94279-131">指出應該使用哪個公制集合來尋找公制。</span><span class="sxs-lookup"><span data-stu-id="94279-131">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94279-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="94279-132">-Name</span></span>
<span data-ttu-id="94279-133">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="94279-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="94279-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94279-134">-ResourceGroupName</span></span>
<span data-ttu-id="94279-135">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="94279-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="94279-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94279-136">-ResourceId</span></span>
<span data-ttu-id="94279-137">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="94279-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="94279-138">-確認</span><span class="sxs-lookup"><span data-stu-id="94279-138">-Confirm</span></span>
<span data-ttu-id="94279-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94279-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94279-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94279-140">-WhatIf</span></span>
<span data-ttu-id="94279-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94279-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94279-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94279-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94279-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94279-143">CommonParameters</span></span>
<span data-ttu-id="94279-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94279-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94279-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94279-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94279-146">輸入</span><span class="sxs-lookup"><span data-stu-id="94279-146">INPUTS</span></span>

### <span data-ttu-id="94279-147">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="94279-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="94279-148">System.object</span><span class="sxs-lookup"><span data-stu-id="94279-148">System.String</span></span>

## <span data-ttu-id="94279-149">輸出</span><span class="sxs-lookup"><span data-stu-id="94279-149">OUTPUTS</span></span>

### <span data-ttu-id="94279-150">PSConfigurationMetricsResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="94279-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="94279-151">筆記</span><span class="sxs-lookup"><span data-stu-id="94279-151">NOTES</span></span>

## <span data-ttu-id="94279-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="94279-152">RELATED LINKS</span></span>
