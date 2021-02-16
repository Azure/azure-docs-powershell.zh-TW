---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: d27f3ece14e18465fc534bff1a3451eaec2c40a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141926"
---
# <span data-ttu-id="ac1eb-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ac1eb-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="ac1eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1eb-103">在兩個 Redis 緩存之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ac1eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac1eb-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac1eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="ac1eb-106">在兩個 Redis 緩存之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="ac1eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="ac1eb-108">範例1：建立兩個快取記憶體之間的連結</span><span class="sxs-lookup"><span data-stu-id="ac1eb-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="ac1eb-109">這個命令會在 Redis Cache mycache1 和 mycache2 之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="ac1eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac1eb-110">PARAMETERS</span></span>

### <span data-ttu-id="ac1eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1eb-111">-DefaultProfile</span></span>
<span data-ttu-id="ac1eb-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac1eb-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="ac1eb-113">-PrimaryServerName</span></span>
<span data-ttu-id="ac1eb-114">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="ac1eb-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="ac1eb-115">-SecondaryServerName</span></span>
<span data-ttu-id="ac1eb-116">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="ac1eb-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ac1eb-117">-Confirm</span></span>
<span data-ttu-id="ac1eb-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac1eb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac1eb-119">-WhatIf</span></span>
<span data-ttu-id="ac1eb-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac1eb-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac1eb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1eb-122">CommonParameters</span></span>
<span data-ttu-id="ac1eb-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1eb-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1eb-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ac1eb-125">INPUTS</span></span>

### <span data-ttu-id="ac1eb-126">System.object</span><span class="sxs-lookup"><span data-stu-id="ac1eb-126">System.String</span></span>

## <span data-ttu-id="ac1eb-127">輸出</span><span class="sxs-lookup"><span data-stu-id="ac1eb-127">OUTPUTS</span></span>

### <span data-ttu-id="ac1eb-128">PSRedisLinkedServer 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="ac1eb-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="ac1eb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="ac1eb-129">NOTES</span></span>

## <span data-ttu-id="ac1eb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac1eb-130">RELATED LINKS</span></span>

[<span data-ttu-id="ac1eb-131">AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ac1eb-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="ac1eb-132">移除-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="ac1eb-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="ac1eb-133">AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac1eb-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ac1eb-134">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac1eb-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ac1eb-135">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac1eb-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ac1eb-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ac1eb-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)