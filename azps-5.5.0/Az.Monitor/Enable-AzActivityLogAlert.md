---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135130"
---
# <span data-ttu-id="5b789-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="5b789-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5b789-102">SYNOPSIS</span></span>
<span data-ttu-id="5b789-103">啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="5b789-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="5b789-104">句法</span><span class="sxs-lookup"><span data-stu-id="5b789-104">SYNTAX</span></span>

### <span data-ttu-id="5b789-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5b789-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b789-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b789-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b789-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b789-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5b789-108">說明</span><span class="sxs-lookup"><span data-stu-id="5b789-108">DESCRIPTION</span></span>
<span data-ttu-id="5b789-109">**Enable-AzActivityLogAlert** Cmdlet 可啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="5b789-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="5b789-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b789-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="5b789-111">示例</span><span class="sxs-lookup"><span data-stu-id="5b789-111">EXAMPLES</span></span>

### <span data-ttu-id="5b789-112">範例1：啟用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="5b789-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="5b789-113">這個命令會在資源群組預設-ActivityLogsAlerts 中啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="5b789-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="5b789-114">範例2：使用 PSActivityLogAlertResource 物件做為輸入來啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="5b789-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="5b789-115">這個命令會啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="5b789-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="5b789-116">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="5b789-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="5b789-117">範例3：使用 ResourceId 參數啟用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="5b789-118">這個命令會從管道使用 ResourceId 參數來啟用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="5b789-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5b789-119">參數</span><span class="sxs-lookup"><span data-stu-id="5b789-119">PARAMETERS</span></span>

### <span data-ttu-id="5b789-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b789-120">-DefaultProfile</span></span>
<span data-ttu-id="5b789-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5b789-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b789-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b789-122">-InputObject</span></span>
<span data-ttu-id="5b789-123">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="5b789-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b789-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5b789-124">-Name</span></span>
<span data-ttu-id="5b789-125">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b789-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b789-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b789-126">-ResourceGroupName</span></span>
<span data-ttu-id="5b789-127">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5b789-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b789-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b789-128">-ResourceId</span></span>
<span data-ttu-id="5b789-129">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="5b789-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b789-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5b789-130">-Confirm</span></span>
<span data-ttu-id="5b789-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5b789-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b789-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b789-132">-WhatIf</span></span>
<span data-ttu-id="5b789-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5b789-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b789-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5b789-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b789-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b789-135">CommonParameters</span></span>
<span data-ttu-id="5b789-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5b789-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b789-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5b789-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b789-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5b789-138">INPUTS</span></span>

### <span data-ttu-id="5b789-139">System.object</span><span class="sxs-lookup"><span data-stu-id="5b789-139">System.String</span></span>

### <span data-ttu-id="5b789-140">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="5b789-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5b789-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5b789-141">OUTPUTS</span></span>

### <span data-ttu-id="5b789-142">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="5b789-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5b789-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5b789-143">NOTES</span></span>

## <span data-ttu-id="5b789-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5b789-144">RELATED LINKS</span></span>

[<span data-ttu-id="5b789-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="5b789-146">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="5b789-147">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="5b789-148">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="5b789-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="5b789-149">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5b789-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="5b789-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5b789-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
