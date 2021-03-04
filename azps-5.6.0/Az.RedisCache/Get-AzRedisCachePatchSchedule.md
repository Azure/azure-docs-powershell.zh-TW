---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 297966fe0ad59948fd321ec52cf066ad5caa3d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916508"
---
# <span data-ttu-id="e292a-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e292a-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="e292a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e292a-102">SYNOPSIS</span></span>
<span data-ttu-id="e292a-103">獲得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="e292a-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="e292a-104">語法</span><span class="sxs-lookup"><span data-stu-id="e292a-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e292a-105">描述</span><span class="sxs-lookup"><span data-stu-id="e292a-105">DESCRIPTION</span></span>
<span data-ttu-id="e292a-106">**Get-AzRedisCachePatchSchedule** Cmdlet 取得 Azure Redis Cache 中快卡的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="e292a-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="e292a-107">例子</span><span class="sxs-lookup"><span data-stu-id="e292a-107">EXAMPLES</span></span>

### <span data-ttu-id="e292a-108">範例 1：取得修補程式排程</span><span class="sxs-lookup"><span data-stu-id="e292a-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="e292a-109">此命令會從名為 RedisCache06 的緩存中獲得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="e292a-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="e292a-110">參數</span><span class="sxs-lookup"><span data-stu-id="e292a-110">PARAMETERS</span></span>

### <span data-ttu-id="e292a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e292a-111">-DefaultProfile</span></span>
<span data-ttu-id="e292a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e292a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e292a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e292a-113">-Name</span></span>
<span data-ttu-id="e292a-114">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="e292a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="e292a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e292a-115">-ResourceGroupName</span></span>
<span data-ttu-id="e292a-116">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e292a-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="e292a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e292a-117">CommonParameters</span></span>
<span data-ttu-id="e292a-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e292a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e292a-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e292a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e292a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="e292a-120">INPUTS</span></span>

### <span data-ttu-id="e292a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e292a-121">System.String</span></span>

## <span data-ttu-id="e292a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="e292a-122">OUTPUTS</span></span>

### <span data-ttu-id="e292a-123">Microsoft.Azure.Commands.RedisCache.models.PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e292a-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="e292a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="e292a-124">NOTES</span></span>
* <span data-ttu-id="e292a-125">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="e292a-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e292a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="e292a-126">RELATED LINKS</span></span>

[<span data-ttu-id="e292a-127">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e292a-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="e292a-128">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="e292a-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="e292a-129">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="e292a-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


