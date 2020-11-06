---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452104"
---
# <span data-ttu-id="3e2c5-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="3e2c5-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="3e2c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2c5-103">取得保存庫中 Azure Site Recovery 事件的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e2c5-104">SYNTAX</span></span>

### <span data-ttu-id="3e2c5-105">ByParam (預設) </span><span class="sxs-lookup"><span data-stu-id="3e2c5-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e2c5-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2c5-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e2c5-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="3e2c5-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e2c5-108">ByName</span><span class="sxs-lookup"><span data-stu-id="3e2c5-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e2c5-109">說明</span><span class="sxs-lookup"><span data-stu-id="3e2c5-109">DESCRIPTION</span></span>
<span data-ttu-id="3e2c5-110">AzureRmRecoveryServicesAsrEvent 會根據指定的選取範圍篩選， **取得** vault 中的事件清單。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="3e2c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="3e2c5-111">EXAMPLES</span></span>

### <span data-ttu-id="3e2c5-112">範例1</span><span class="sxs-lookup"><span data-stu-id="3e2c5-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="3e2c5-113">所有事件的清單。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-113">List of all events.</span></span>

### <span data-ttu-id="3e2c5-114">範例2</span><span class="sxs-lookup"><span data-stu-id="3e2c5-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="3e2c5-115">依名稱取得事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-115">Get event by name.</span></span>

### <span data-ttu-id="3e2c5-116">範例3</span><span class="sxs-lookup"><span data-stu-id="3e2c5-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="3e2c5-117">受影響物件的事件清單。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-117">List of event for affected Object.</span></span>

### <span data-ttu-id="3e2c5-118">範例4</span><span class="sxs-lookup"><span data-stu-id="3e2c5-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="3e2c5-119">在時間開始時間與結束時間、嚴重性緊急和健康情況類型 VmHealth 之間的事件清單。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="3e2c5-120">參數</span><span class="sxs-lookup"><span data-stu-id="3e2c5-120">PARAMETERS</span></span>

### <span data-ttu-id="3e2c5-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="3e2c5-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="3e2c5-122">指定搜尋的 AffectedObject FriendlyName。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2c5-123">-DefaultProfile</span></span>
<span data-ttu-id="3e2c5-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3e2c5-125">-EndTime</span></span>
<span data-ttu-id="3e2c5-126">指定搜尋視窗的結束時間。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="3e2c5-127">使用這個參數，只取得在指定的時間之前發生的那些事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-128">-事件</span><span class="sxs-lookup"><span data-stu-id="3e2c5-128">-EventType</span></span>
<span data-ttu-id="3e2c5-129">依事件種類篩選事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-130">-結構</span><span class="sxs-lookup"><span data-stu-id="3e2c5-130">-Fabric</span></span>
<span data-ttu-id="3e2c5-131">依指定結構篩選事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="3e2c5-132">-FabricId</span></span>
<span data-ttu-id="3e2c5-133">指定要篩選的 fabricId。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e2c5-134">-Name</span></span>
<span data-ttu-id="3e2c5-135">指定要搜尋的事件名稱。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e2c5-136">-ResourceId</span></span>
<span data-ttu-id="3e2c5-137">Specifes 事件 ReourceId 事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-138">-嚴重度</span><span class="sxs-lookup"><span data-stu-id="3e2c5-138">-Severity</span></span>
<span data-ttu-id="3e2c5-139">要篩選的事件嚴重度。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3e2c5-140">-StartTime</span></span>
<span data-ttu-id="3e2c5-141">指定搜尋視窗的開始時間。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="3e2c5-142">使用這個參數，只取得在指定時間之後所發生的那些事件。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e2c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2c5-143">CommonParameters</span></span>
<span data-ttu-id="3e2c5-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2c5-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e2c5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2c5-146">輸入</span><span class="sxs-lookup"><span data-stu-id="3e2c5-146">INPUTS</span></span>

### <span data-ttu-id="3e2c5-147">RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3e2c5-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3e2c5-148">輸出</span><span class="sxs-lookup"><span data-stu-id="3e2c5-148">OUTPUTS</span></span>

### <span data-ttu-id="3e2c5-149">System.object. IEnumerable "1 [ASREvent，RecoveryServices. SiteRecovery，Version = 0.1.0.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="3e2c5-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3e2c5-150">筆記</span><span class="sxs-lookup"><span data-stu-id="3e2c5-150">NOTES</span></span>

## <span data-ttu-id="3e2c5-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e2c5-151">RELATED LINKS</span></span>
