---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 3da9950f2dfdf38bc4e1b461ffd1fcf409b445e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611821"
---
# <span data-ttu-id="e802c-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="e802c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e802c-102">SYNOPSIS</span></span>
<span data-ttu-id="e802c-103">建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="e802c-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="e802c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e802c-104">SYNTAX</span></span>

### <span data-ttu-id="e802c-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e802c-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e802c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e802c-107">DESCRIPTION</span></span>
<span data-ttu-id="e802c-108">**AzAutoscaleSetting** Cmdlet 會建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="e802c-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="e802c-109">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="e802c-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e802c-110">示例</span><span class="sxs-lookup"><span data-stu-id="e802c-110">EXAMPLES</span></span>

### <span data-ttu-id="e802c-111">範例1：建立自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="e802c-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="e802c-112">前兩個命令使用 New-AzAutoscaleRule 來建立兩個自動縮放規則，$Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="e802c-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="e802c-113">第三個和第四個命令使用 New-AzAutoscaleProfile 來建立自動縮放設定檔，$Profile 1 和 $Profile 2，使用 $Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="e802c-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="e802c-114">最終命令會使用 $Profile 1 和 $Profile 2 中的設定檔來建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="e802c-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="e802c-115">參數</span><span class="sxs-lookup"><span data-stu-id="e802c-115">PARAMETERS</span></span>

### <span data-ttu-id="e802c-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e802c-116">-AutoscaleProfile</span></span>
<span data-ttu-id="e802c-117">指定要新增到自動縮放設定的配置檔案清單，或 $Null 以新增無設定檔。</span><span class="sxs-lookup"><span data-stu-id="e802c-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="e802c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e802c-118">-DefaultProfile</span></span>
<span data-ttu-id="e802c-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e802c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e802c-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-120">-DisableSetting</span></span>
<span data-ttu-id="e802c-121">停用現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="e802c-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="e802c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e802c-122">-InputObject</span></span>
<span data-ttu-id="e802c-123">AutoscaleSetting 的完整規格</span><span class="sxs-lookup"><span data-stu-id="e802c-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="e802c-124">-位置</span><span class="sxs-lookup"><span data-stu-id="e802c-124">-Location</span></span>
<span data-ttu-id="e802c-125">指定自動縮放設定的位置。</span><span class="sxs-lookup"><span data-stu-id="e802c-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="e802c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e802c-126">-Name</span></span>
<span data-ttu-id="e802c-127">指定要建立的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="e802c-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="e802c-128">-通知</span><span class="sxs-lookup"><span data-stu-id="e802c-128">-Notification</span></span>
<span data-ttu-id="e802c-129">指定以逗號分隔的通知清單。</span><span class="sxs-lookup"><span data-stu-id="e802c-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="e802c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e802c-130">-ResourceGroupName</span></span>
<span data-ttu-id="e802c-131">指定與自動縮放設定相關聯之資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e802c-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="e802c-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e802c-132">-TargetResourceId</span></span>
<span data-ttu-id="e802c-133">指定要自動縮放的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e802c-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="e802c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e802c-134">-Confirm</span></span>
<span data-ttu-id="e802c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e802c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e802c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e802c-136">-WhatIf</span></span>
<span data-ttu-id="e802c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e802c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e802c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e802c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e802c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e802c-139">CommonParameters</span></span>
<span data-ttu-id="e802c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e802c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e802c-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e802c-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e802c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e802c-142">INPUTS</span></span>

### <span data-ttu-id="e802c-143">PSAutoscaleSetting 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e802c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="e802c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e802c-144">System.String</span></span>

### <span data-ttu-id="e802c-145">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e802c-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e802c-146">[System.object]。清單 ' 1 [AutoscaleProfile，，Marvell. PowerShell. Monitor，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="e802c-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e802c-147">[System.object]。清單 ' 1 [AutoscaleNotification，，Marvell. PowerShell. Monitor，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="e802c-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e802c-148">輸出</span><span class="sxs-lookup"><span data-stu-id="e802c-148">OUTPUTS</span></span>

### <span data-ttu-id="e802c-149">PSAddAutoscaleSettingOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e802c-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="e802c-150">筆記</span><span class="sxs-lookup"><span data-stu-id="e802c-150">NOTES</span></span>

## <span data-ttu-id="e802c-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="e802c-151">RELATED LINKS</span></span>

[<span data-ttu-id="e802c-152">AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="e802c-153">新-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e802c-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="e802c-154">新-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="e802c-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="e802c-155">移除-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e802c-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)

