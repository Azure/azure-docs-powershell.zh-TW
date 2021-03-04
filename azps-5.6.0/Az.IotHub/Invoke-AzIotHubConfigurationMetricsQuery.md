---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 07772e7d0cbec3a2cd8241de3afa0100e1c253cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904670"
---
# <span data-ttu-id="31aea-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="31aea-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="31aea-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31aea-102">SYNOPSIS</span></span>
<span data-ttu-id="31aea-103">請用 IoT 裝置組配置計量查詢。</span><span class="sxs-lookup"><span data-stu-id="31aea-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="31aea-104">語法</span><span class="sxs-lookup"><span data-stu-id="31aea-104">SYNTAX</span></span>

### <span data-ttu-id="31aea-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="31aea-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31aea-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31aea-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31aea-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31aea-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31aea-108">描述</span><span class="sxs-lookup"><span data-stu-id="31aea-108">DESCRIPTION</span></span>
<span data-ttu-id="31aea-109">評估 IoT 裝置組配置中定義的目標自訂或系統度量。</span><span class="sxs-lookup"><span data-stu-id="31aea-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="31aea-110">有預先定義的系統度量是由 Iot Hub 計算，無法自訂。</span><span class="sxs-lookup"><span data-stu-id="31aea-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="31aea-111">「已指定」指定符合目標條件的裝置放大器數目。</span><span class="sxs-lookup"><span data-stu-id="31aea-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="31aea-112">「已使用」指定已由組組修改的裝置直方裝置數目。</span><span class="sxs-lookup"><span data-stu-id="31aea-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="31aea-113">例子</span><span class="sxs-lookup"><span data-stu-id="31aea-113">EXAMPLES</span></span>

### <span data-ttu-id="31aea-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="31aea-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="31aea-115">評估自訂定義的 "warningLimit" 度量。</span><span class="sxs-lookup"><span data-stu-id="31aea-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="31aea-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="31aea-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="31aea-117">評估系統 'applied' 度量。</span><span class="sxs-lookup"><span data-stu-id="31aea-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="31aea-118">參數</span><span class="sxs-lookup"><span data-stu-id="31aea-118">PARAMETERS</span></span>

### <span data-ttu-id="31aea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aea-119">-DefaultProfile</span></span>
<span data-ttu-id="31aea-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31aea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31aea-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31aea-121">-InputObject</span></span>
<span data-ttu-id="31aea-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="31aea-122">IotHub object</span></span>

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

### <span data-ttu-id="31aea-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="31aea-123">-IotHubName</span></span>
<span data-ttu-id="31aea-124">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="31aea-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="31aea-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="31aea-125">-MetricName</span></span>
<span data-ttu-id="31aea-126">評估的目標度量。</span><span class="sxs-lookup"><span data-stu-id="31aea-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="31aea-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="31aea-127">-MetricType</span></span>
<span data-ttu-id="31aea-128">指出應該使用哪些計量集合來尋找度量。</span><span class="sxs-lookup"><span data-stu-id="31aea-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="31aea-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="31aea-129">-Name</span></span>
<span data-ttu-id="31aea-130">組配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="31aea-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="31aea-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31aea-131">-ResourceGroupName</span></span>
<span data-ttu-id="31aea-132">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="31aea-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="31aea-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31aea-133">-ResourceId</span></span>
<span data-ttu-id="31aea-134">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="31aea-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="31aea-135">-確認</span><span class="sxs-lookup"><span data-stu-id="31aea-135">-Confirm</span></span>
<span data-ttu-id="31aea-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31aea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31aea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31aea-137">-WhatIf</span></span>
<span data-ttu-id="31aea-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31aea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31aea-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31aea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31aea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aea-140">CommonParameters</span></span>
<span data-ttu-id="31aea-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31aea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aea-142">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="31aea-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aea-143">輸入</span><span class="sxs-lookup"><span data-stu-id="31aea-143">INPUTS</span></span>

### <span data-ttu-id="31aea-144">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="31aea-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="31aea-145">System.String</span><span class="sxs-lookup"><span data-stu-id="31aea-145">System.String</span></span>

## <span data-ttu-id="31aea-146">輸出</span><span class="sxs-lookup"><span data-stu-id="31aea-146">OUTPUTS</span></span>

### <span data-ttu-id="31aea-147">Microsoft.Azure.Commands.management.IotHub.models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="31aea-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="31aea-148">筆記</span><span class="sxs-lookup"><span data-stu-id="31aea-148">NOTES</span></span>

## <span data-ttu-id="31aea-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="31aea-149">RELATED LINKS</span></span>
