---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: e2b09005714021bc8b428b93214f30a16a279ce8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794638"
---
# <span data-ttu-id="98ee8-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="98ee8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98ee8-102">SYNOPSIS</span></span>
<span data-ttu-id="98ee8-103">啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="98ee8-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="98ee8-104">句法</span><span class="sxs-lookup"><span data-stu-id="98ee8-104">SYNTAX</span></span>

### <span data-ttu-id="98ee8-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="98ee8-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ee8-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="98ee8-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98ee8-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="98ee8-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98ee8-108">說明</span><span class="sxs-lookup"><span data-stu-id="98ee8-108">DESCRIPTION</span></span>
<span data-ttu-id="98ee8-109">**Enable-AzActivityLogAlert** Cmdlet 可啟用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="98ee8-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="98ee8-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="98ee8-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="98ee8-111">示例</span><span class="sxs-lookup"><span data-stu-id="98ee8-111">EXAMPLES</span></span>

### <span data-ttu-id="98ee8-112">範例1：啟用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="98ee8-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="98ee8-113">這個命令會在資源群組預設-ActivityLogsAlerts 中啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="98ee8-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="98ee8-114">範例2：使用 PSActivityLogAlertResource 物件做為輸入來啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="98ee8-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="98ee8-115">這個命令會啟用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="98ee8-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="98ee8-116">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="98ee8-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="98ee8-117">範例3：使用 ResourceId 參數啟用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="98ee8-118">這個命令會從管道使用 ResourceId 參數來啟用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="98ee8-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="98ee8-119">參數</span><span class="sxs-lookup"><span data-stu-id="98ee8-119">PARAMETERS</span></span>

### <span data-ttu-id="98ee8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ee8-120">-DefaultProfile</span></span>
<span data-ttu-id="98ee8-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="98ee8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98ee8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98ee8-122">-InputObject</span></span>
<span data-ttu-id="98ee8-123">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="98ee8-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="98ee8-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="98ee8-124">-Name</span></span>
<span data-ttu-id="98ee8-125">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="98ee8-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="98ee8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98ee8-126">-ResourceGroupName</span></span>
<span data-ttu-id="98ee8-127">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="98ee8-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="98ee8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98ee8-128">-ResourceId</span></span>
<span data-ttu-id="98ee8-129">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="98ee8-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="98ee8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="98ee8-130">-Confirm</span></span>
<span data-ttu-id="98ee8-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="98ee8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ee8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ee8-132">-WhatIf</span></span>
<span data-ttu-id="98ee8-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="98ee8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98ee8-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="98ee8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ee8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ee8-135">CommonParameters</span></span>
<span data-ttu-id="98ee8-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98ee8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ee8-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98ee8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ee8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="98ee8-138">INPUTS</span></span>

### <span data-ttu-id="98ee8-139">System.object</span><span class="sxs-lookup"><span data-stu-id="98ee8-139">System.String</span></span>

### <span data-ttu-id="98ee8-140">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="98ee8-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="98ee8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="98ee8-141">OUTPUTS</span></span>

### <span data-ttu-id="98ee8-142">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="98ee8-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="98ee8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="98ee8-143">NOTES</span></span>

## <span data-ttu-id="98ee8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="98ee8-144">RELATED LINKS</span></span>

[<span data-ttu-id="98ee8-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="98ee8-146">AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="98ee8-147">移除-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="98ee8-148">新-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="98ee8-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="98ee8-149">新-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="98ee8-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="98ee8-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98ee8-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)