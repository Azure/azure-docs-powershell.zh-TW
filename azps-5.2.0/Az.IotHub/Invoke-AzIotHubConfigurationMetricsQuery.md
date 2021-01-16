---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278120"
---
# <span data-ttu-id="89db0-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="89db0-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="89db0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89db0-102">SYNOPSIS</span></span>
<span data-ttu-id="89db0-103">喚醒呼叫 [IoT 裝置設定度量值] 查詢。</span><span class="sxs-lookup"><span data-stu-id="89db0-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="89db0-104">句法</span><span class="sxs-lookup"><span data-stu-id="89db0-104">SYNTAX</span></span>

### <span data-ttu-id="89db0-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89db0-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89db0-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89db0-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89db0-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89db0-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89db0-108">說明</span><span class="sxs-lookup"><span data-stu-id="89db0-108">DESCRIPTION</span></span>
<span data-ttu-id="89db0-109">評估在 IoT 裝置配置中定義的目標自訂或系統規格。</span><span class="sxs-lookup"><span data-stu-id="89db0-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="89db0-110">預先定義的系統規格是由 Iot 中樞計算且無法自訂。</span><span class="sxs-lookup"><span data-stu-id="89db0-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="89db0-111">「目標」指定符合目標條件的裝置 twins 數目。</span><span class="sxs-lookup"><span data-stu-id="89db0-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="89db0-112">"已套用"：已指定由設定修改的裝置 twins 數目。</span><span class="sxs-lookup"><span data-stu-id="89db0-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="89db0-113">示例</span><span class="sxs-lookup"><span data-stu-id="89db0-113">EXAMPLES</span></span>

### <span data-ttu-id="89db0-114">範例1</span><span class="sxs-lookup"><span data-stu-id="89db0-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="89db0-115">評估自訂的「warningLimit」指標。</span><span class="sxs-lookup"><span data-stu-id="89db0-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="89db0-116">範例2</span><span class="sxs-lookup"><span data-stu-id="89db0-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="89db0-117">評估系統「已套用」的指標。</span><span class="sxs-lookup"><span data-stu-id="89db0-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="89db0-118">參數</span><span class="sxs-lookup"><span data-stu-id="89db0-118">PARAMETERS</span></span>

### <span data-ttu-id="89db0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89db0-119">-DefaultProfile</span></span>
<span data-ttu-id="89db0-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89db0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89db0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89db0-121">-InputObject</span></span>
<span data-ttu-id="89db0-122">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="89db0-122">IotHub object</span></span>

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

### <span data-ttu-id="89db0-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="89db0-123">-IotHubName</span></span>
<span data-ttu-id="89db0-124">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="89db0-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="89db0-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="89db0-125">-MetricName</span></span>
<span data-ttu-id="89db0-126">評估的目標度量。</span><span class="sxs-lookup"><span data-stu-id="89db0-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="89db0-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="89db0-127">-MetricType</span></span>
<span data-ttu-id="89db0-128">指出應該使用哪個公制集合來尋找公制。</span><span class="sxs-lookup"><span data-stu-id="89db0-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="89db0-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="89db0-129">-Name</span></span>
<span data-ttu-id="89db0-130">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89db0-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="89db0-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89db0-131">-ResourceGroupName</span></span>
<span data-ttu-id="89db0-132">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="89db0-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89db0-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89db0-133">-ResourceId</span></span>
<span data-ttu-id="89db0-134">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89db0-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="89db0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="89db0-135">-Confirm</span></span>
<span data-ttu-id="89db0-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="89db0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89db0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89db0-137">-WhatIf</span></span>
<span data-ttu-id="89db0-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89db0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89db0-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89db0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89db0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89db0-140">CommonParameters</span></span>
<span data-ttu-id="89db0-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89db0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89db0-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89db0-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89db0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="89db0-143">INPUTS</span></span>

### <span data-ttu-id="89db0-144">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="89db0-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="89db0-145">System.object</span><span class="sxs-lookup"><span data-stu-id="89db0-145">System.String</span></span>

## <span data-ttu-id="89db0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="89db0-146">OUTPUTS</span></span>

### <span data-ttu-id="89db0-147">PSConfigurationMetricsResult （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="89db0-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="89db0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="89db0-148">NOTES</span></span>

## <span data-ttu-id="89db0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="89db0-149">RELATED LINKS</span></span>
