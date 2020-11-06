---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: e4f4dd72104b4a57823c54e6cf56f531f48e610d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620978"
---
# <span data-ttu-id="08782-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08782-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="08782-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08782-102">SYNOPSIS</span></span>
<span data-ttu-id="08782-103">在兩個 Redis 緩存間移除地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="08782-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="08782-104">句法</span><span class="sxs-lookup"><span data-stu-id="08782-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08782-105">說明</span><span class="sxs-lookup"><span data-stu-id="08782-105">DESCRIPTION</span></span>
<span data-ttu-id="08782-106">在兩個 Redis 緩存間移除地域複製連結。</span><span class="sxs-lookup"><span data-stu-id="08782-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="08782-107">示例</span><span class="sxs-lookup"><span data-stu-id="08782-107">EXAMPLES</span></span>

### <span data-ttu-id="08782-108">範例1：移除地域複製連結</span><span class="sxs-lookup"><span data-stu-id="08782-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="08782-109">這個命令會移除名為 mycache1 的 Redis 快取的地理複製連結，而名為 mycache2 的 Redis 快取是次要的。</span><span class="sxs-lookup"><span data-stu-id="08782-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="08782-110">參數</span><span class="sxs-lookup"><span data-stu-id="08782-110">PARAMETERS</span></span>

### <span data-ttu-id="08782-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08782-111">-DefaultProfile</span></span>
<span data-ttu-id="08782-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="08782-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08782-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08782-113">-PassThru</span></span>
<span data-ttu-id="08782-114">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="08782-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="08782-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="08782-115">-PrimaryServerName</span></span>
<span data-ttu-id="08782-116">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="08782-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="08782-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="08782-117">-SecondaryServerName</span></span>
<span data-ttu-id="08782-118">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="08782-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="08782-119">-確認</span><span class="sxs-lookup"><span data-stu-id="08782-119">-Confirm</span></span>
<span data-ttu-id="08782-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="08782-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08782-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08782-121">-WhatIf</span></span>
<span data-ttu-id="08782-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="08782-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08782-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08782-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08782-124">CommonParameters</span></span>
<span data-ttu-id="08782-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08782-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08782-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08782-127">輸入</span><span class="sxs-lookup"><span data-stu-id="08782-127">INPUTS</span></span>

### <span data-ttu-id="08782-128">System.object</span><span class="sxs-lookup"><span data-stu-id="08782-128">System.String</span></span>

## <span data-ttu-id="08782-129">輸出</span><span class="sxs-lookup"><span data-stu-id="08782-129">OUTPUTS</span></span>

### <span data-ttu-id="08782-130">System.object</span><span class="sxs-lookup"><span data-stu-id="08782-130">System.Boolean</span></span>

## <span data-ttu-id="08782-131">筆記</span><span class="sxs-lookup"><span data-stu-id="08782-131">NOTES</span></span>

## <span data-ttu-id="08782-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="08782-132">RELATED LINKS</span></span>

[<span data-ttu-id="08782-133">新-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08782-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="08782-134">AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="08782-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="08782-135">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08782-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="08782-136">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08782-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="08782-137">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08782-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="08782-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="08782-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)