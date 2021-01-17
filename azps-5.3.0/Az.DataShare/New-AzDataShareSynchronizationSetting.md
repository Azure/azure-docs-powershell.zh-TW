---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: df8f61b10750f50bef1b3417da7f28be4ec0d0d5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286363"
---
# <span data-ttu-id="e1d67-101">New-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="e1d67-101">New-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="e1d67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1d67-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d67-103">建立共用的同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="e1d67-103">Creates Synchronization setting for a share.</span></span>

## <span data-ttu-id="e1d67-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1d67-104">SYNTAX</span></span>

```
New-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -Name <String> -RecurrenceInterval <String> -SynchronizationTime <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d67-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1d67-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d67-106">[ **新-AzDataShareSynchronizationSetting** ] 會建立在 [共用帳戶] 中的 [共用] 設定，以在每日或每小時的特定時間間隔進行共用。</span><span class="sxs-lookup"><span data-stu-id="e1d67-106">The **New-AzDataShareSynchronizationSetting** creates a synchronization setting for share in share account for a recurrence interval of either daily or hourly at a particular time.</span></span>

## <span data-ttu-id="e1d67-107">示例</span><span class="sxs-lookup"><span data-stu-id="e1d67-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d67-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e1d67-108">Example 1</span></span>
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

<span data-ttu-id="e1d67-109">這個命令會針對 [資料共用帳戶 WikiAds] 中的 [共用 AdsShare]，在 9:00 am 的每日定期間隔建立同步處理設定。</span><span class="sxs-lookup"><span data-stu-id="e1d67-109">This commands creates a synchronization setting on Daily recurrence interval at 9:00 am for share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="e1d67-110">參數</span><span class="sxs-lookup"><span data-stu-id="e1d67-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d67-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e1d67-111">-AccountName</span></span>
<span data-ttu-id="e1d67-112">Azure 資料共用帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-112">Azure data share account name</span></span>

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

### <span data-ttu-id="e1d67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d67-113">-DefaultProfile</span></span>
<span data-ttu-id="e1d67-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1d67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1d67-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-115">-Name</span></span>
<span data-ttu-id="e1d67-116">同步處理設定名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-116">Synchronization setting name</span></span>

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

### <span data-ttu-id="e1d67-117">-RecurrenceInterval</span><span class="sxs-lookup"><span data-stu-id="e1d67-117">-RecurrenceInterval</span></span>
<span data-ttu-id="e1d67-118">同步處理設定的定期間隔 (天或小時) </span><span class="sxs-lookup"><span data-stu-id="e1d67-118">The recurrence interval for the synchronization setting (Day or Hour)</span></span>

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

### <span data-ttu-id="e1d67-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d67-119">-ResourceGroupName</span></span>
<span data-ttu-id="e1d67-120">Azure 資料共用帳戶的資源組名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="e1d67-121">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-121">-ShareName</span></span>
<span data-ttu-id="e1d67-122">Azure 資料共用名稱</span><span class="sxs-lookup"><span data-stu-id="e1d67-122">Azure data share name</span></span>

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

### <span data-ttu-id="e1d67-123">-SynchronizationTime</span><span class="sxs-lookup"><span data-stu-id="e1d67-123">-SynchronizationTime</span></span>
<span data-ttu-id="e1d67-124">排定的同步處理設定的開始時間</span><span class="sxs-lookup"><span data-stu-id="e1d67-124">The start time of the scheduled synchronization setting</span></span>

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

### <span data-ttu-id="e1d67-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e1d67-125">-Confirm</span></span>
<span data-ttu-id="e1d67-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e1d67-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d67-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d67-127">-WhatIf</span></span>
<span data-ttu-id="e1d67-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e1d67-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1d67-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1d67-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d67-130">CommonParameters</span></span>
<span data-ttu-id="e1d67-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1d67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d67-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e1d67-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d67-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e1d67-133">INPUTS</span></span>

### <span data-ttu-id="e1d67-134">所有</span><span class="sxs-lookup"><span data-stu-id="e1d67-134">None</span></span>

## <span data-ttu-id="e1d67-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e1d67-135">OUTPUTS</span></span>

### <span data-ttu-id="e1d67-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="e1d67-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="e1d67-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e1d67-137">NOTES</span></span>

## <span data-ttu-id="e1d67-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1d67-138">RELATED LINKS</span></span>
