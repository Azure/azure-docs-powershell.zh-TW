---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 367327e19ff95132b7b7d6bc2d86970892ab6e55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792296"
---
# <span data-ttu-id="15e6d-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="15e6d-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="15e6d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15e6d-102">SYNOPSIS</span></span>
<span data-ttu-id="15e6d-103">新增 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="15e6d-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="15e6d-104">句法</span><span class="sxs-lookup"><span data-stu-id="15e6d-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15e6d-105">說明</span><span class="sxs-lookup"><span data-stu-id="15e6d-105">DESCRIPTION</span></span>
<span data-ttu-id="15e6d-106">**新的-AzRedisCachePatchSchedule** Cmdlet 會將修補程式排程新增至 Azure Redis 快取中的快取。</span><span class="sxs-lookup"><span data-stu-id="15e6d-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="15e6d-107">示例</span><span class="sxs-lookup"><span data-stu-id="15e6d-107">EXAMPLES</span></span>

### <span data-ttu-id="15e6d-108">範例1：在快取中建立及新增修補程式排程</span><span class="sxs-lookup"><span data-stu-id="15e6d-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="15e6d-109">這個命令會將修補程式排程新增到名為 RedisCache06 的快取。</span><span class="sxs-lookup"><span data-stu-id="15e6d-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="15e6d-110">Entries 參數會將使用 **New-AzRedisCacheScheduleEntry** 的命令當作其值來建立排程。</span><span class="sxs-lookup"><span data-stu-id="15e6d-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="15e6d-111">參數</span><span class="sxs-lookup"><span data-stu-id="15e6d-111">PARAMETERS</span></span>

### <span data-ttu-id="15e6d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15e6d-112">-DefaultProfile</span></span>
<span data-ttu-id="15e6d-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15e6d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15e6d-114">-專案</span><span class="sxs-lookup"><span data-stu-id="15e6d-114">-Entries</span></span>
<span data-ttu-id="15e6d-115">指定此 Cmdlet 在快取上設定的排程陣列。</span><span class="sxs-lookup"><span data-stu-id="15e6d-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="15e6d-116">若要取得 **PSScheduleEntry** 物件，請使用 New-AzRedisCacheScheduleEntry Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15e6d-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e6d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="15e6d-117">-Name</span></span>
<span data-ttu-id="15e6d-118">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="15e6d-118">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e6d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15e6d-119">-ResourceGroupName</span></span>
<span data-ttu-id="15e6d-120">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15e6d-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e6d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="15e6d-121">-Confirm</span></span>
<span data-ttu-id="15e6d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="15e6d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15e6d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15e6d-123">-WhatIf</span></span>
<span data-ttu-id="15e6d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15e6d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15e6d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15e6d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15e6d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e6d-126">CommonParameters</span></span>
<span data-ttu-id="15e6d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15e6d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e6d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15e6d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e6d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="15e6d-129">INPUTS</span></span>

### <span data-ttu-id="15e6d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="15e6d-130">System.String</span></span>

### <span data-ttu-id="15e6d-131">PSScheduleEntry [] 的 RedisCache []</span><span class="sxs-lookup"><span data-stu-id="15e6d-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="15e6d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="15e6d-132">OUTPUTS</span></span>

### <span data-ttu-id="15e6d-133">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="15e6d-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="15e6d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="15e6d-134">NOTES</span></span>
* <span data-ttu-id="15e6d-135">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="15e6d-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="15e6d-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="15e6d-136">RELATED LINKS</span></span>

[<span data-ttu-id="15e6d-137">AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="15e6d-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="15e6d-138">新-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="15e6d-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="15e6d-139">移除-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="15e6d-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


