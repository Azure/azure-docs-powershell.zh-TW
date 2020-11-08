---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 993e1b9cde421bad1039f94f4557ee58f781c20b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799926"
---
# <span data-ttu-id="01a0c-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="01a0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="01a0c-103">建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="01a0c-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01a0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="01a0c-104">SYNTAX</span></span>

### <span data-ttu-id="01a0c-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01a0c-105">SetByNameAndResourceGroup</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a0c-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="01a0c-106">SetByResourceId</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01a0c-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="01a0c-107">SetByInputObject</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01a0c-108">說明</span><span class="sxs-lookup"><span data-stu-id="01a0c-108">DESCRIPTION</span></span>
<span data-ttu-id="01a0c-109">**AzureRmActivityLogAlert** Cmdlet 會建立新的或設定現有的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="01a0c-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="01a0c-110">針對標記、條件及動作，您必須事先建立物件，並以逗號分隔的方式將物件作為參數傳遞， (請參閱以下範例) 。</span><span class="sxs-lookup"><span data-stu-id="01a0c-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="01a0c-111">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立/修改資源前，可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="01a0c-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="01a0c-112">**注意** ：這個 Cmdlet 及其相關的 **AzureRmLogAlertRule** 會取代2017年11月) 的已過時的 (。</span><span class="sxs-lookup"><span data-stu-id="01a0c-112">**NOTE** : This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzureRmLogAlertRule**.</span></span>

## <span data-ttu-id="01a0c-113">示例</span><span class="sxs-lookup"><span data-stu-id="01a0c-113">EXAMPLES</span></span>

### <span data-ttu-id="01a0c-114">範例1：建立活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="01a0c-114">Example 1: Create an Activity Log Alert</span></span>
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

<span data-ttu-id="01a0c-115">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="01a0c-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="01a0c-116">最終命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="01a0c-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="01a0c-117">範例2：建立活動記錄通知已停用</span><span class="sxs-lookup"><span data-stu-id="01a0c-117">Example 2: Create an Activity Log Alert disabled</span></span>
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

<span data-ttu-id="01a0c-118">前四個命令會建立葉條件和動作群組。</span><span class="sxs-lookup"><span data-stu-id="01a0c-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="01a0c-119">最後一個命令會使用 [條件] 和 [動作] 群組建立活動記錄提醒，但會建立 [已停用] 通知。</span><span class="sxs-lookup"><span data-stu-id="01a0c-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="01a0c-120">範例3：根據管道或 InputObject 參數中的值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="01a0c-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="01a0c-121">第一個命令與 nop 類似，它會使用與其他命令相同的值來設定通知，以取得警報規則、變更描述並停用，然後使用 InputObject 參數保留這些變更</span><span class="sxs-lookup"><span data-stu-id="01a0c-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="01a0c-122">範例4：使用管道中的 ResourceId 值來設定活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="01a0c-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="01a0c-123">如果有指定的記錄警示規則，這個命令會停用。</span><span class="sxs-lookup"><span data-stu-id="01a0c-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="01a0c-124">參數</span><span class="sxs-lookup"><span data-stu-id="01a0c-124">PARAMETERS</span></span>

