---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: ee249d7379198a28cad22bf78a6c9ac1bf48f920
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626279"
---
# <span data-ttu-id="68029-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68029-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="68029-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68029-102">SYNOPSIS</span></span>
<span data-ttu-id="68029-103">建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="68029-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68029-104">句法</span><span class="sxs-lookup"><span data-stu-id="68029-104">SYNTAX</span></span>

### <span data-ttu-id="68029-105">更新語義中 Add-AzureRmAutoscaleSetting Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="68029-105">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics</span></span>
```
Add-AzureRmAutoscaleSetting -SettingSpec <PSAutoscaleSetting> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="68029-106">建立語義中 Add-AzureRmAutoscaleSetting Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="68029-106">Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroup <String> [-DisableSetting]
 [-AutoscaleProfiles <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notifications <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68029-107">說明</span><span class="sxs-lookup"><span data-stu-id="68029-107">DESCRIPTION</span></span>
<span data-ttu-id="68029-108">**AzureRmAutoscaleSetting** Cmdlet 會建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="68029-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>

## <span data-ttu-id="68029-109">示例</span><span class="sxs-lookup"><span data-stu-id="68029-109">EXAMPLES</span></span>

### <span data-ttu-id="68029-110">範例1：建立自動縮放設定</span><span class="sxs-lookup"><span data-stu-id="68029-110">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroup "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="68029-111">前兩個命令使用 New-AzureRmAutoscaleRule 來建立兩個自動縮放規則，$Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="68029-111">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>

<span data-ttu-id="68029-112">第三個和第四個命令使用 New-AzureRmAutoscaleProfile 來建立自動縮放設定檔，$Profile 1 和 $Profile 2，使用 $Rule 1 和 $Rule 2。</span><span class="sxs-lookup"><span data-stu-id="68029-112">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>

<span data-ttu-id="68029-113">最終命令會使用 $Profile 1 和 $Profile 2 中的設定檔來建立自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="68029-113">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="68029-114">參數</span><span class="sxs-lookup"><span data-stu-id="68029-114">PARAMETERS</span></span>

### <span data-ttu-id="68029-115">-AutoscaleProfiles</span><span class="sxs-lookup"><span data-stu-id="68029-115">-AutoscaleProfiles</span></span>
<span data-ttu-id="68029-116">指定要新增到自動縮放設定的配置檔案清單，或 $Null 以新增無設定檔。</span><span class="sxs-lookup"><span data-stu-id="68029-116">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="68029-117">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="68029-117">-DisableSetting</span></span>
<span data-ttu-id="68029-118">停用現有自動縮放設定。</span><span class="sxs-lookup"><span data-stu-id="68029-118">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="68029-119">-位置</span><span class="sxs-lookup"><span data-stu-id="68029-119">-Location</span></span>
<span data-ttu-id="68029-120">指定自動縮放設定的位置。</span><span class="sxs-lookup"><span data-stu-id="68029-120">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68029-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="68029-121">-Name</span></span>
<span data-ttu-id="68029-122">指定要建立的自動縮放設定的名稱。</span><span class="sxs-lookup"><span data-stu-id="68029-122">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68029-123">-通知</span><span class="sxs-lookup"><span data-stu-id="68029-123">-Notifications</span></span>
<span data-ttu-id="68029-124">指定以逗號分隔的通知清單。</span><span class="sxs-lookup"><span data-stu-id="68029-124">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="68029-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="68029-125">-ResourceGroup</span></span>
<span data-ttu-id="68029-126">指定與自動縮放設定相關聯之資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68029-126">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68029-127">-SettingSpec</span><span class="sxs-lookup"><span data-stu-id="68029-127">-SettingSpec</span></span>
<span data-ttu-id="68029-128">指定 **AutoscaleSetting** 物件。</span><span class="sxs-lookup"><span data-stu-id="68029-128">Specifies an **AutoscaleSetting** object.</span></span>
<span data-ttu-id="68029-129">您可以使用 Get-AzureRmAutoscaleSetting Cmdlet 取得 **AutoscaleSetting** 物件，也可以在 Windows PowerShell 腳本中構造一個物件。</span><span class="sxs-lookup"><span data-stu-id="68029-129">You can use the Get-AzureRmAutoscaleSetting cmdlet to get an **AutoscaleSetting** object or you can construct one in a Windows PowerShell script.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the update semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68029-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="68029-130">-TargetResourceId</span></span>
<span data-ttu-id="68029-131">指定要自動縮放的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68029-131">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Add-AzureRmAutoscaleSetting cmdlet in the create semantics
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68029-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68029-132">-DefaultProfile</span></span>
<span data-ttu-id="68029-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68029-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68029-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68029-134">CommonParameters</span></span>
<span data-ttu-id="68029-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68029-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68029-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68029-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68029-137">輸入</span><span class="sxs-lookup"><span data-stu-id="68029-137">INPUTS</span></span>

## <span data-ttu-id="68029-138">輸出</span><span class="sxs-lookup"><span data-stu-id="68029-138">OUTPUTS</span></span>

### <span data-ttu-id="68029-139">PSAddAutoscaleSettingOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="68029-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="68029-140">筆記</span><span class="sxs-lookup"><span data-stu-id="68029-140">NOTES</span></span>

## <span data-ttu-id="68029-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="68029-141">RELATED LINKS</span></span>

[<span data-ttu-id="68029-142">AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68029-142">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="68029-143">新-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="68029-143">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="68029-144">新-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="68029-144">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="68029-145">移除-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="68029-145">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


