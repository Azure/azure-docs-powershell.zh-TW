---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624814"
---
# <span data-ttu-id="5236c-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="5236c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5236c-102">SYNOPSIS</span></span>
<span data-ttu-id="5236c-103">建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="5236c-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5236c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5236c-104">SYNTAX</span></span>

### <span data-ttu-id="5236c-105">設定活動記錄通知的預設參數</span><span class="sxs-lookup"><span data-stu-id="5236c-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5236c-106">用來設定活動記錄通知的參數從管道取得 ResourceId 的值</span><span class="sxs-lookup"><span data-stu-id="5236c-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5236c-107">設定活動記錄通知從管道取得價值的參數</span><span class="sxs-lookup"><span data-stu-id="5236c-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5236c-108">說明</span><span class="sxs-lookup"><span data-stu-id="5236c-108">DESCRIPTION</span></span>
<span data-ttu-id="5236c-109">**AzureRmActivityLogAlert** Cmdlet 會建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="5236c-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="5236c-110">針對標記、條件及動作，您必須事先建立物件，並以逗號分隔的方式將物件作為參數傳遞， (請參閱以下範例) 。</span><span class="sxs-lookup"><span data-stu-id="5236c-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="5236c-111">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立/修改資源前，可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="5236c-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="5236c-112">示例</span><span class="sxs-lookup"><span data-stu-id="5236c-112">EXAMPLES</span></span>

### <span data-ttu-id="5236c-113">範例1：建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5236c-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="5236c-114">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="5236c-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="5236c-115">最終命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="5236c-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="5236c-116">範例2：建立活動記錄通知已停用</span><span class="sxs-lookup"><span data-stu-id="5236c-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="5236c-117">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="5236c-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="5236c-118">最後一個命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒，但會建立 [已停用] 通知。</span><span class="sxs-lookup"><span data-stu-id="5236c-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="5236c-119">範例3：根據管道或 InputObject 參數中的值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5236c-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="5236c-120">第一個命令與 nop 類似，它會使用與其他命令相同的值來設定通知，以取得警報規則、變更描述並停用，然後使用 InputObject 參數保留這些變更</span><span class="sxs-lookup"><span data-stu-id="5236c-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="5236c-121">範例4：使用管道中的 ResourceId 值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5236c-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="5236c-122">如果有指定的記錄警示規則，這個命令會停用。</span><span class="sxs-lookup"><span data-stu-id="5236c-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="5236c-123">參數</span><span class="sxs-lookup"><span data-stu-id="5236c-123">PARAMETERS</span></span>

### <span data-ttu-id="5236c-124">-位置</span><span class="sxs-lookup"><span data-stu-id="5236c-124">-Location</span></span>
<span data-ttu-id="5236c-125">活動記錄通知存在的位置。</span><span class="sxs-lookup"><span data-stu-id="5236c-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5236c-126">-Name</span></span>
<span data-ttu-id="5236c-127">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="5236c-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5236c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5236c-129">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5236c-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-130">-範圍</span><span class="sxs-lookup"><span data-stu-id="5236c-130">-Scope</span></span>
<span data-ttu-id="5236c-131">活動記錄通知的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="5236c-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-132">-條件</span><span class="sxs-lookup"><span data-stu-id="5236c-132">-Condition</span></span>
<span data-ttu-id="5236c-133">活動記錄通知的條件清單。</span><span class="sxs-lookup"><span data-stu-id="5236c-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="5236c-134">**注意** ：在條件清單中，至少必須有一個欄位等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="5236c-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="5236c-135">如果此條件不存在，後端會以 400 (BadRequest) 回應。</span><span class="sxs-lookup"><span data-stu-id="5236c-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-136">-動作</span><span class="sxs-lookup"><span data-stu-id="5236c-136">-Action</span></span>
<span data-ttu-id="5236c-137">活動記錄通知的動作群組清單。</span><span class="sxs-lookup"><span data-stu-id="5236c-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-138">-DisableAlert</span></span>
<span data-ttu-id="5236c-139">允許使用者建立停用的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="5236c-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="5236c-140">如果未指定，即會啟用通知。</span><span class="sxs-lookup"><span data-stu-id="5236c-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-141">-描述</span><span class="sxs-lookup"><span data-stu-id="5236c-141">-Description</span></span>
<span data-ttu-id="5236c-142">警報資源的描述。</span><span class="sxs-lookup"><span data-stu-id="5236c-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="5236c-143">-Tag</span></span>
<span data-ttu-id="5236c-144">設定活動記錄通知資源的 tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="5236c-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5236c-145">-InputObject</span></span>
<span data-ttu-id="5236c-146">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="5236c-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5236c-147">-ResourceId</span></span>
<span data-ttu-id="5236c-148">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="5236c-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5236c-149">-確認</span><span class="sxs-lookup"><span data-stu-id="5236c-149">-Confirm</span></span>
<span data-ttu-id="5236c-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5236c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5236c-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5236c-151">-DefaultProfile</span></span>
<span data-ttu-id="5236c-152">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5236c-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5236c-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5236c-153">-WhatIf</span></span>
<span data-ttu-id="5236c-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5236c-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5236c-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5236c-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5236c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5236c-156">CommonParameters</span></span>
<span data-ttu-id="5236c-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5236c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5236c-158">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5236c-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5236c-159">輸入</span><span class="sxs-lookup"><span data-stu-id="5236c-159">INPUTS</span></span>

## <span data-ttu-id="5236c-160">輸出</span><span class="sxs-lookup"><span data-stu-id="5236c-160">OUTPUTS</span></span>

### <span data-ttu-id="5236c-161">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="5236c-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5236c-162">筆記</span><span class="sxs-lookup"><span data-stu-id="5236c-162">NOTES</span></span>

## <span data-ttu-id="5236c-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="5236c-163">RELATED LINKS</span></span>

[<span data-ttu-id="5236c-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5236c-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5236c-166">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5236c-167">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5236c-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="5236c-168">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="5236c-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="5236c-169">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5236c-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
