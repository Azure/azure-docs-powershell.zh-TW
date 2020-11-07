---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 091d3d52da1319842d221881f03fca2b21353fa9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623592"
---
# <span data-ttu-id="ad13e-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="ad13e-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="ad13e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ad13e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad13e-103">取得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="ad13e-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad13e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ad13e-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad13e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ad13e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad13e-106">AzureRmRedisCachePatchSchedule Cmdlet 會取得 Azure Redis Cache 中 **快取** 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="ad13e-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="ad13e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ad13e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad13e-108">範例1：取得修補程式排程</span><span class="sxs-lookup"><span data-stu-id="ad13e-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="ad13e-109">這個命令會從快取中取得名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="ad13e-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="ad13e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ad13e-110">PARAMETERS</span></span>

### <span data-ttu-id="ad13e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad13e-111">-DefaultProfile</span></span>
<span data-ttu-id="ad13e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ad13e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad13e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ad13e-113">-Name</span></span>
<span data-ttu-id="ad13e-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad13e-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ad13e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad13e-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad13e-116">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ad13e-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="ad13e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad13e-117">CommonParameters</span></span>
<span data-ttu-id="ad13e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ad13e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad13e-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ad13e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad13e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ad13e-120">INPUTS</span></span>

### <span data-ttu-id="ad13e-121">所有</span><span class="sxs-lookup"><span data-stu-id="ad13e-121">None</span></span>
<span data-ttu-id="ad13e-122">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ad13e-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ad13e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ad13e-123">OUTPUTS</span></span>

### <span data-ttu-id="ad13e-124">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="ad13e-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="ad13e-125">這個 Cmdlet 會傳回在快取上設定的修補程式排程專案。</span><span class="sxs-lookup"><span data-stu-id="ad13e-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="ad13e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ad13e-126">NOTES</span></span>
* <span data-ttu-id="ad13e-127">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="ad13e-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ad13e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="ad13e-128">RELATED LINKS</span></span>

[<span data-ttu-id="ad13e-129">新-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="ad13e-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="ad13e-130">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="ad13e-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="ad13e-131">移除-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="ad13e-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


