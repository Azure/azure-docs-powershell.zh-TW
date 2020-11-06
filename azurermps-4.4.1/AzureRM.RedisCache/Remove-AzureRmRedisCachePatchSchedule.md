---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446685"
---
# <span data-ttu-id="1ba43-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1ba43-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="1ba43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ba43-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba43-103">移除 [修補程式排程]。</span><span class="sxs-lookup"><span data-stu-id="1ba43-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ba43-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ba43-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ba43-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ba43-105">DESCRIPTION</span></span>
<span data-ttu-id="1ba43-106">AzureRmRedisCachePatchSchedule Cmdlet 會從 Azure Redis Cache 中的快 **取** 中移除修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="1ba43-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="1ba43-107">示例</span><span class="sxs-lookup"><span data-stu-id="1ba43-107">EXAMPLES</span></span>

### <span data-ttu-id="1ba43-108">範例1：移除修補程式排程</span><span class="sxs-lookup"><span data-stu-id="1ba43-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="1ba43-109">這個命令會從快取中移除名為 RedisCache06 的修補程式排程。</span><span class="sxs-lookup"><span data-stu-id="1ba43-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="1ba43-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ba43-110">PARAMETERS</span></span>

### <span data-ttu-id="1ba43-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ba43-111">-Name</span></span>
<span data-ttu-id="1ba43-112">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba43-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1ba43-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ba43-113">-ResourceGroupName</span></span>
<span data-ttu-id="1ba43-114">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ba43-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="1ba43-115">-確認</span><span class="sxs-lookup"><span data-stu-id="1ba43-115">-Confirm</span></span>
<span data-ttu-id="1ba43-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ba43-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ba43-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ba43-117">-WhatIf</span></span>
<span data-ttu-id="1ba43-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ba43-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ba43-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ba43-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ba43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba43-120">-DefaultProfile</span></span>
<span data-ttu-id="1ba43-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ba43-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ba43-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba43-122">CommonParameters</span></span>
<span data-ttu-id="1ba43-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ba43-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba43-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ba43-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba43-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1ba43-125">INPUTS</span></span>

### <span data-ttu-id="1ba43-126">所有</span><span class="sxs-lookup"><span data-stu-id="1ba43-126">None</span></span>
<span data-ttu-id="1ba43-127">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ba43-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1ba43-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1ba43-128">OUTPUTS</span></span>

### <span data-ttu-id="1ba43-129">所有</span><span class="sxs-lookup"><span data-stu-id="1ba43-129">None</span></span>

## <span data-ttu-id="1ba43-130">筆記</span><span class="sxs-lookup"><span data-stu-id="1ba43-130">NOTES</span></span>
* <span data-ttu-id="1ba43-131">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="1ba43-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1ba43-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ba43-132">RELATED LINKS</span></span>

[<span data-ttu-id="1ba43-133">AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1ba43-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1ba43-134">新-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1ba43-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1ba43-135">新-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1ba43-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


