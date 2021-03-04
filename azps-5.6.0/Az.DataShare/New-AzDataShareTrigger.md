---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareTrigger.md
ms.openlocfilehash: fe082dc38f8a16dcca897623c4817d728fdaf3c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905106"
---
# <span data-ttu-id="8d4f9-101">New-AzDataShareTrigger</span><span class="sxs-lookup"><span data-stu-id="8d4f9-101">New-AzDataShareTrigger</span></span>

## <span data-ttu-id="8d4f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8d4f9-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4f9-103">建立共用訂閱的觸發。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-103">Creates a trigger for share subscription.</span></span>

## <span data-ttu-id="8d4f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="8d4f9-104">SYNTAX</span></span>

```
New-AzDataShareTrigger -ResourceGroupName <String> -AccountName <String> [-ShareSubscriptionName <String>]
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d4f9-105">描述</span><span class="sxs-lookup"><span data-stu-id="8d4f9-105">DESCRIPTION</span></span>
<span data-ttu-id="8d4f9-106">**New-AzDataShareTrigger** Cmdlet 會針對 Azure 資料共用帳戶下指定的週期間隔和同步處理時間，建立共用訂閱的觸發程式。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-106">The **New-AzDataShareTrigger** cmdlet creates a trigger for share subscription for the specified recurrence interval and synchronization time under azure data share account.</span></span>

## <span data-ttu-id="8d4f9-107">例子</span><span class="sxs-lookup"><span data-stu-id="8d4f9-107">EXAMPLES</span></span>

### <span data-ttu-id="8d4f9-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8d4f9-108">Example 1</span></span>
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

<span data-ttu-id="8d4f9-109">此命令會針對共用訂閱 AdsShareSubscription 建立一個新的觸發程式 AdsTricription，每天的週期間隔為上午 9 點。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-109">This command creates a new trigger AdsTrigger for share subscription AdsShareSubscription with a daily recurrence interval of 9 am.</span></span>

## <span data-ttu-id="8d4f9-110">參數</span><span class="sxs-lookup"><span data-stu-id="8d4f9-110">PARAMETERS</span></span>

### <span data-ttu-id="8d4f9-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8d4f9-111">-AccountName</span></span>
<span data-ttu-id="8d4f9-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="8d4f9-112">Azure data share account name</span></span>

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

### <span data-ttu-id="8d4f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d4f9-113">-AsJob</span></span>
<span data-ttu-id="8d4f9-114">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8d4f9-114">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="8d4f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4f9-115">-DefaultProfile</span></span>
<span data-ttu-id="8d4f9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d4f9-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8d4f9-117">-Name</span></span>
<span data-ttu-id="8d4f9-118">Azure 資料共用觸發名稱</span><span class="sxs-lookup"><span data-stu-id="8d4f9-118">Azure data share trigger name</span></span>

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

### <span data-ttu-id="8d4f9-119">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="8d4f9-119">-RecurrenceInterval</span></span>
<span data-ttu-id="8d4f9-120">觸發事件的週期間隔 (日或小時) </span><span class="sxs-lookup"><span data-stu-id="8d4f9-120">The recurrence interval for the trigger (Day or Hour)</span></span>

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

### <span data-ttu-id="8d4f9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4f9-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d4f9-122">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="8d4f9-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8d4f9-123">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8d4f9-123">-ShareSubscriptionName</span></span>
<span data-ttu-id="8d4f9-124">Azure 資料共用訂閱名稱</span><span class="sxs-lookup"><span data-stu-id="8d4f9-124">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8d4f9-125">-同步處理時間</span><span class="sxs-lookup"><span data-stu-id="8d4f9-125">-SynchronizationTime</span></span>
<span data-ttu-id="8d4f9-126">觸發程式排定同步處理開始時間</span><span class="sxs-lookup"><span data-stu-id="8d4f9-126">The start time of the scheduled synchronization for the trigger</span></span>

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

### <span data-ttu-id="8d4f9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="8d4f9-127">-Confirm</span></span>
<span data-ttu-id="8d4f9-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d4f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4f9-129">-WhatIf</span></span>
<span data-ttu-id="8d4f9-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4f9-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d4f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4f9-132">CommonParameters</span></span>
<span data-ttu-id="8d4f9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8d4f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4f9-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d4f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4f9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8d4f9-135">INPUTS</span></span>

### <span data-ttu-id="8d4f9-136">沒有</span><span class="sxs-lookup"><span data-stu-id="8d4f9-136">None</span></span>

## <span data-ttu-id="8d4f9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="8d4f9-137">OUTPUTS</span></span>

### <span data-ttu-id="8d4f9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span><span class="sxs-lookup"><span data-stu-id="8d4f9-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareInvitation</span></span>

## <span data-ttu-id="8d4f9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="8d4f9-139">NOTES</span></span>

## <span data-ttu-id="8d4f9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d4f9-140">RELATED LINKS</span></span>
