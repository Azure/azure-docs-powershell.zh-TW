---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 5c4375b4bb325877ec0520e0641496e8adfafec0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444395"
---
# <span data-ttu-id="71ec7-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="71ec7-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="71ec7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="71ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="71ec7-103">新增 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="71ec7-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ec7-104">句法</span><span class="sxs-lookup"><span data-stu-id="71ec7-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ec7-105">說明</span><span class="sxs-lookup"><span data-stu-id="71ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="71ec7-106">**新的-AzureRmRedisCachePatchSchedule** Cmdlet 會將修補程式排程新增至 Azure Redis 快取中的快取。</span><span class="sxs-lookup"><span data-stu-id="71ec7-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="71ec7-107">示例</span><span class="sxs-lookup"><span data-stu-id="71ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="71ec7-108">範例1：在快取中建立及新增修補程式排程</span><span class="sxs-lookup"><span data-stu-id="71ec7-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="71ec7-109">這個命令會將修補程式排程新增到名為 RedisCache06 的快取。</span><span class="sxs-lookup"><span data-stu-id="71ec7-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="71ec7-110">Entries 參數會將使用 **New-AzureRmRedisCacheScheduleEntry** 的命令當作其值來建立排程。</span><span class="sxs-lookup"><span data-stu-id="71ec7-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="71ec7-111">參數</span><span class="sxs-lookup"><span data-stu-id="71ec7-111">PARAMETERS</span></span>

### <span data-ttu-id="71ec7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ec7-112">-DefaultProfile</span></span>
<span data-ttu-id="71ec7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="71ec7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71ec7-114">-專案</span><span class="sxs-lookup"><span data-stu-id="71ec7-114">-Entries</span></span>
<span data-ttu-id="71ec7-115">指定此 Cmdlet 在快取上設定的排程陣列。</span><span class="sxs-lookup"><span data-stu-id="71ec7-115">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="71ec7-116">若要取得 **PSScheduleEntry** 物件，請使用 New-AzureRmRedisCacheScheduleEntry Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71ec7-116">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

```yaml
Type: PSScheduleEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ec7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="71ec7-117">-Name</span></span>
<span data-ttu-id="71ec7-118">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="71ec7-118">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ec7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71ec7-119">-ResourceGroupName</span></span>
<span data-ttu-id="71ec7-120">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="71ec7-120">Specifies the name of the resource group which contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71ec7-121">-確認</span><span class="sxs-lookup"><span data-stu-id="71ec7-121">-Confirm</span></span>
<span data-ttu-id="71ec7-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="71ec7-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ec7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ec7-123">-WhatIf</span></span>
<span data-ttu-id="71ec7-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="71ec7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71ec7-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71ec7-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ec7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ec7-126">CommonParameters</span></span>
<span data-ttu-id="71ec7-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="71ec7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ec7-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="71ec7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ec7-129">輸入</span><span class="sxs-lookup"><span data-stu-id="71ec7-129">INPUTS</span></span>

### <span data-ttu-id="71ec7-130">所有</span><span class="sxs-lookup"><span data-stu-id="71ec7-130">None</span></span>
<span data-ttu-id="71ec7-131">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="71ec7-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="71ec7-132">輸出</span><span class="sxs-lookup"><span data-stu-id="71ec7-132">OUTPUTS</span></span>

### <span data-ttu-id="71ec7-133">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="71ec7-133">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="71ec7-134">這個 Cmdlet 會傳回在快取上設定的修補程式排程專案。</span><span class="sxs-lookup"><span data-stu-id="71ec7-134">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="71ec7-135">筆記</span><span class="sxs-lookup"><span data-stu-id="71ec7-135">NOTES</span></span>
* <span data-ttu-id="71ec7-136">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="71ec7-136">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="71ec7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="71ec7-137">RELATED LINKS</span></span>

[<span data-ttu-id="71ec7-138">AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="71ec7-138">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="71ec7-139">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="71ec7-139">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="71ec7-140">移除-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="71ec7-140">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


