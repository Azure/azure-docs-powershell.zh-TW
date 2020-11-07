---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: F7FAFF52-5E07-4D88-B48F-BC70C43E8691
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: b04977869364f43644556b9ef6bf16ac68d01f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623864"
---
# <span data-ttu-id="136ad-101">New-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="136ad-101">New-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="136ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="136ad-102">SYNOPSIS</span></span>
<span data-ttu-id="136ad-103">新增 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="136ad-103">Adds a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="136ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="136ad-104">SYNTAX</span></span>

```
New-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String> -Entries <PSScheduleEntry[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="136ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="136ad-105">DESCRIPTION</span></span>
<span data-ttu-id="136ad-106">**新的-AzureRmRedisCachePatchSchedule** Cmdlet 會將修補程式排程新增至 Azure Redis 快取中的快取。</span><span class="sxs-lookup"><span data-stu-id="136ad-106">The **New-AzureRmRedisCachePatchSchedule** cmdlet adds a patch schedule to a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="136ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="136ad-107">EXAMPLES</span></span>

### <span data-ttu-id="136ad-108">範例1：在快取中建立及新增修補程式排程</span><span class="sxs-lookup"><span data-stu-id="136ad-108">Example 1: Create and add a patch schedule on a cache</span></span>
```
PS C:\>New-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Entries @(New-AzureRmRedisCacheScheduleEntry -DayOfWeek "Weekend" -StartHourUtc 2 -MaintenanceWindow "06:00:00")
```

<span data-ttu-id="136ad-109">這個命令會將修補程式排程新增到名為 RedisCache06 的快取。</span><span class="sxs-lookup"><span data-stu-id="136ad-109">This command adds a patch schedule to the cache named RedisCache06.</span></span>
<span data-ttu-id="136ad-110">Entries 參數會將使用 **New-AzureRmRedisCacheScheduleEntry** 的命令當作其值來建立排程。</span><span class="sxs-lookup"><span data-stu-id="136ad-110">The Entries parameter takes as its value a command that uses **New-AzureRmRedisCacheScheduleEntry** to create a schedule.</span></span>

## <span data-ttu-id="136ad-111">參數</span><span class="sxs-lookup"><span data-stu-id="136ad-111">PARAMETERS</span></span>

### <span data-ttu-id="136ad-112">-專案</span><span class="sxs-lookup"><span data-stu-id="136ad-112">-Entries</span></span>
<span data-ttu-id="136ad-113">指定此 Cmdlet 在快取上設定的排程陣列。</span><span class="sxs-lookup"><span data-stu-id="136ad-113">Specifies an array of schedules that this cmdlet sets on a cache.</span></span> <span data-ttu-id="136ad-114">若要取得 **PSScheduleEntry** 物件，請使用 New-AzureRmRedisCacheScheduleEntry Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="136ad-114">To obtain a **PSScheduleEntry** object, use the New-AzureRmRedisCacheScheduleEntry cmdlet.</span></span>

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

### <span data-ttu-id="136ad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="136ad-115">-Name</span></span>
<span data-ttu-id="136ad-116">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="136ad-116">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="136ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="136ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="136ad-118">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="136ad-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="136ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136ad-119">-DefaultProfile</span></span>
<span data-ttu-id="136ad-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="136ad-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136ad-121">CommonParameters</span></span>
<span data-ttu-id="136ad-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="136ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136ad-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="136ad-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136ad-124">輸入</span><span class="sxs-lookup"><span data-stu-id="136ad-124">INPUTS</span></span>

### <span data-ttu-id="136ad-125">所有</span><span class="sxs-lookup"><span data-stu-id="136ad-125">None</span></span>
<span data-ttu-id="136ad-126">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="136ad-126">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="136ad-127">輸出</span><span class="sxs-lookup"><span data-stu-id="136ad-127">OUTPUTS</span></span>

### <span data-ttu-id="136ad-128">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="136ad-128">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="136ad-129">這個 Cmdlet 會傳回在快取上設定的修補程式排程專案。</span><span class="sxs-lookup"><span data-stu-id="136ad-129">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="136ad-130">筆記</span><span class="sxs-lookup"><span data-stu-id="136ad-130">NOTES</span></span>
* <span data-ttu-id="136ad-131">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="136ad-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="136ad-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="136ad-132">RELATED LINKS</span></span>

[<span data-ttu-id="136ad-133">AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="136ad-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="136ad-134">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="136ad-134">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="136ad-135">移除-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="136ad-135">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


