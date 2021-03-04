---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheLink.md
ms.openlocfilehash: 2227f4fc9cd8128018160a3e62d9ba56bd664d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902194"
---
# <span data-ttu-id="90e4e-101">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="90e4e-101">Remove-AzRedisCacheLink</span></span>

## <span data-ttu-id="90e4e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="90e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="90e4e-103">移除兩個 Redis Cache 之間的地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="90e4e-103">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="90e4e-104">語法</span><span class="sxs-lookup"><span data-stu-id="90e4e-104">SYNTAX</span></span>

```
Remove-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e4e-105">描述</span><span class="sxs-lookup"><span data-stu-id="90e4e-105">DESCRIPTION</span></span>
<span data-ttu-id="90e4e-106">移除兩個 Redis Cache 之間的地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="90e4e-106">Remove a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="90e4e-107">例子</span><span class="sxs-lookup"><span data-stu-id="90e4e-107">EXAMPLES</span></span>

### <span data-ttu-id="90e4e-108">範例 1：移除異地複製連結</span><span class="sxs-lookup"><span data-stu-id="90e4e-108">Example 1: Remove a geo replication link</span></span>
```
PS C:\>Remove-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"
```

<span data-ttu-id="90e4e-109">此命令會移除名為 mycache1 的 Redis Cache 為主要且名稱為 mycache2 的 Redis Cache 為次要位置的地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="90e4e-109">This command removes a geo-replication links where Redis Cache named mycache1 is primary and Redis Cache named mycache2 is secondary.</span></span>

## <span data-ttu-id="90e4e-110">參數</span><span class="sxs-lookup"><span data-stu-id="90e4e-110">PARAMETERS</span></span>

### <span data-ttu-id="90e4e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e4e-111">-DefaultProfile</span></span>
<span data-ttu-id="90e4e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="90e4e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e4e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e4e-113">-PassThru</span></span>
<span data-ttu-id="90e4e-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="90e4e-114">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="90e4e-115">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="90e4e-115">-PrimaryServerName</span></span>
<span data-ttu-id="90e4e-116">連結中主要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e4e-116">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="90e4e-117">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="90e4e-117">-SecondaryServerName</span></span>
<span data-ttu-id="90e4e-118">連結中次要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e4e-118">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="90e4e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="90e4e-119">-Confirm</span></span>
<span data-ttu-id="90e4e-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="90e4e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e4e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e4e-121">-WhatIf</span></span>
<span data-ttu-id="90e4e-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="90e4e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e4e-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90e4e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e4e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e4e-124">CommonParameters</span></span>
<span data-ttu-id="90e4e-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="90e4e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e4e-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="90e4e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e4e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="90e4e-127">INPUTS</span></span>

### <span data-ttu-id="90e4e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="90e4e-128">System.String</span></span>

## <span data-ttu-id="90e4e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="90e4e-129">OUTPUTS</span></span>

### <span data-ttu-id="90e4e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="90e4e-130">System.Boolean</span></span>

## <span data-ttu-id="90e4e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="90e4e-131">NOTES</span></span>

## <span data-ttu-id="90e4e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="90e4e-132">RELATED LINKS</span></span>

[<span data-ttu-id="90e4e-133">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="90e4e-133">New-AzRedisCacheLink</span></span>](./New-AzRedisCacheLink.md)

[<span data-ttu-id="90e4e-134">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="90e4e-134">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="90e4e-135">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90e4e-135">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="90e4e-136">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90e4e-136">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="90e4e-137">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90e4e-137">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="90e4e-138">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="90e4e-138">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)