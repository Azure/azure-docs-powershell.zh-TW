---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 52c694010673d11c269f94a05474e9399e87c962
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913341"
---
# <span data-ttu-id="9ddde-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="9ddde-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="9ddde-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9ddde-102">SYNOPSIS</span></span>
<span data-ttu-id="9ddde-103">在儲存庫中獲得 Azure 網站修復事件的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="9ddde-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="9ddde-104">語法</span><span class="sxs-lookup"><span data-stu-id="9ddde-104">SYNTAX</span></span>

### <span data-ttu-id="9ddde-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="9ddde-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ddde-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ddde-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ddde-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="9ddde-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ddde-108">ByName</span><span class="sxs-lookup"><span data-stu-id="9ddde-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ddde-109">描述</span><span class="sxs-lookup"><span data-stu-id="9ddde-109">DESCRIPTION</span></span>
<span data-ttu-id="9ddde-110">**Get-AzRecoveryServicesAsrEvent** 會依據指定的選取篩選，取得資料庫中的事件清單。</span><span class="sxs-lookup"><span data-stu-id="9ddde-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="9ddde-111">例子</span><span class="sxs-lookup"><span data-stu-id="9ddde-111">EXAMPLES</span></span>

### <span data-ttu-id="9ddde-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="9ddde-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="9ddde-113">所有事件的清單。</span><span class="sxs-lookup"><span data-stu-id="9ddde-113">List of all events.</span></span>

### <span data-ttu-id="9ddde-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="9ddde-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="9ddde-115">按名稱取得事件。</span><span class="sxs-lookup"><span data-stu-id="9ddde-115">Get event by name.</span></span>

### <span data-ttu-id="9ddde-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="9ddde-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="9ddde-117">受影響物件的事件清單。</span><span class="sxs-lookup"><span data-stu-id="9ddde-117">List of event for affected Object.</span></span>

### <span data-ttu-id="9ddde-118">範例 4</span><span class="sxs-lookup"><span data-stu-id="9ddde-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="9ddde-119">時間開始時間和結束時間之間的事件清單、嚴重性臨界值及健康情況類型 VmHealth。</span><span class="sxs-lookup"><span data-stu-id="9ddde-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="9ddde-120">參數</span><span class="sxs-lookup"><span data-stu-id="9ddde-120">PARAMETERS</span></span>

### <span data-ttu-id="9ddde-121">-AffectedObject有一個名稱</span><span class="sxs-lookup"><span data-stu-id="9ddde-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="9ddde-122">指定搜尋的 AffectedObject FriendlyName。</span><span class="sxs-lookup"><span data-stu-id="9ddde-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ddde-123">-DefaultProfile</span></span>
<span data-ttu-id="9ddde-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ddde-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ddde-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="9ddde-125">-EndTime</span></span>
<span data-ttu-id="9ddde-126">指定搜尋視窗的結束時間。</span><span class="sxs-lookup"><span data-stu-id="9ddde-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="9ddde-127">使用此參數僅取得指定時間之前發生的事件。</span><span class="sxs-lookup"><span data-stu-id="9ddde-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="9ddde-128">-EventType</span></span>
<span data-ttu-id="9ddde-129">根據事件種類篩選事件。</span><span class="sxs-lookup"><span data-stu-id="9ddde-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-130">-布料</span><span class="sxs-lookup"><span data-stu-id="9ddde-130">-Fabric</span></span>
<span data-ttu-id="9ddde-131">根據指定的結構篩選事件。</span><span class="sxs-lookup"><span data-stu-id="9ddde-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="9ddde-132">-FabricId</span></span>
<span data-ttu-id="9ddde-133">指定要篩選的交換矩陣Id。</span><span class="sxs-lookup"><span data-stu-id="9ddde-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ddde-134">-Name</span></span>
<span data-ttu-id="9ddde-135">指定要搜尋的事件名稱。</span><span class="sxs-lookup"><span data-stu-id="9ddde-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ddde-136">-ResourceId</span></span>
<span data-ttu-id="9ddde-137">指定事件的事件 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="9ddde-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-138">-嚴重性</span><span class="sxs-lookup"><span data-stu-id="9ddde-138">-Severity</span></span>
<span data-ttu-id="9ddde-139">要篩選的事件嚴重性。</span><span class="sxs-lookup"><span data-stu-id="9ddde-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9ddde-140">-StartTime</span></span>
<span data-ttu-id="9ddde-141">指定搜尋視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="9ddde-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="9ddde-142">使用此參數只取得指定時間之後發生的事件。</span><span class="sxs-lookup"><span data-stu-id="9ddde-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ddde-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ddde-143">CommonParameters</span></span>
<span data-ttu-id="9ddde-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9ddde-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ddde-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ddde-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ddde-146">輸入</span><span class="sxs-lookup"><span data-stu-id="9ddde-146">INPUTS</span></span>

### <span data-ttu-id="9ddde-147">System.String</span><span class="sxs-lookup"><span data-stu-id="9ddde-147">System.String</span></span>

## <span data-ttu-id="9ddde-148">輸出</span><span class="sxs-lookup"><span data-stu-id="9ddde-148">OUTPUTS</span></span>

### <span data-ttu-id="9ddde-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span><span class="sxs-lookup"><span data-stu-id="9ddde-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="9ddde-150">筆記</span><span class="sxs-lookup"><span data-stu-id="9ddde-150">NOTES</span></span>

## <span data-ttu-id="9ddde-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ddde-151">RELATED LINKS</span></span>
