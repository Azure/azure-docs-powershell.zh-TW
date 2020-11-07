---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: dd84c2b12af850cc38770243df74a6bd25c205f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800501"
---
# <span data-ttu-id="ba682-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="ba682-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba682-102">SYNOPSIS</span></span>
<span data-ttu-id="ba682-103">停用活動記錄通知並設定其標記。</span><span class="sxs-lookup"><span data-stu-id="ba682-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba682-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba682-104">SYNTAX</span></span>

### <span data-ttu-id="ba682-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ba682-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba682-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="ba682-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba682-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba682-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba682-108">說明</span><span class="sxs-lookup"><span data-stu-id="ba682-108">DESCRIPTION</span></span>
<span data-ttu-id="ba682-109">**Disable AzureRmActivityLogAlert** Cmdlet 會停用和活動記錄通知，並允許您設定其標記。</span><span class="sxs-lookup"><span data-stu-id="ba682-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="ba682-110">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際修補資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba682-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="ba682-111">示例</span><span class="sxs-lookup"><span data-stu-id="ba682-111">EXAMPLES</span></span>

### <span data-ttu-id="ba682-112">範例1：停用活動記錄通知</span><span class="sxs-lookup"><span data-stu-id="ba682-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="ba682-113">這個命令會停用資源群組預設-ActivityLogsAlerts 中稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="ba682-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="ba682-114">這個命令會變更名為 alert1 的活動記錄提醒的 tags 屬性並停用。</span><span class="sxs-lookup"><span data-stu-id="ba682-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="ba682-115">範例2：使用 PSActivityLogAlertResource 物件做為輸入來停用活動記錄提醒</span><span class="sxs-lookup"><span data-stu-id="ba682-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="ba682-116">這個命令會停用稱為 alert1 的活動記錄提醒。</span><span class="sxs-lookup"><span data-stu-id="ba682-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="ba682-117">針對這種情況，它會使用 PSActivityLogAlertResource 物件做為輸入引數。</span><span class="sxs-lookup"><span data-stu-id="ba682-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="ba682-118">範例3：使用 ResourceId 參數停用 ActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="ba682-119">這個命令會使用管道中的 ResourceId 參數停用 ActivityLogAlert。</span><span class="sxs-lookup"><span data-stu-id="ba682-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="ba682-120">參數</span><span class="sxs-lookup"><span data-stu-id="ba682-120">PARAMETERS</span></span>

### <span data-ttu-id="ba682-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba682-121">-DefaultProfile</span></span>
<span data-ttu-id="ba682-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ba682-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba682-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba682-123">-InputObject</span></span>
<span data-ttu-id="ba682-124">設定通話的 InputObject tags 屬性來解壓縮所需的名稱、資源組名稱，以及選用的標籤屬性。</span><span class="sxs-lookup"><span data-stu-id="ba682-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="ba682-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba682-125">-Name</span></span>
<span data-ttu-id="ba682-126">活動記錄通知的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba682-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="ba682-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba682-127">-ResourceGroupName</span></span>
<span data-ttu-id="ba682-128">要在其中存在預警資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ba682-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="ba682-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba682-129">-ResourceId</span></span>
<span data-ttu-id="ba682-130">設定呼叫的 ResourceId 標籤屬性來解壓縮所需的名稱、資源組名稱屬性。</span><span class="sxs-lookup"><span data-stu-id="ba682-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="ba682-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ba682-131">-Confirm</span></span>
<span data-ttu-id="ba682-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba682-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba682-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba682-133">-WhatIf</span></span>
<span data-ttu-id="ba682-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba682-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba682-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba682-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba682-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba682-136">CommonParameters</span></span>
<span data-ttu-id="ba682-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba682-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba682-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba682-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba682-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ba682-139">INPUTS</span></span>

### <span data-ttu-id="ba682-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ba682-140">System.String</span></span>

### <span data-ttu-id="ba682-141">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="ba682-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="ba682-142">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="ba682-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="ba682-143">輸出</span><span class="sxs-lookup"><span data-stu-id="ba682-143">OUTPUTS</span></span>

### <span data-ttu-id="ba682-144">PSActivityLogAlertResource 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="ba682-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="ba682-145">筆記</span><span class="sxs-lookup"><span data-stu-id="ba682-145">NOTES</span></span>

## <span data-ttu-id="ba682-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba682-146">RELATED LINKS</span></span>

[<span data-ttu-id="ba682-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba682-148">AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba682-149">移除-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="ba682-150">新-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="ba682-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="ba682-151">新-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="ba682-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="ba682-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ba682-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
