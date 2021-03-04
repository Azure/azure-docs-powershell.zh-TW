---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscachelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheLink.md
ms.openlocfilehash: 41a2172fffdbd83edc8ab72a4fe922d600362731
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907098"
---
# <span data-ttu-id="40ba0-101">New-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="40ba0-101">New-AzRedisCacheLink</span></span>

## <span data-ttu-id="40ba0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="40ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="40ba0-103">在兩個 Redis Caches 之間建立地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="40ba0-103">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="40ba0-104">語法</span><span class="sxs-lookup"><span data-stu-id="40ba0-104">SYNTAX</span></span>

```
New-AzRedisCacheLink -PrimaryServerName <String> -SecondaryServerName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40ba0-105">描述</span><span class="sxs-lookup"><span data-stu-id="40ba0-105">DESCRIPTION</span></span>
<span data-ttu-id="40ba0-106">在兩個 Redis Caches 之間建立地理位置複製連結。</span><span class="sxs-lookup"><span data-stu-id="40ba0-106">Create a geo replication link between two Redis Caches.</span></span>

## <span data-ttu-id="40ba0-107">例子</span><span class="sxs-lookup"><span data-stu-id="40ba0-107">EXAMPLES</span></span>

### <span data-ttu-id="40ba0-108">範例 1：在兩個緩存之間建立連結</span><span class="sxs-lookup"><span data-stu-id="40ba0-108">Example 1: Create a link between two caches</span></span>
```
PS C:\>New-AzRedisCacheLink -PrimaryServerName "mycache1" -SecondaryServerName "mycache2"

        PrimaryServerName   : mycache1
        SecondaryServerName : mycache2
        ProvisioningState   : Creating
```

<span data-ttu-id="40ba0-109">此命令會建立 Redis Cache mycache1 和 mycache2 之間的異地複製連結。</span><span class="sxs-lookup"><span data-stu-id="40ba0-109">This command creates geo-replication link between Redis Cache mycache1 and mycache2.</span></span>

## <span data-ttu-id="40ba0-110">參數</span><span class="sxs-lookup"><span data-stu-id="40ba0-110">PARAMETERS</span></span>

### <span data-ttu-id="40ba0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ba0-111">-DefaultProfile</span></span>
<span data-ttu-id="40ba0-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="40ba0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40ba0-113">-PrimaryServerName</span><span class="sxs-lookup"><span data-stu-id="40ba0-113">-PrimaryServerName</span></span>
<span data-ttu-id="40ba0-114">連結中主要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="40ba0-114">Name of primary redis cache in link.</span></span>

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

### <span data-ttu-id="40ba0-115">-SecondaryServerName</span><span class="sxs-lookup"><span data-stu-id="40ba0-115">-SecondaryServerName</span></span>
<span data-ttu-id="40ba0-116">連結中次要重新顯示緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="40ba0-116">Name of secondary redis cache in link.</span></span>

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

### <span data-ttu-id="40ba0-117">-確認</span><span class="sxs-lookup"><span data-stu-id="40ba0-117">-Confirm</span></span>
<span data-ttu-id="40ba0-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="40ba0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40ba0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ba0-119">-WhatIf</span></span>
<span data-ttu-id="40ba0-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40ba0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40ba0-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40ba0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40ba0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ba0-122">CommonParameters</span></span>
<span data-ttu-id="40ba0-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="40ba0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ba0-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="40ba0-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ba0-125">輸入</span><span class="sxs-lookup"><span data-stu-id="40ba0-125">INPUTS</span></span>

### <span data-ttu-id="40ba0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="40ba0-126">System.String</span></span>

## <span data-ttu-id="40ba0-127">輸出</span><span class="sxs-lookup"><span data-stu-id="40ba0-127">OUTPUTS</span></span>

### <span data-ttu-id="40ba0-128">Microsoft.Azure.Commands.RedisCache.models.PSRedisLinkedServer</span><span class="sxs-lookup"><span data-stu-id="40ba0-128">Microsoft.Azure.Commands.RedisCache.Models.PSRedisLinkedServer</span></span>

## <span data-ttu-id="40ba0-129">筆記</span><span class="sxs-lookup"><span data-stu-id="40ba0-129">NOTES</span></span>

## <span data-ttu-id="40ba0-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="40ba0-130">RELATED LINKS</span></span>

[<span data-ttu-id="40ba0-131">Get-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="40ba0-131">Get-AzRedisCacheLink</span></span>](./Get-AzRedisCacheLink.md)

[<span data-ttu-id="40ba0-132">Remove-AzRedisCacheLink</span><span class="sxs-lookup"><span data-stu-id="40ba0-132">Remove-AzRedisCacheLink</span></span>](./Remove-AzRedisCacheLink.md)

[<span data-ttu-id="40ba0-133">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="40ba0-133">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="40ba0-134">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="40ba0-134">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="40ba0-135">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="40ba0-135">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="40ba0-136">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="40ba0-136">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)