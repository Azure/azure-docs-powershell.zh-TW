---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCachePatchSchedule.md
ms.openlocfilehash: ebc51005bcffdde2ad5f64764e90440e8d1e7583
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904353"
---
# <span data-ttu-id="fca4e-101">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fca4e-101">New-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="fca4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fca4e-102">SYNOPSIS</span></span>
<span data-ttu-id="fca4e-103">新增修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="fca4e-103">Adds a patch schedule.</span></span>

## <span data-ttu-id="fca4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="fca4e-104">SYNTAX</span></span>

```
New-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca4e-105">描述</span><span class="sxs-lookup"><span data-stu-id="fca4e-105">DESCRIPTION</span></span>
<span data-ttu-id="fca4e-106">**New-AzRedisCachePatchSchedule** Cmdlet 會將修補程式排程新增到 Azure Redis Cache 中的緩存。</span><span class="sxs-lookup"><span data-stu-id="fca4e-106">The **New-AzRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="fca4e-107">例子</span><span class="sxs-lookup"><span data-stu-id="fca4e-107">EXAMPLES</span></span>

### <span data-ttu-id="fca4e-108">範例 1：在緩存上建立及新增修補程式排程</span><span class="sxs-lookup"><span data-stu-id="fca4e-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="fca4e-109">此命令會將修補程式排程新增到名為 RedisCache06 的緩存。</span><span class="sxs-lookup"><span data-stu-id="fca4e-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="fca4e-110">專案參數會採用使用 **New-AzRedisCacheScheduleEntry** 建立排程的命令做為值。</span><span class="sxs-lookup"><span data-stu-id="fca4e-110">The Entries parameter takes as its value a command that uses **New-AzRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="fca4e-111">參數</span><span class="sxs-lookup"><span data-stu-id="fca4e-111">PARAMETERS</span></span>

### <span data-ttu-id="fca4e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca4e-112">-DefaultProfile</span></span>
<span data-ttu-id="fca4e-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fca4e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fca4e-114">-專案</span><span class="sxs-lookup"><span data-stu-id="fca4e-114">-Entries</span></span>
<span data-ttu-id="fca4e-115">指定此 Cmdlet 在緩存上設定排程的陣列。</span><span class="sxs-lookup"><span data-stu-id="fca4e-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="fca4e-116">若要取得 **PSScheduleEntry** 物件，請使用 New-AzRedisCacheScheduleEntry Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fca4e-116">To obtain a **PSScheduleEntry** object, use the New-AzRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="fca4e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fca4e-117">-Name</span></span>
<span data-ttu-id="fca4e-118">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="fca4e-118">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="fca4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="fca4e-120">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="fca4e-120">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="fca4e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="fca4e-121">-Confirm</span></span>
<span data-ttu-id="fca4e-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fca4e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca4e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca4e-123">-WhatIf</span></span>
<span data-ttu-id="fca4e-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fca4e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fca4e-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fca4e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca4e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca4e-126">CommonParameters</span></span>
<span data-ttu-id="fca4e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fca4e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca4e-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fca4e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca4e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fca4e-129">INPUTS</span></span>

### <span data-ttu-id="fca4e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fca4e-130">System.String</span></span>

### <span data-ttu-id="fca4e-131">Microsoft.Azure.Commands.RedisCache.models.PSScheduleEntry[]</span><span class="sxs-lookup"><span data-stu-id="fca4e-131">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry[]</span></span>

## <span data-ttu-id="fca4e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fca4e-132">OUTPUTS</span></span>

### <span data-ttu-id="fca4e-133">Microsoft.Azure.Commands.RedisCache.models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="fca4e-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="fca4e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fca4e-134">NOTES</span></span>
* <span data-ttu-id="fca4e-135">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="fca4e-135">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="fca4e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fca4e-136">RELATED LINKS</span></span>

[<span data-ttu-id="fca4e-137">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fca4e-137">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="fca4e-138">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="fca4e-138">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="fca4e-139">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="fca4e-139">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


