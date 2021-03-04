---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 0f8e532e1bda9555c12cdf0770a5c2c986e8eac7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908981"
---
# <span data-ttu-id="71e6a-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="71e6a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="71e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="71e6a-103">停用活動記錄提醒並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="71e6a-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="71e6a-104">語法</span><span class="sxs-lookup"><span data-stu-id="71e6a-104">SYNTAX</span></span>

### <span data-ttu-id="71e6a-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="71e6a-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e6a-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="71e6a-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71e6a-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="71e6a-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71e6a-108">描述</span><span class="sxs-lookup"><span data-stu-id="71e6a-108">DESCRIPTION</span></span>
<span data-ttu-id="71e6a-109">**Disable-AzActivityLogAlert** Cmdlet 會停用和活動記錄提醒，並允許設定其標籤。</span><span class="sxs-lookup"><span data-stu-id="71e6a-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="71e6a-110">此 Cmdlet 實做 ShouldProcess 模式，即實際修補資源之前，可能會要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="71e6a-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="71e6a-111">例子</span><span class="sxs-lookup"><span data-stu-id="71e6a-111">EXAMPLES</span></span>

### <span data-ttu-id="71e6a-112">範例 1：停用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="71e6a-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="71e6a-113">此命令會停用資源群組 Default-ActivityLogsAlerts 中稱為警示1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="71e6a-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="71e6a-114">此命令會變更稱為警示1 的活動記錄提醒的標記屬性，並停用該屬性。</span><span class="sxs-lookup"><span data-stu-id="71e6a-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="71e6a-115">範例 2：停用使用 PSActivityLogAlertResource 物件做為輸入的活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="71e6a-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="71e6a-116">此命令會停用稱為警示1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="71e6a-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="71e6a-117">為此，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="71e6a-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="71e6a-118">範例 3：使用 ResourceId 參數停用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="71e6a-119">此命令會使用來自管道的 ResourceId 參數停用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="71e6a-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="71e6a-120">參數</span><span class="sxs-lookup"><span data-stu-id="71e6a-120">PARAMETERS</span></span>

### <span data-ttu-id="71e6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71e6a-121">-DefaultProfile</span></span>
<span data-ttu-id="71e6a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="71e6a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71e6a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71e6a-123">-InputObject</span></span>
<span data-ttu-id="71e6a-124">設定呼叫的 InputObject 標記屬性，以解壓縮必要的名稱、資源組名及選擇性的標記屬性。</span><span class="sxs-lookup"><span data-stu-id="71e6a-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="71e6a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="71e6a-125">-Name</span></span>
<span data-ttu-id="71e6a-126">活動記錄提醒的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e6a-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="71e6a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71e6a-127">-ResourceGroupName</span></span>
<span data-ttu-id="71e6a-128">警示資源將存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71e6a-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="71e6a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71e6a-129">-ResourceId</span></span>
<span data-ttu-id="71e6a-130">設定呼叫的 ResourceId 標記屬性，以解壓縮必要的名稱、資源組名屬性。</span><span class="sxs-lookup"><span data-stu-id="71e6a-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="71e6a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="71e6a-131">-Confirm</span></span>
<span data-ttu-id="71e6a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="71e6a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71e6a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71e6a-133">-WhatIf</span></span>
<span data-ttu-id="71e6a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71e6a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71e6a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71e6a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71e6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71e6a-136">CommonParameters</span></span>
<span data-ttu-id="71e6a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="71e6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71e6a-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71e6a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71e6a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="71e6a-139">INPUTS</span></span>

### <span data-ttu-id="71e6a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="71e6a-140">System.String</span></span>

### <span data-ttu-id="71e6a-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="71e6a-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="71e6a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="71e6a-142">OUTPUTS</span></span>

### <span data-ttu-id="71e6a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="71e6a-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="71e6a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="71e6a-144">NOTES</span></span>

## <span data-ttu-id="71e6a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="71e6a-145">RELATED LINKS</span></span>

[<span data-ttu-id="71e6a-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="71e6a-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="71e6a-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="71e6a-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="71e6a-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="71e6a-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="71e6a-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="71e6a-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="71e6a-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
