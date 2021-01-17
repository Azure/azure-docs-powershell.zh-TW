---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: e264dce6c99aaee7803881ab5eaa0ef529a53b48
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286359"
---
# <span data-ttu-id="04678-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="04678-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="04678-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04678-102">SYNOPSIS</span></span>
<span data-ttu-id="04678-103">建立共用訂閱的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="04678-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="04678-104">句法</span><span class="sxs-lookup"><span data-stu-id="04678-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04678-105">說明</span><span class="sxs-lookup"><span data-stu-id="04678-105">DESCRIPTION</span></span>
<span data-ttu-id="04678-106">**新的-AzDataShareTrigger** Cmdlet 會在 azure 資料共用帳戶下，為指定的定期間隔及同步處理時間建立觸發程式。</span><span class="sxs-lookup"><span data-stu-id="04678-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="04678-107">示例</span><span class="sxs-lookup"><span data-stu-id="04678-107">EXAMPLES</span></span>

### <span data-ttu-id="04678-108">範例1</span><span class="sxs-lookup"><span data-stu-id="04678-108">Example 1</span></span>
```
PS C:\> New-AzDataShareTrigger -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -Name "AdsTrigger" -RecurrenceInterval "Day" -SynchronizationTime "9:00"
CreatedAt           : 7/10/2019 12:16:34 AM
CreatedBy           : Ads test
ProvisioningState   : Succeeded
RecurrenceInterval  : Day
SynchronizationMode : Incremental
SynchronizationTime : 7/9/2019 9:00:00 AM
TriggerStatus       : Active
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/triggers/AdsTrigger
Name                : AdsTrigger
Type                : Microsoft.DataShare/Triggers
```

<span data-ttu-id="04678-109">這個命令會針對共用訂閱 AdsShareSubscription 建立新的觸發程式 AdsTrigger，每日定期間隔為 9 am。</span><span class="sxs-lookup"><span data-stu-id="04678-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="04678-110">參數</span><span class="sxs-lookup"><span data-stu-id="04678-110">PARAMETERS</span></span>

### <span data-ttu-id="04678-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04678-111">-AccountName</span></span>
<span data-ttu-id="04678-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="04678-112">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04678-113">-AsJob</span></span>
<span data-ttu-id="04678-114">{{Fill AsJob 描述}}</span><span class="sxs-lookup"><span data-stu-id="04678-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="04678-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04678-115">-DefaultProfile</span></span>
<span data-ttu-id="04678-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="04678-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04678-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="04678-117">-Name</span></span>
<span data-ttu-id="04678-118">Azure 資料共用觸發程式名稱</span><span class="sxs-lookup"><span data-stu-id="04678-118">Azure data share trigger name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="04678-119">-RecurrenceInterval</span></span>
<span data-ttu-id="04678-120">觸發程式 (天或小時的定期間隔) </span><span class="sxs-lookup"><span data-stu-id="04678-120">The recurrence interval for the trigger (Day or Hour)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04678-121">-ResourceGroupName</span></span>
<span data-ttu-id="04678-122">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="04678-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="04678-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="04678-124">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="04678-124">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-125">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="04678-125">-SynchronizationTime</span></span>
<span data-ttu-id="04678-126">觸發程式排程同步處理的開始時間</span><span class="sxs-lookup"><span data-stu-id="04678-126">The start time of the scheduled synchronization for the trigger</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04678-127">-確認</span><span class="sxs-lookup"><span data-stu-id="04678-127">-Confirm</span></span>
<span data-ttu-id="04678-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="04678-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04678-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04678-129">-WhatIf</span></span>
<span data-ttu-id="04678-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="04678-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04678-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="04678-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04678-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04678-132">CommonParameters</span></span>
<span data-ttu-id="04678-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04678-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04678-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="04678-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04678-135">輸入</span><span class="sxs-lookup"><span data-stu-id="04678-135">INPUTS</span></span>

### <span data-ttu-id="04678-136">所有</span><span class="sxs-lookup"><span data-stu-id="04678-136">None</span></span>

## <span data-ttu-id="04678-137">輸出</span><span class="sxs-lookup"><span data-stu-id="04678-137">OUTPUTS</span></span>

### <span data-ttu-id="04678-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="04678-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="04678-139">筆記</span><span class="sxs-lookup"><span data-stu-id="04678-139">NOTES</span></span>

## <span data-ttu-id="04678-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="04678-140">RELATED LINKS</span></span>
