---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: ac1184dcdcc55a0b5cac28f996c29c3476ba3613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625259"
---
# <span data-ttu-id="355ec-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="355ec-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="355ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="355ec-102">SYNOPSIS</span></span>
<span data-ttu-id="355ec-103">取得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="355ec-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="355ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="355ec-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="355ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="355ec-105">DESCRIPTION</span></span>
<span data-ttu-id="355ec-106">AzureRmRedisCachePatchSchedule Cmdlet 會取得 Azure Redis Cache 中 **快取** 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="355ec-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="355ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="355ec-107">EXAMPLES</span></span>

### <span data-ttu-id="355ec-108">範例1：取得修補程式排程</span><span class="sxs-lookup"><span data-stu-id="355ec-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="355ec-109">這個命令會從快取中取得名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="355ec-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="355ec-110">參數</span><span class="sxs-lookup"><span data-stu-id="355ec-110">PARAMETERS</span></span>

### <span data-ttu-id="355ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="355ec-111">-DefaultProfile</span></span>
<span data-ttu-id="355ec-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="355ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="355ec-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="355ec-113">-Name</span></span>
<span data-ttu-id="355ec-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="355ec-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="355ec-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355ec-115">-ResourceGroupName</span></span>
<span data-ttu-id="355ec-116">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="355ec-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="355ec-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="355ec-117">CommonParameters</span></span>
<span data-ttu-id="355ec-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="355ec-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="355ec-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="355ec-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="355ec-120">輸入</span><span class="sxs-lookup"><span data-stu-id="355ec-120">INPUTS</span></span>

### <span data-ttu-id="355ec-121">System.object</span><span class="sxs-lookup"><span data-stu-id="355ec-121">System.String</span></span>

## <span data-ttu-id="355ec-122">輸出</span><span class="sxs-lookup"><span data-stu-id="355ec-122">OUTPUTS</span></span>

### <span data-ttu-id="355ec-123">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="355ec-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="355ec-124">筆記</span><span class="sxs-lookup"><span data-stu-id="355ec-124">NOTES</span></span>
* <span data-ttu-id="355ec-125">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="355ec-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="355ec-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="355ec-126">RELATED LINKS</span></span>

[<span data-ttu-id="355ec-127">新-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="355ec-127">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="355ec-128">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="355ec-128">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="355ec-129">移除-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="355ec-129">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


