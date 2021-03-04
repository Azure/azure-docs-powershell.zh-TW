---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 02870d2bf0016704328e157b948b9db8ae1207f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904666"
---
# <span data-ttu-id="540a5-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="540a5-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="540a5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="540a5-102">SYNOPSIS</span></span>
<span data-ttu-id="540a5-103">請用 IoT Edge 部署計量查詢。</span><span class="sxs-lookup"><span data-stu-id="540a5-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="540a5-104">語法</span><span class="sxs-lookup"><span data-stu-id="540a5-104">SYNTAX</span></span>

### <span data-ttu-id="540a5-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="540a5-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="540a5-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="540a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="540a5-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="540a5-108">描述</span><span class="sxs-lookup"><span data-stu-id="540a5-108">DESCRIPTION</span></span>
<span data-ttu-id="540a5-109">評估 IoT Edge 部署中定義的目標自訂或系統度量。</span><span class="sxs-lookup"><span data-stu-id="540a5-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="540a5-110">有預先定義的系統度量是由 Iot Hub 計算，無法自訂。</span><span class="sxs-lookup"><span data-stu-id="540a5-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="540a5-111">「已鎖定」顯示符合部署目標條件的 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="540a5-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="540a5-112">「已使用」顯示其他較高優先順序部署未鎖定的目標 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="540a5-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="540a5-113">「報告成功」顯示已報告模組已成功部署的 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="540a5-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="540a5-114">「報告失敗」顯示已報告尚未成功部署一或多個模組的 IoT Edge 裝置。</span><span class="sxs-lookup"><span data-stu-id="540a5-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="540a5-115">若要進一步調查錯誤，請從遠端連線到這些裝置，並查看記錄檔。</span><span class="sxs-lookup"><span data-stu-id="540a5-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="540a5-116">例子</span><span class="sxs-lookup"><span data-stu-id="540a5-116">EXAMPLES</span></span>

### <span data-ttu-id="540a5-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="540a5-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="540a5-118">評估自訂定義的 "warningLimit" 度量。</span><span class="sxs-lookup"><span data-stu-id="540a5-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="540a5-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="540a5-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="540a5-120">評估系統的 "Reporting Success" 度量。</span><span class="sxs-lookup"><span data-stu-id="540a5-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="540a5-121">參數</span><span class="sxs-lookup"><span data-stu-id="540a5-121">PARAMETERS</span></span>

### <span data-ttu-id="540a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540a5-122">-DefaultProfile</span></span>
<span data-ttu-id="540a5-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="540a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="540a5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="540a5-124">-InputObject</span></span>
<span data-ttu-id="540a5-125">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="540a5-125">IotHub object</span></span>

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

### <span data-ttu-id="540a5-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="540a5-126">-IotHubName</span></span>
<span data-ttu-id="540a5-127">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="540a5-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="540a5-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="540a5-128">-MetricName</span></span>
<span data-ttu-id="540a5-129">評估的目標度量。</span><span class="sxs-lookup"><span data-stu-id="540a5-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="540a5-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="540a5-130">-MetricType</span></span>
<span data-ttu-id="540a5-131">指出應該使用哪些計量集合來尋找度量。</span><span class="sxs-lookup"><span data-stu-id="540a5-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="540a5-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="540a5-132">-Name</span></span>
<span data-ttu-id="540a5-133">部署的識別碼。</span><span class="sxs-lookup"><span data-stu-id="540a5-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="540a5-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540a5-134">-ResourceGroupName</span></span>
<span data-ttu-id="540a5-135">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="540a5-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="540a5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="540a5-136">-ResourceId</span></span>
<span data-ttu-id="540a5-137">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="540a5-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="540a5-138">-確認</span><span class="sxs-lookup"><span data-stu-id="540a5-138">-Confirm</span></span>
<span data-ttu-id="540a5-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="540a5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540a5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540a5-140">-WhatIf</span></span>
<span data-ttu-id="540a5-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="540a5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540a5-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="540a5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540a5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a5-143">CommonParameters</span></span>
<span data-ttu-id="540a5-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="540a5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a5-145">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="540a5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="540a5-146">INPUTS</span></span>

### <span data-ttu-id="540a5-147">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="540a5-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="540a5-148">System.String</span><span class="sxs-lookup"><span data-stu-id="540a5-148">System.String</span></span>

## <span data-ttu-id="540a5-149">輸出</span><span class="sxs-lookup"><span data-stu-id="540a5-149">OUTPUTS</span></span>

### <span data-ttu-id="540a5-150">Microsoft.Azure.Commands.management.IotHub.models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="540a5-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="540a5-151">筆記</span><span class="sxs-lookup"><span data-stu-id="540a5-151">NOTES</span></span>

## <span data-ttu-id="540a5-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="540a5-152">RELATED LINKS</span></span>
