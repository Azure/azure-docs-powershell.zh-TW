---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: f1af25ca59b6af6a9712019d541e68c269609242
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409183"
---
# <span data-ttu-id="06d9a-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="06d9a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="06d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="06d9a-103">啟用活動記錄提醒並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="06d9a-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="06d9a-104">語法</span><span class="sxs-lookup"><span data-stu-id="06d9a-104">SYNTAX</span></span>

### <span data-ttu-id="06d9a-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="06d9a-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d9a-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="06d9a-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06d9a-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="06d9a-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06d9a-108">描述</span><span class="sxs-lookup"><span data-stu-id="06d9a-108">DESCRIPTION</span></span>
<span data-ttu-id="06d9a-109">**Enable-AzActivityLogAlert** Cmdlet 允許啟用活動記錄提醒並設定其標籤。</span><span class="sxs-lookup"><span data-stu-id="06d9a-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="06d9a-110">此 Cmdlet 實做 ShouldProcess 模式，即實際修補資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="06d9a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="06d9a-111">例子</span><span class="sxs-lookup"><span data-stu-id="06d9a-111">EXAMPLES</span></span>

### <span data-ttu-id="06d9a-112">範例 1：啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="06d9a-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="06d9a-113">此命令會啟用資源群組 Default-ActivityLogsAlerts 中稱為通知1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="06d9a-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="06d9a-114">範例 2：使用 PSActivityLogAlertResource 物件做為輸入來啟用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="06d9a-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="06d9a-115">此命令會啟用稱為警示1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="06d9a-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="06d9a-116">為此，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="06d9a-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="06d9a-117">範例 3：使用 ResourceId 參數啟用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="06d9a-118">此命令會使用來自管道的 ResourceId 參數啟用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="06d9a-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="06d9a-119">參數</span><span class="sxs-lookup"><span data-stu-id="06d9a-119">PARAMETERS</span></span>

### <span data-ttu-id="06d9a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d9a-120">-DefaultProfile</span></span>
<span data-ttu-id="06d9a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="06d9a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06d9a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06d9a-122">-InputObject</span></span>
<span data-ttu-id="06d9a-123">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱、資源組名，以及選擇性的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="06d9a-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="06d9a-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="06d9a-124">-Name</span></span>
<span data-ttu-id="06d9a-125">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d9a-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="06d9a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06d9a-126">-ResourceGroupName</span></span>
<span data-ttu-id="06d9a-127">警示資源將存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="06d9a-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="06d9a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06d9a-128">-ResourceId</span></span>
<span data-ttu-id="06d9a-129">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="06d9a-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="06d9a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="06d9a-130">-Confirm</span></span>
<span data-ttu-id="06d9a-131">執行 Cmdlet 之前，系統會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="06d9a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06d9a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06d9a-132">-WhatIf</span></span>
<span data-ttu-id="06d9a-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="06d9a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06d9a-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="06d9a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06d9a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d9a-135">CommonParameters</span></span>
<span data-ttu-id="06d9a-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="06d9a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d9a-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06d9a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d9a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="06d9a-138">INPUTS</span></span>

### <span data-ttu-id="06d9a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="06d9a-139">System.String</span></span>

### <span data-ttu-id="06d9a-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="06d9a-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="06d9a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="06d9a-141">OUTPUTS</span></span>

### <span data-ttu-id="06d9a-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="06d9a-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="06d9a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="06d9a-143">NOTES</span></span>

## <span data-ttu-id="06d9a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="06d9a-144">RELATED LINKS</span></span>

[<span data-ttu-id="06d9a-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="06d9a-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="06d9a-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="06d9a-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="06d9a-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="06d9a-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="06d9a-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
