---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129436"
---
# <span data-ttu-id="c22d5-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="c22d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c22d5-102">SYNOPSIS</span></span>
<span data-ttu-id="c22d5-103">停用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="c22d5-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="c22d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="c22d5-104">SYNTAX</span></span>

### <span data-ttu-id="c22d5-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c22d5-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c22d5-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="c22d5-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c22d5-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="c22d5-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c22d5-108">說明</span><span class="sxs-lookup"><span data-stu-id="c22d5-108">DESCRIPTION</span></span>
<span data-ttu-id="c22d5-109">**Disable AzActivityLogAlert** Cmdlet 會停用和活動記錄通知，並允許您設定其標記。</span><span class="sxs-lookup"><span data-stu-id="c22d5-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="c22d5-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="c22d5-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="c22d5-111">示例</span><span class="sxs-lookup"><span data-stu-id="c22d5-111">EXAMPLES</span></span>

### <span data-ttu-id="c22d5-112">範例1：停用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="c22d5-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="c22d5-113">這個命令會停用資源群組預設-ActivityLogsAlerts 中稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c22d5-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="c22d5-114">這個命令會變更名為 alert1 的活動記錄提醒的 tags 屬性並停用。</span><span class="sxs-lookup"><span data-stu-id="c22d5-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="c22d5-115">範例2：使用 PSActivityLogAlertResource 物件做為輸入來停用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="c22d5-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="c22d5-116">這個命令會停用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="c22d5-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="c22d5-117">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="c22d5-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="c22d5-118">範例3：使用 ResourceId 參數停用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="c22d5-119">這個命令會使用管道中的 ResourceId 參數停用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="c22d5-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="c22d5-120">參數</span><span class="sxs-lookup"><span data-stu-id="c22d5-120">PARAMETERS</span></span>

### <span data-ttu-id="c22d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c22d5-121">-DefaultProfile</span></span>
<span data-ttu-id="c22d5-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c22d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c22d5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c22d5-123">-InputObject</span></span>
<span data-ttu-id="c22d5-124">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標籤屬性。</span><span class="sxs-lookup"><span data-stu-id="c22d5-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c22d5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c22d5-125">-Name</span></span>
<span data-ttu-id="c22d5-126">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22d5-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c22d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="c22d5-128">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c22d5-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22d5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c22d5-129">-ResourceId</span></span>
<span data-ttu-id="c22d5-130">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="c22d5-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c22d5-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c22d5-131">-Confirm</span></span>
<span data-ttu-id="c22d5-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c22d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c22d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c22d5-133">-WhatIf</span></span>
<span data-ttu-id="c22d5-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c22d5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c22d5-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c22d5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c22d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c22d5-136">CommonParameters</span></span>
<span data-ttu-id="c22d5-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c22d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c22d5-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c22d5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c22d5-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c22d5-139">INPUTS</span></span>

### <span data-ttu-id="c22d5-140">System.object</span><span class="sxs-lookup"><span data-stu-id="c22d5-140">System.String</span></span>

### <span data-ttu-id="c22d5-141">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="c22d5-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c22d5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c22d5-142">OUTPUTS</span></span>

### <span data-ttu-id="c22d5-143">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="c22d5-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c22d5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c22d5-144">NOTES</span></span>

## <span data-ttu-id="c22d5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c22d5-145">RELATED LINKS</span></span>

[<span data-ttu-id="c22d5-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c22d5-147">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="c22d5-148">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="c22d5-149">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c22d5-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="c22d5-150">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="c22d5-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="c22d5-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c22d5-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)