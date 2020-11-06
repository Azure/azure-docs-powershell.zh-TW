---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 08e7558bb357c930749cf4a93bfa428560c64395
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456212"
---
# <span data-ttu-id="b87d6-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="b87d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b87d6-102">SYNOPSIS</span></span>
<span data-ttu-id="b87d6-103">建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b87d6-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b87d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="b87d6-104">SYNTAX</span></span>

### <span data-ttu-id="b87d6-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b87d6-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b87d6-107">說明</span><span class="sxs-lookup"><span data-stu-id="b87d6-107">DESCRIPTION</span></span>
<span data-ttu-id="b87d6-108">**AzureRmAutoscaleSetting** Cmdlet 會建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b87d6-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

<span data-ttu-id="b87d6-109">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="b87d6-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="b87d6-110">示例</span><span class="sxs-lookup"><span data-stu-id="b87d6-110">EXAMPLES</span></span>

### <span data-ttu-id="b87d6-111">範例1：建立自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="b87d6-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="b87d6-112">前兩個命令使用 New-AzureRmAutoscaleRule 來建立兩個自動縮放規則，$Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="b87d6-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="b87d6-113">第三個和第四個命令使用 New-AzureRmAutoscaleProfile 來建立自動縮放設定檔，$Profile 1 和 $Profile 2，使用 $Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="b87d6-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="b87d6-114">最終命令會使用 $Profile 1 和 $Profile 2 中的設定檔來建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b87d6-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="b87d6-115">參數</span><span class="sxs-lookup"><span data-stu-id="b87d6-115">PARAMETERS</span></span>

### <span data-ttu-id="b87d6-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b87d6-116">-AutoscaleProfile</span></span>
<span data-ttu-id="b87d6-117">指定要新增到自動縮放設定的配置檔案清單，或 $Null 以新增無設定檔。</span><span class="sxs-lookup"><span data-stu-id="b87d6-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases: AutoscaleProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b87d6-118">-DefaultProfile</span></span>
<span data-ttu-id="b87d6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b87d6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-120">-DisableSetting</span></span>
<span data-ttu-id="b87d6-121">停用現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="b87d6-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-122">-位置</span><span class="sxs-lookup"><span data-stu-id="b87d6-122">-Location</span></span>
<span data-ttu-id="b87d6-123">指定自動縮放設定的位置。</span><span class="sxs-lookup"><span data-stu-id="b87d6-123">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b87d6-124">-Name</span></span>
<span data-ttu-id="b87d6-125">指定要建立的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b87d6-125">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-126">-通知</span><span class="sxs-lookup"><span data-stu-id="b87d6-126">-Notification</span></span>
<span data-ttu-id="b87d6-127">指定以逗號分隔的通知清單。</span><span class="sxs-lookup"><span data-stu-id="b87d6-127">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases: Notifications

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b87d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="b87d6-129">指定與自動縮放設定相關聯之資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b87d6-129">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-130">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="b87d6-130">-SettingSpec</span></span>
<span data-ttu-id="b87d6-131">指定 **AutoscaleSetting** 物件。</span><span class="sxs-lookup"><span data-stu-id="b87d6-131">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="b87d6-132">您可以使用 Get-AzureRmAutoscaleSetting Cmdlet 取得 **AutoscaleSetting** 物件，也可以在 Windows PowerShell 腳本中構造一個物件。</span><span class="sxs-lookup"><span data-stu-id="b87d6-132">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-133">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b87d6-133">-TargetResourceId</span></span>
<span data-ttu-id="b87d6-134">指定要自動縮放的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b87d6-134">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: String
Parameter Sets: CreateAutoscaleSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b87d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b87d6-135">CommonParameters</span></span>
<span data-ttu-id="b87d6-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b87d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b87d6-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b87d6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b87d6-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b87d6-138">INPUTS</span></span>

### <span data-ttu-id="b87d6-139">所有</span><span class="sxs-lookup"><span data-stu-id="b87d6-139">None</span></span>
<span data-ttu-id="b87d6-140">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b87d6-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b87d6-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b87d6-141">OUTPUTS</span></span>

### <span data-ttu-id="b87d6-142">PSAddAutoscaleSettingOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="b87d6-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="b87d6-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b87d6-143">NOTES</span></span>

## <span data-ttu-id="b87d6-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b87d6-144">RELATED LINKS</span></span>

[<span data-ttu-id="b87d6-145">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="b87d6-146">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="b87d6-146">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="b87d6-147">新-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="b87d6-147">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="b87d6-148">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="b87d6-148">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


