---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheLink.md
ms.openlocfilehash: dd9e070a0228cf9bc492f8680917ae0f308e9019
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625002"
---
# <span data-ttu-id="62a7a-101">New-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="62a7a-101">New-AzureRmRedisCacheLink</span></span>

## <span data-ttu-id="62a7a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62a7a-102">SYNOPSIS</span></span>
<span data-ttu-id="62a7a-103">在兩個 Redis 緩存之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="62a7a-103">Create a geo replication link between two Redis Caches.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a7a-104">句法</span><span class="sxs-lookup"><span data-stu-id="62a7a-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a7a-105">說明</span><span class="sxs-lookup"><span data-stu-id="62a7a-105">DESCRIPTION</span></span>
<span data-ttu-id="62a7a-106">在兩個 Redis 緩存之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="62a7a-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="62a7a-107">示例</span><span class="sxs-lookup"><span data-stu-id="62a7a-107">EXAMPLES</span></span>

### <span data-ttu-id="62a7a-108">範例1：建立兩個快取記憶體之間的連結</span><span class="sxs-lookup"><span data-stu-id="62a7a-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzureRmRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="62a7a-109">這個命令會在 Redis Cache mycache1 和 mycache2 之間建立地理複製連結。</span><span class="sxs-lookup"><span data-stu-id="62a7a-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="62a7a-110">參數</span><span class="sxs-lookup"><span data-stu-id="62a7a-110">PARAMETERS</span></span>

### <span data-ttu-id="62a7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a7a-111">-DefaultProfile</span></span>
<span data-ttu-id="62a7a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62a7a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62a7a-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="62a7a-113">-PrimaryServerName</span></span>
<span data-ttu-id="62a7a-114">連結中主要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="62a7a-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="62a7a-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="62a7a-115">-SecondaryServerName</span></span>
<span data-ttu-id="62a7a-116">連結中次要 redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="62a7a-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="62a7a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="62a7a-117">-Confirm</span></span>
<span data-ttu-id="62a7a-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="62a7a-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a7a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a7a-119">-WhatIf</span></span>
<span data-ttu-id="62a7a-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="62a7a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a7a-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="62a7a-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a7a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a7a-122">CommonParameters</span></span>
<span data-ttu-id="62a7a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62a7a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a7a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62a7a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a7a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="62a7a-125">INPUTS</span></span>

### <span data-ttu-id="62a7a-126">System.object</span><span class="sxs-lookup"><span data-stu-id="62a7a-126">System.String</span></span>

## <span data-ttu-id="62a7a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="62a7a-127">OUTPUTS</span></span>

### <span data-ttu-id="62a7a-128">PSRedisLinkedServer 中的 RedisCache。</span><span class="sxs-lookup"><span data-stu-id="62a7a-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="62a7a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="62a7a-129">NOTES</span></span>

## <span data-ttu-id="62a7a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="62a7a-130">RELATED LINKS</span></span>

[<span data-ttu-id="62a7a-131">AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="62a7a-131">Get-AzureRmRedisCacheLink</span></span>](./Get-AzureRmRedisCacheLink.md)

[<span data-ttu-id="62a7a-132">移除-AzureRmRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="62a7a-132">Remove-AzureRmRedisCacheLink</span></span>](./Remove-AzureRmRedisCacheLink.md)

[<span data-ttu-id="62a7a-133">AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="62a7a-133">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="62a7a-134">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="62a7a-134">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="62a7a-135">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="62a7a-135">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="62a7a-136">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="62a7a-136">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)