### <span data-ttu-id="01a0c-125">-動作</span><span class="sxs-lookup"><span data-stu-id="01a0c-125">-Action</span></span>
<span data-ttu-id="01a0c-126">活動記錄通知的動作群組清單。</span><span class="sxs-lookup"><span data-stu-id="01a0c-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-127">-條件</span><span class="sxs-lookup"><span data-stu-id="01a0c-127">-Condition</span></span>
<span data-ttu-id="01a0c-128">活動記錄通知的條件清單。</span><span class="sxs-lookup"><span data-stu-id="01a0c-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="01a0c-129">**注意** ：在條件清單中，至少必須有一個欄位等於 "Category"。</span><span class="sxs-lookup"><span data-stu-id="01a0c-129">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="01a0c-130">如果此條件不存在，後端會以 400 (BadRequest) 回應。</span><span class="sxs-lookup"><span data-stu-id="01a0c-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01a0c-131">-DefaultProfile</span></span>
<span data-ttu-id="01a0c-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="01a0c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01a0c-133">-描述</span><span class="sxs-lookup"><span data-stu-id="01a0c-133">-Description</span></span>
<span data-ttu-id="01a0c-134">警報資源的描述。</span><span class="sxs-lookup"><span data-stu-id="01a0c-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-135">-DisableAlert</span></span>
<span data-ttu-id="01a0c-136">允許使用者建立停用的活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="01a0c-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="01a0c-137">如果未指定，即會啟用通知。</span><span class="sxs-lookup"><span data-stu-id="01a0c-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01a0c-138">-InputObject</span></span>
<span data-ttu-id="01a0c-139">設定呼叫的 InputObject tags 屬性來解壓縮所需的名稱，以及資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="01a0c-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-140">-位置</span><span class="sxs-lookup"><span data-stu-id="01a0c-140">-Location</span></span>
<span data-ttu-id="01a0c-141">活動記錄通知存在的位置。</span><span class="sxs-lookup"><span data-stu-id="01a0c-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="01a0c-142">-Name</span></span>
<span data-ttu-id="01a0c-143">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="01a0c-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01a0c-144">-ResourceGroupName</span></span>
<span data-ttu-id="01a0c-145">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="01a0c-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01a0c-146">-ResourceId</span></span>
<span data-ttu-id="01a0c-147">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="01a0c-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="01a0c-148">-Scope</span></span>
<span data-ttu-id="01a0c-149">活動記錄通知的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="01a0c-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="01a0c-150">-Tag</span></span>
<span data-ttu-id="01a0c-151">設定活動記錄通知資源的 tags 屬性。</span><span class="sxs-lookup"><span data-stu-id="01a0c-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01a0c-152">-確認</span><span class="sxs-lookup"><span data-stu-id="01a0c-152">-Confirm</span></span>
<span data-ttu-id="01a0c-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01a0c-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01a0c-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01a0c-154">-WhatIf</span></span>
<span data-ttu-id="01a0c-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01a0c-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01a0c-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01a0c-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01a0c-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01a0c-157">CommonParameters</span></span>
<span data-ttu-id="01a0c-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01a0c-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01a0c-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="01a0c-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01a0c-160">輸入</span><span class="sxs-lookup"><span data-stu-id="01a0c-160">INPUTS</span></span>

### <span data-ttu-id="01a0c-161">System.object</span><span class="sxs-lookup"><span data-stu-id="01a0c-161">System.String</span></span>

### <span data-ttu-id="01a0c-162">[System.object]。清單 ' 1 [系統. 字串，字串，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01a0c-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="01a0c-163">[System.object]。清單 ' 1 [5.1.0.0 ActivityLogAlertLeafCondition，，版本 =，Culture = 中性，PublicKeyToken = null]」））））中的集合。</span><span class="sxs-lookup"><span data-stu-id="01a0c-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="01a0c-164">[System.object]。清單 ' 1 [5.1.0.0 ActivityLogAlertActionGroup，，版本 =，Culture = 中性，PublicKeyToken = null]」））））中的集合。</span><span class="sxs-lookup"><span data-stu-id="01a0c-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="01a0c-165">[System.object]。字典 "2 [" System.object = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]，[System. 字串，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="01a0c-165">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="01a0c-166">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="01a0c-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="01a0c-167">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="01a0c-167">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="01a0c-168">輸出</span><span class="sxs-lookup"><span data-stu-id="01a0c-168">OUTPUTS</span></span>

### <span data-ttu-id="01a0c-169">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="01a0c-169">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="01a0c-170">筆記</span><span class="sxs-lookup"><span data-stu-id="01a0c-170">NOTES</span></span>

## <span data-ttu-id="01a0c-171">相關連結</span><span class="sxs-lookup"><span data-stu-id="01a0c-171">RELATED LINKS</span></span>

[<span data-ttu-id="01a0c-172">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-172">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="01a0c-173">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-173">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="01a0c-174">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-174">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="01a0c-175">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="01a0c-175">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="01a0c-176">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="01a0c-176">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="01a0c-177">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="01a0c-177">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)