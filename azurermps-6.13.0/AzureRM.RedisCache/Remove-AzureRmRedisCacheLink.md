---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheLink.md
ms.openlocfilehash: e4c45095dba8ec72e00fa26eee2d8a3fb6f029fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625570"
---
# <span data-ttu-id="fa4d9-101">Remove-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fa4d9-101">Remove-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="fa4d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4d9-103">在兩個 Redis 緩存間移除地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-103">Remove a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa4d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa4d9-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa4d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4d9-106">在兩個 Redis 緩存間移除地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="fa4d9-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fa4d9-108">範例1：移除地域複製連結</span><span class="sxs-lookup"><span data-stu-id="fa4d9-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="fa4d9-109">這個命令會移除名為 mycache1 的 Redis 快取的地理複製連結，而名為 mycache2 的 Redis 快取是次要的。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="fa4d9-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa4d9-110">PARAMETERS</span></span>

### <span data-ttu-id="fa4d9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4d9-111">-DefaultProfile</span></span>
<span data-ttu-id="fa4d9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa4d9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa4d9-113">-PassThru</span></span>
<span data-ttu-id="fa4d9-114">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="fa4d9-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fa4d9-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="fa4d9-115">-PrimaryServerName</span></span>
<span data-ttu-id="fa4d9-116">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="fa4d9-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="fa4d9-117">-SecondaryServerName</span></span>
<span data-ttu-id="fa4d9-118">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="fa4d9-119">-確認</span><span class="sxs-lookup"><span data-stu-id="fa4d9-119">-Confirm</span></span>
<span data-ttu-id="fa4d9-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4d9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4d9-121">-WhatIf</span></span>
<span data-ttu-id="fa4d9-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4d9-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa4d9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4d9-124">CommonParameters</span></span>
<span data-ttu-id="fa4d9-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4d9-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa4d9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4d9-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fa4d9-127">INPUTS</span></span>

### <span data-ttu-id="fa4d9-128">System.object</span><span class="sxs-lookup"><span data-stu-id="fa4d9-128">System.String</span></span>

## <span data-ttu-id="fa4d9-129">輸出</span><span class="sxs-lookup"><span data-stu-id="fa4d9-129">OUTPUTS</span></span>

### <span data-ttu-id="fa4d9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fa4d9-130">System.Boolean</span></span>

## <span data-ttu-id="fa4d9-131">筆記</span><span class="sxs-lookup"><span data-stu-id="fa4d9-131">NOTES</span></span>

## <span data-ttu-id="fa4d9-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa4d9-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa4d9-133">新-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fa4d9-133">New-AzureRmRedisCacheLink</span></span>](./New-AzureRmRedisCacheLink.md)

[<span data-ttu-id="fa4d9-134">AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="fa4d9-134">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="fa4d9-135">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fa4d9-135">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="fa4d9-136">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fa4d9-136">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="fa4d9-137">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fa4d9-137">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="fa4d9-138">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="fa4d9-138">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
