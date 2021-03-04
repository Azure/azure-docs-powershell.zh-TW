---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: 4303e824d218082bfc85391ac834e2764a485fcb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915765"
---
# <span data-ttu-id="28f5f-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="28f5f-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="28f5f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="28f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="28f5f-103">在裝置上設定觸發。</span><span class="sxs-lookup"><span data-stu-id="28f5f-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="28f5f-104">語法</span><span class="sxs-lookup"><span data-stu-id="28f5f-104">SYNTAX</span></span>

### <span data-ttu-id="28f5f-105">FileEventTriventParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="28f5f-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28f5f-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f5f-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28f5f-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f5f-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28f5f-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f5f-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28f5f-109">描述</span><span class="sxs-lookup"><span data-stu-id="28f5f-109">DESCRIPTION</span></span>
<span data-ttu-id="28f5f-110">**New-AzStackEdgeTrigger Cmdlet** 會設定 Stack Edge 裝置上的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="28f5f-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="28f5f-111">例子</span><span class="sxs-lookup"><span data-stu-id="28f5f-111">EXAMPLES</span></span>

### <span data-ttu-id="28f5f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="28f5f-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="28f5f-113">參數</span><span class="sxs-lookup"><span data-stu-id="28f5f-113">PARAMETERS</span></span>

### <span data-ttu-id="28f5f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28f5f-114">-AsJob</span></span>
<span data-ttu-id="28f5f-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="28f5f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f5f-116">-DefaultProfile</span></span>
<span data-ttu-id="28f5f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="28f5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28f5f-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="28f5f-118">-DeviceName</span></span>
<span data-ttu-id="28f5f-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="28f5f-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="28f5f-120">-FileEvent</span></span>
<span data-ttu-id="28f5f-121">傳遞此參數以設定 FileEvent Trigger</span><span class="sxs-lookup"><span data-stu-id="28f5f-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="28f5f-122">-Name</span></span>
<span data-ttu-id="28f5f-123">資源名稱</span><span class="sxs-lookup"><span data-stu-id="28f5f-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="28f5f-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="28f5f-125">傳遞此參數以設定 PeriodicTimerEvent Trigger</span><span class="sxs-lookup"><span data-stu-id="28f5f-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28f5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="28f5f-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="28f5f-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="28f5f-128">-RoleName</span></span>
<span data-ttu-id="28f5f-129">要根據該角色計算事件。</span><span class="sxs-lookup"><span data-stu-id="28f5f-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-130">-排程</span><span class="sxs-lookup"><span data-stu-id="28f5f-130">-Schedule</span></span>
<span data-ttu-id="28f5f-131">需要提高計時器事件的定期頻率。</span><span class="sxs-lookup"><span data-stu-id="28f5f-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="28f5f-132">指定排程 (介於 1 到 365) 、小時 (介於 1 到 23) ，或分鐘 (介於 1 到 59) 。</span><span class="sxs-lookup"><span data-stu-id="28f5f-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="28f5f-133">-ShareId</span></span>
<span data-ttu-id="28f5f-134">FileEvent Trigger 中要傳遞的檔案共用識別碼</span><span class="sxs-lookup"><span data-stu-id="28f5f-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="28f5f-135">-ShareName</span></span>
<span data-ttu-id="28f5f-136">FileEvent Trigger 中要傳遞的檔案共用識別碼</span><span class="sxs-lookup"><span data-stu-id="28f5f-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="28f5f-137">-StartTime</span></span>
<span data-ttu-id="28f5f-138">產生有效觸發的一天中時間。</span><span class="sxs-lookup"><span data-stu-id="28f5f-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="28f5f-139">排程是參照指定最多秒的時間來計算。</span><span class="sxs-lookup"><span data-stu-id="28f5f-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="28f5f-140">如果未指定時區，則時間會視為位於裝置時區。</span><span class="sxs-lookup"><span data-stu-id="28f5f-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="28f5f-141">值一定會以 UTC 時間退回。</span><span class="sxs-lookup"><span data-stu-id="28f5f-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-142">-主題</span><span class="sxs-lookup"><span data-stu-id="28f5f-142">-Topic</span></span>
<span data-ttu-id="28f5f-143">定期事件發佈至 IoT 裝置的主題。</span><span class="sxs-lookup"><span data-stu-id="28f5f-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f5f-144">-確認</span><span class="sxs-lookup"><span data-stu-id="28f5f-144">-Confirm</span></span>
<span data-ttu-id="28f5f-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="28f5f-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f5f-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f5f-146">-WhatIf</span></span>
<span data-ttu-id="28f5f-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="28f5f-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28f5f-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28f5f-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f5f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f5f-149">CommonParameters</span></span>
<span data-ttu-id="28f5f-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="28f5f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f5f-151">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28f5f-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f5f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="28f5f-152">INPUTS</span></span>

### <span data-ttu-id="28f5f-153">沒有</span><span class="sxs-lookup"><span data-stu-id="28f5f-153">None</span></span>

## <span data-ttu-id="28f5f-154">輸出</span><span class="sxs-lookup"><span data-stu-id="28f5f-154">OUTPUTS</span></span>

### <span data-ttu-id="28f5f-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.models.PSStackEdgeTrirr</span><span class="sxs-lookup"><span data-stu-id="28f5f-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="28f5f-156">筆記</span><span class="sxs-lookup"><span data-stu-id="28f5f-156">NOTES</span></span>

## <span data-ttu-id="28f5f-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="28f5f-157">RELATED LINKS</span></span>
