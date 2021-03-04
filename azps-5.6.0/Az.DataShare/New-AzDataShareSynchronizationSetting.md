---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 5632aed8c1b3dde653be65fd587be5f1adf9cbbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913537"
---
# <span data-ttu-id="66c53-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="66c53-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="66c53-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66c53-102">SYNOPSIS</span></span>
<span data-ttu-id="66c53-103">建立共用同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="66c53-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="66c53-104">語法</span><span class="sxs-lookup"><span data-stu-id="66c53-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c53-105">描述</span><span class="sxs-lookup"><span data-stu-id="66c53-105">DESCRIPTION</span></span>
<span data-ttu-id="66c53-106">**New-AzDataShareSynchronizationSetting** 會針對共用帳戶中的共用建立同步處理設定，其週期間隔為每天或每小時一次。</span><span class="sxs-lookup"><span data-stu-id="66c53-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="66c53-107">例子</span><span class="sxs-lookup"><span data-stu-id="66c53-107">EXAMPLES</span></span>

### <span data-ttu-id="66c53-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="66c53-108">Example 1</span></span>
```
PS C:\>  New-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization" -RecurrenceInterval "Day" -SynchronizationTime 9:00
RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : Ads Company
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="66c53-109">這個命令會針對資料共用帳戶 WikiAds 中的 Share AdsShare，在上午 9：00 的每日週期間隔建立同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="66c53-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="66c53-110">參數</span><span class="sxs-lookup"><span data-stu-id="66c53-110">PARAMETERS</span></span>

### <span data-ttu-id="66c53-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="66c53-111">-AccountName</span></span>
<span data-ttu-id="66c53-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="66c53-112">Azure data share account name</span></span>

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

### <span data-ttu-id="66c53-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c53-113">-DefaultProfile</span></span>
<span data-ttu-id="66c53-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="66c53-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66c53-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="66c53-115">-Name</span></span>
<span data-ttu-id="66c53-116">同步處理設定名稱</span><span class="sxs-lookup"><span data-stu-id="66c53-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="66c53-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="66c53-117">-RecurrenceInterval</span></span>
<span data-ttu-id="66c53-118">同步處理設定在日或小時 (週期間隔) </span><span class="sxs-lookup"><span data-stu-id="66c53-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="66c53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c53-119">-ResourceGroupName</span></span>
<span data-ttu-id="66c53-120">Azure 資料共用帳戶的資源組名</span><span class="sxs-lookup"><span data-stu-id="66c53-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="66c53-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="66c53-121">-ShareName</span></span>
<span data-ttu-id="66c53-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="66c53-122">Azure data share name</span></span>

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

### <span data-ttu-id="66c53-123">-同步處理時間</span><span class="sxs-lookup"><span data-stu-id="66c53-123">-SynchronizationTime</span></span>
<span data-ttu-id="66c53-124">排定同步處理設定開始時間</span><span class="sxs-lookup"><span data-stu-id="66c53-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="66c53-125">-確認</span><span class="sxs-lookup"><span data-stu-id="66c53-125">-Confirm</span></span>
<span data-ttu-id="66c53-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="66c53-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c53-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c53-127">-WhatIf</span></span>
<span data-ttu-id="66c53-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66c53-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="66c53-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66c53-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c53-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c53-130">CommonParameters</span></span>
<span data-ttu-id="66c53-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66c53-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c53-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66c53-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c53-133">輸入</span><span class="sxs-lookup"><span data-stu-id="66c53-133">INPUTS</span></span>

### <span data-ttu-id="66c53-134">沒有</span><span class="sxs-lookup"><span data-stu-id="66c53-134">None</span></span>

## <span data-ttu-id="66c53-135">輸出</span><span class="sxs-lookup"><span data-stu-id="66c53-135">OUTPUTS</span></span>

### <span data-ttu-id="66c53-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="66c53-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="66c53-137">筆記</span><span class="sxs-lookup"><span data-stu-id="66c53-137">NOTES</span></span>

## <span data-ttu-id="66c53-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="66c53-138">RELATED LINKS</span></span>
