---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: af115413fd7dfe2821bf6937e33859c8d6e57c0b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406497"
---
# <span data-ttu-id="e0b10-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="e0b10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e0b10-102">SYNOPSIS</span></span>
<span data-ttu-id="e0b10-103">停用活動記錄提醒並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="e0b10-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="e0b10-104">語法</span><span class="sxs-lookup"><span data-stu-id="e0b10-104">SYNTAX</span></span>

### <span data-ttu-id="e0b10-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e0b10-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b10-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0b10-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0b10-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0b10-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e0b10-108">描述</span><span class="sxs-lookup"><span data-stu-id="e0b10-108">DESCRIPTION</span></span>
<span data-ttu-id="e0b10-109">**Disable-AzActivityLogAlert** Cmdlet 會停用和活動記錄提醒，並允許設定其標籤。</span><span class="sxs-lookup"><span data-stu-id="e0b10-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="e0b10-110">此 Cmdlet 實做 ShouldProcess 模式，即實際修補資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="e0b10-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="e0b10-111">例子</span><span class="sxs-lookup"><span data-stu-id="e0b10-111">EXAMPLES</span></span>

### <span data-ttu-id="e0b10-112">範例 1：停用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="e0b10-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="e0b10-113">此命令會停用資源群組 Default-ActivityLogsAlerts 中稱為警示1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="e0b10-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="e0b10-114">此命令會變更稱為警示1 的活動記錄提醒的標記屬性，並停用該屬性。</span><span class="sxs-lookup"><span data-stu-id="e0b10-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="e0b10-115">範例 2：停用使用 PSActivityLogAlertResource 物件做為輸入的活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="e0b10-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="e0b10-116">此命令會停用稱為警示1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="e0b10-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="e0b10-117">為此，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="e0b10-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="e0b10-118">範例 3：使用 ResourceId 參數停用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="e0b10-119">此命令會使用來自管道的 ResourceId 參數停用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="e0b10-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="e0b10-120">參數</span><span class="sxs-lookup"><span data-stu-id="e0b10-120">PARAMETERS</span></span>

### <span data-ttu-id="e0b10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0b10-121">-DefaultProfile</span></span>
<span data-ttu-id="e0b10-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e0b10-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0b10-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0b10-123">-InputObject</span></span>
<span data-ttu-id="e0b10-124">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱、資源組名及選擇性的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="e0b10-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="e0b10-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0b10-125">-Name</span></span>
<span data-ttu-id="e0b10-126">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b10-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="e0b10-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0b10-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0b10-128">警示資源將存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0b10-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="e0b10-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0b10-129">-ResourceId</span></span>
<span data-ttu-id="e0b10-130">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="e0b10-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="e0b10-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e0b10-131">-Confirm</span></span>
<span data-ttu-id="e0b10-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e0b10-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0b10-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0b10-133">-WhatIf</span></span>
<span data-ttu-id="e0b10-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e0b10-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0b10-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e0b10-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0b10-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0b10-136">CommonParameters</span></span>
<span data-ttu-id="e0b10-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e0b10-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0b10-138">詳細資訊[請參閱about_CommonParameters。](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0b10-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0b10-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e0b10-139">INPUTS</span></span>

### <span data-ttu-id="e0b10-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e0b10-140">System.String</span></span>

### <span data-ttu-id="e0b10-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e0b10-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e0b10-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e0b10-142">OUTPUTS</span></span>

### <span data-ttu-id="e0b10-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="e0b10-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="e0b10-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e0b10-144">NOTES</span></span>

## <span data-ttu-id="e0b10-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0b10-145">RELATED LINKS</span></span>

[<span data-ttu-id="e0b10-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="e0b10-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="e0b10-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="e0b10-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="e0b10-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="e0b10-150">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e0b10-150">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
