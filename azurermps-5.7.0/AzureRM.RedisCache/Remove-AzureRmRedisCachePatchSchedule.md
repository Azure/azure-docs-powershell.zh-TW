---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452088"
---
# <span data-ttu-id="4e68c-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4e68c-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="4e68c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e68c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e68c-103">移除 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="4e68c-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e68c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e68c-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e68c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e68c-105">DESCRIPTION</span></span>
<span data-ttu-id="4e68c-106">AzureRmRedisCachePatchSchedule Cmdlet 會從 Azure Redis Cache 中的快 **取** 中移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="4e68c-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="4e68c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e68c-107">EXAMPLES</span></span>

### <span data-ttu-id="4e68c-108">範例1：移除修補程式排程</span><span class="sxs-lookup"><span data-stu-id="4e68c-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="4e68c-109">這個命令會從快取中移除名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="4e68c-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="4e68c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e68c-110">PARAMETERS</span></span>

### <span data-ttu-id="4e68c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e68c-111">-DefaultProfile</span></span>
<span data-ttu-id="4e68c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e68c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e68c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e68c-113">-Name</span></span>
<span data-ttu-id="4e68c-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e68c-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="4e68c-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e68c-115">-PassThru</span></span>
<span data-ttu-id="4e68c-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="4e68c-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e68c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e68c-118">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e68c-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="4e68c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4e68c-119">-Confirm</span></span>
<span data-ttu-id="4e68c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e68c-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e68c-121">-WhatIf</span></span>
<span data-ttu-id="4e68c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e68c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e68c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e68c-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e68c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e68c-124">CommonParameters</span></span>
<span data-ttu-id="4e68c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e68c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e68c-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e68c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e68c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4e68c-127">INPUTS</span></span>

### <span data-ttu-id="4e68c-128">所有</span><span class="sxs-lookup"><span data-stu-id="4e68c-128">None</span></span>
<span data-ttu-id="4e68c-129">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e68c-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="4e68c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4e68c-130">OUTPUTS</span></span>

### <span data-ttu-id="4e68c-131">所有</span><span class="sxs-lookup"><span data-stu-id="4e68c-131">None</span></span>

## <span data-ttu-id="4e68c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4e68c-132">NOTES</span></span>
* <span data-ttu-id="4e68c-133">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="4e68c-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="4e68c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e68c-134">RELATED LINKS</span></span>

[<span data-ttu-id="4e68c-135">AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4e68c-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4e68c-136">新-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="4e68c-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="4e68c-137">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="4e68c-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


