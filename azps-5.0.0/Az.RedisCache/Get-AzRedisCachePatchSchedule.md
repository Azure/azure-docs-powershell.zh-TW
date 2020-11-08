---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138998"
---
# <span data-ttu-id="cf3bd-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cf3bd-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="cf3bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3bd-103">取得修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="cf3bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf3bd-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf3bd-105">DESCRIPTION</span></span>
<span data-ttu-id="cf3bd-106">AzRedisCachePatchSchedule Cmdlet 會取得 Azure Redis Cache 中 **快取** 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="cf3bd-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf3bd-107">EXAMPLES</span></span>

### <span data-ttu-id="cf3bd-108">範例1：取得修補程式排程</span><span class="sxs-lookup"><span data-stu-id="cf3bd-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="cf3bd-109">這個命令會從快取中取得名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="cf3bd-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf3bd-110">PARAMETERS</span></span>

### <span data-ttu-id="cf3bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3bd-111">-DefaultProfile</span></span>
<span data-ttu-id="cf3bd-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf3bd-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf3bd-113">-Name</span></span>
<span data-ttu-id="cf3bd-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="cf3bd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3bd-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf3bd-116">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="cf3bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3bd-117">CommonParameters</span></span>
<span data-ttu-id="cf3bd-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3bd-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3bd-120">輸入</span><span class="sxs-lookup"><span data-stu-id="cf3bd-120">INPUTS</span></span>

### <span data-ttu-id="cf3bd-121">System.object</span><span class="sxs-lookup"><span data-stu-id="cf3bd-121">System.String</span></span>

## <span data-ttu-id="cf3bd-122">輸出</span><span class="sxs-lookup"><span data-stu-id="cf3bd-122">OUTPUTS</span></span>

### <span data-ttu-id="cf3bd-123">PSScheduleEntry 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="cf3bd-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="cf3bd-124">筆記</span><span class="sxs-lookup"><span data-stu-id="cf3bd-124">NOTES</span></span>
* <span data-ttu-id="cf3bd-125">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="cf3bd-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="cf3bd-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf3bd-126">RELATED LINKS</span></span>

[<span data-ttu-id="cf3bd-127">新-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cf3bd-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="cf3bd-128">新-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="cf3bd-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="cf3bd-129">移除-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="cf3bd-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


