---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 6b2fbc3f28b34e1c71f8093953c54c107f4a0357
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620997"
---
# <span data-ttu-id="a60ca-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a60ca-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a60ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a60ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a60ca-103">取得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="a60ca-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="a60ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="a60ca-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="a60ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a60ca-106">AzRedisCachePatchSchedule Cmdlet 會取得 Azure Redis Cache 中 **快取** 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="a60ca-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a60ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="a60ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a60ca-108">範例1：取得修補程式排程</span><span class="sxs-lookup"><span data-stu-id="a60ca-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a60ca-109">這個命令會從快取中取得名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="a60ca-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a60ca-110">參數</span><span class="sxs-lookup"><span data-stu-id="a60ca-110">PARAMETERS</span></span>

### <span data-ttu-id="a60ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60ca-111">-DefaultProfile</span></span>
<span data-ttu-id="a60ca-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a60ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60ca-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a60ca-113">-Name</span></span>
<span data-ttu-id="a60ca-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a60ca-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a60ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="a60ca-116">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a60ca-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a60ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60ca-117">CommonParameters</span></span>
<span data-ttu-id="a60ca-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a60ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60ca-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a60ca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60ca-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a60ca-120">INPUTS</span></span>

### <span data-ttu-id="a60ca-121">System.object</span><span class="sxs-lookup"><span data-stu-id="a60ca-121">System.String</span></span>

## <span data-ttu-id="a60ca-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a60ca-122">OUTPUTS</span></span>

### <span data-ttu-id="a60ca-123">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="a60ca-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="a60ca-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a60ca-124">NOTES</span></span>
* <span data-ttu-id="a60ca-125">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="a60ca-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a60ca-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a60ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="a60ca-127">新-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a60ca-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a60ca-128">新-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a60ca-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="a60ca-129">移除-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a60ca-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


