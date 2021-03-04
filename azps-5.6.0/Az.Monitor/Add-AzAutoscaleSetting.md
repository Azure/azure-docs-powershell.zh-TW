---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b761422a3a2c81d1070dbc5852ca67e2ac91117c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909013"
---
# <span data-ttu-id="94f46-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="94f46-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94f46-102">SYNOPSIS</span></span>
<span data-ttu-id="94f46-103">建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="94f46-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="94f46-104">語法</span><span class="sxs-lookup"><span data-stu-id="94f46-104">SYNTAX</span></span>

### <span data-ttu-id="94f46-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f46-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f46-107">描述</span><span class="sxs-lookup"><span data-stu-id="94f46-107">DESCRIPTION</span></span>
<span data-ttu-id="94f46-108">**Add-AzAutoscaleSetting** Cmdlet 會建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="94f46-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="94f46-109">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="94f46-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="94f46-110">例子</span><span class="sxs-lookup"><span data-stu-id="94f46-110">EXAMPLES</span></span>

### <span data-ttu-id="94f46-111">範例 1：建立自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="94f46-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="94f46-112">前兩個命令使用 [New-AzAutoscaleRule](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) 建立兩個自動縮放規則，$Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="94f46-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="94f46-113">第三個和第四個命令使用 [New-AzAutoscaleProfile，](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) 使用 $Profile 1 和 $Profile 2 建立自動縮放設定檔$Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="94f46-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="94f46-114">最後一個命令會使用 $Profile 1 和 $Profile 2 中的設定檔建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="94f46-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="94f46-115">參數</span><span class="sxs-lookup"><span data-stu-id="94f46-115">PARAMETERS</span></span>

### <span data-ttu-id="94f46-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="94f46-116">-AutoscaleProfile</span></span>
<span data-ttu-id="94f46-117">指定要新增到自動縮放設定之配置檔案清單，或指定$Null設定檔的清單。</span><span class="sxs-lookup"><span data-stu-id="94f46-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f46-118">-DefaultProfile</span></span>
<span data-ttu-id="94f46-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="94f46-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94f46-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-120">-DisableSetting</span></span>
<span data-ttu-id="94f46-121">停用現有的自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="94f46-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f46-122">-InputObject</span></span>
<span data-ttu-id="94f46-123">自動縮放設定的完整規格</span><span class="sxs-lookup"><span data-stu-id="94f46-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-124">-位置</span><span class="sxs-lookup"><span data-stu-id="94f46-124">-Location</span></span>
<span data-ttu-id="94f46-125">指定自動縮放設定的位置。</span><span class="sxs-lookup"><span data-stu-id="94f46-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="94f46-126">-Name</span></span>
<span data-ttu-id="94f46-127">指定要建立之自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="94f46-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-128">-通知</span><span class="sxs-lookup"><span data-stu-id="94f46-128">-Notification</span></span>
<span data-ttu-id="94f46-129">指定逗號分隔通知的清單。</span><span class="sxs-lookup"><span data-stu-id="94f46-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f46-130">-ResourceGroupName</span></span>
<span data-ttu-id="94f46-131">指定與自動縮放設定相關聯的資源資源組名。</span><span class="sxs-lookup"><span data-stu-id="94f46-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="94f46-132">-TargetResourceId</span></span>
<span data-ttu-id="94f46-133">指定要自動縮放的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="94f46-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f46-134">-確認</span><span class="sxs-lookup"><span data-stu-id="94f46-134">-Confirm</span></span>
<span data-ttu-id="94f46-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94f46-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f46-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f46-136">-WhatIf</span></span>
<span data-ttu-id="94f46-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f46-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94f46-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f46-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f46-139">CommonParameters</span></span>
<span data-ttu-id="94f46-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94f46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f46-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94f46-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f46-142">輸入</span><span class="sxs-lookup"><span data-stu-id="94f46-142">INPUTS</span></span>

### <span data-ttu-id="94f46-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="94f46-144">System.String</span><span class="sxs-lookup"><span data-stu-id="94f46-144">System.String</span></span>

### <span data-ttu-id="94f46-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="94f46-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="94f46-146">System.Collections.generic.List'1[[Microsoft.Azure.management.Monitor.management.models.AutoscaleProfile，Microsoft.Azure.PowerShell.Cmdlets.Monitor， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="94f46-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="94f46-147">System.Collections.generic.List'1[[Microsoft.Azure.management.Monitor.management.models.AutoscaleNotification，Microsoft.Azure.PowerShell.Cmdlets.Monitor， Version=1.0.0.0， Culture=neutral， PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="94f46-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="94f46-148">輸出</span><span class="sxs-lookup"><span data-stu-id="94f46-148">OUTPUTS</span></span>

### <span data-ttu-id="94f46-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94f46-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="94f46-150">筆記</span><span class="sxs-lookup"><span data-stu-id="94f46-150">NOTES</span></span>

## <span data-ttu-id="94f46-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f46-151">RELATED LINKS</span></span>

[<span data-ttu-id="94f46-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="94f46-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="94f46-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="94f46-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="94f46-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="94f46-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="94f46-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


