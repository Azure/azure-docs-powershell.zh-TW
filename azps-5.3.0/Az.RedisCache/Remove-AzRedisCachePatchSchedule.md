---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435603"
---
# <span data-ttu-id="8f5ed-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8f5ed-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="8f5ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5ed-103">移除 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="8f5ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f5ed-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="8f5ed-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5ed-106">AzRedisCachePatchSchedule Cmdlet 會從 Azure Redis Cache 中的快 **取** 中移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="8f5ed-107">示例</span><span class="sxs-lookup"><span data-stu-id="8f5ed-107">EXAMPLES</span></span>

### <span data-ttu-id="8f5ed-108">範例1：移除修補程式排程</span><span class="sxs-lookup"><span data-stu-id="8f5ed-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="8f5ed-109">這個命令會從快取中移除名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="8f5ed-110">參數</span><span class="sxs-lookup"><span data-stu-id="8f5ed-110">PARAMETERS</span></span>

### <span data-ttu-id="8f5ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5ed-111">-DefaultProfile</span></span>
<span data-ttu-id="8f5ed-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f5ed-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="8f5ed-113">-Name</span></span>
<span data-ttu-id="8f5ed-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="8f5ed-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f5ed-115">-PassThru</span></span>
<span data-ttu-id="8f5ed-116">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="8f5ed-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8f5ed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5ed-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f5ed-118">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="8f5ed-119">-確認</span><span class="sxs-lookup"><span data-stu-id="8f5ed-119">-Confirm</span></span>
<span data-ttu-id="8f5ed-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5ed-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5ed-121">-WhatIf</span></span>
<span data-ttu-id="8f5ed-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5ed-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5ed-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5ed-124">CommonParameters</span></span>
<span data-ttu-id="8f5ed-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5ed-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8f5ed-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5ed-127">輸入</span><span class="sxs-lookup"><span data-stu-id="8f5ed-127">INPUTS</span></span>

### <span data-ttu-id="8f5ed-128">System.object</span><span class="sxs-lookup"><span data-stu-id="8f5ed-128">System.String</span></span>

## <span data-ttu-id="8f5ed-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8f5ed-129">OUTPUTS</span></span>

### <span data-ttu-id="8f5ed-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8f5ed-130">System.Boolean</span></span>

## <span data-ttu-id="8f5ed-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8f5ed-131">NOTES</span></span>
* <span data-ttu-id="8f5ed-132">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="8f5ed-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="8f5ed-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f5ed-133">RELATED LINKS</span></span>

[<span data-ttu-id="8f5ed-134">AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8f5ed-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="8f5ed-135">新-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="8f5ed-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="8f5ed-136">新-AzRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="8f5ed-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


