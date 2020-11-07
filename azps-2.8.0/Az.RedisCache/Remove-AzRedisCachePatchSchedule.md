---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 83fab07a44dd85e000e86597881341cad6c641e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791394"
---
# <span data-ttu-id="a6b52-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6b52-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="a6b52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6b52-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b52-103">移除 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="a6b52-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="a6b52-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6b52-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6b52-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6b52-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b52-106">AzRedisCachePatchSchedule Cmdlet 會從 Azure Redis Cache 中的快 **取** 中移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="a6b52-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="a6b52-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6b52-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b52-108">範例1：移除修補程式排程</span><span class="sxs-lookup"><span data-stu-id="a6b52-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="a6b52-109">這個命令會從快取中移除名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="a6b52-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="a6b52-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6b52-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b52-111">-DefaultProfile</span></span>
<span data-ttu-id="a6b52-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6b52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6b52-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6b52-113">-Name</span></span>
<span data-ttu-id="a6b52-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b52-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a6b52-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6b52-115">-PassThru</span></span>
<span data-ttu-id="a6b52-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="a6b52-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a6b52-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6b52-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6b52-118">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b52-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="a6b52-119">-確認</span><span class="sxs-lookup"><span data-stu-id="a6b52-119">-Confirm</span></span>
<span data-ttu-id="a6b52-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6b52-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6b52-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6b52-121">-WhatIf</span></span>
<span data-ttu-id="a6b52-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6b52-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6b52-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6b52-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6b52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b52-124">CommonParameters</span></span>
<span data-ttu-id="a6b52-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6b52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b52-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6b52-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b52-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b52-127">INPUTS</span></span>

### <span data-ttu-id="a6b52-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b52-128">System.String</span></span>

## <span data-ttu-id="a6b52-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b52-129">OUTPUTS</span></span>

### <span data-ttu-id="a6b52-130">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b52-130">System.Boolean</span></span>

## <span data-ttu-id="a6b52-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b52-131">NOTES</span></span>
* <span data-ttu-id="a6b52-132">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="a6b52-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a6b52-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b52-133">RELATED LINKS</span></span>

[<span data-ttu-id="a6b52-134">AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6b52-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a6b52-135">新-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="a6b52-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="a6b52-136">新-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="a6b52-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


