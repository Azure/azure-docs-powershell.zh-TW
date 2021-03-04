---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 42f91d45bf93f453e4c6368abaabcb64f9234771
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914689"
---
# <span data-ttu-id="6d68a-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d68a-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="6d68a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d68a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d68a-103">移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="6d68a-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="6d68a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d68a-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d68a-105">描述</span><span class="sxs-lookup"><span data-stu-id="6d68a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d68a-106">**Remove-AzRedisCachePatchSchedule** Cmdlet 會從 Azure Redis Cache 中的緩存移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="6d68a-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="6d68a-107">例子</span><span class="sxs-lookup"><span data-stu-id="6d68a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d68a-108">範例 1：移除修補程式排程</span><span class="sxs-lookup"><span data-stu-id="6d68a-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="6d68a-109">此命令會從名為 RedisCache06 的緩存移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="6d68a-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="6d68a-110">參數</span><span class="sxs-lookup"><span data-stu-id="6d68a-110">PARAMETERS</span></span>

### <span data-ttu-id="6d68a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d68a-111">-DefaultProfile</span></span>
<span data-ttu-id="6d68a-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6d68a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d68a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d68a-113">-Name</span></span>
<span data-ttu-id="6d68a-114">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d68a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="6d68a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d68a-115">-PassThru</span></span>
<span data-ttu-id="6d68a-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6d68a-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d68a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d68a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d68a-118">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6d68a-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="6d68a-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6d68a-119">-Confirm</span></span>
<span data-ttu-id="6d68a-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d68a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d68a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d68a-121">-WhatIf</span></span>
<span data-ttu-id="6d68a-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d68a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d68a-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d68a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d68a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d68a-124">CommonParameters</span></span>
<span data-ttu-id="6d68a-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d68a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d68a-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6d68a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d68a-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6d68a-127">INPUTS</span></span>

### <span data-ttu-id="6d68a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6d68a-128">System.String</span></span>

## <span data-ttu-id="6d68a-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6d68a-129">OUTPUTS</span></span>

### <span data-ttu-id="6d68a-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d68a-130">System.Boolean</span></span>

## <span data-ttu-id="6d68a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6d68a-131">NOTES</span></span>
* <span data-ttu-id="6d68a-132">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="6d68a-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="6d68a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d68a-133">RELATED LINKS</span></span>

[<span data-ttu-id="6d68a-134">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d68a-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6d68a-135">New-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="6d68a-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="6d68a-136">New-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="6d68a-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


