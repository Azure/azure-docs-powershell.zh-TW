---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957259"
---
# <span data-ttu-id="1e742-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1e742-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="1e742-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1e742-102">SYNOPSIS</span></span>
<span data-ttu-id="1e742-103">再生 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1e742-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="1e742-104">句法</span><span class="sxs-lookup"><span data-stu-id="1e742-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e742-105">說明</span><span class="sxs-lookup"><span data-stu-id="1e742-105">DESCRIPTION</span></span>
<span data-ttu-id="1e742-106">**新的-AzRedisCacheKey** Cmdlet 會再生 Azure Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1e742-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="1e742-107">示例</span><span class="sxs-lookup"><span data-stu-id="1e742-107">EXAMPLES</span></span>

### <span data-ttu-id="1e742-108">範例1：重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="1e742-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1e742-109">這個命令會再生 Redis 快取的主鍵。</span><span class="sxs-lookup"><span data-stu-id="1e742-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="1e742-110">範例2：重新產生次要金鑰</span><span class="sxs-lookup"><span data-stu-id="1e742-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1e742-111">這個命令會重新產生 Redis 快取的輔助鍵。</span><span class="sxs-lookup"><span data-stu-id="1e742-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="1e742-112">參數</span><span class="sxs-lookup"><span data-stu-id="1e742-112">PARAMETERS</span></span>

### <span data-ttu-id="1e742-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e742-113">-DefaultProfile</span></span>
<span data-ttu-id="1e742-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1e742-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e742-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1e742-115">-Force</span></span>
<span data-ttu-id="1e742-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1e742-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e742-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1e742-117">-KeyType</span></span>
<span data-ttu-id="1e742-118">指定是否要重新產生主要或次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="1e742-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="1e742-119">有效值為：主要、次要。</span><span class="sxs-lookup"><span data-stu-id="1e742-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e742-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="1e742-120">-Name</span></span>
<span data-ttu-id="1e742-121">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e742-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="1e742-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e742-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e742-123">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1e742-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1e742-124">-確認</span><span class="sxs-lookup"><span data-stu-id="1e742-124">-Confirm</span></span>
<span data-ttu-id="1e742-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1e742-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e742-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e742-126">-WhatIf</span></span>
<span data-ttu-id="1e742-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1e742-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e742-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1e742-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e742-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e742-129">CommonParameters</span></span>
<span data-ttu-id="1e742-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1e742-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e742-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1e742-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e742-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1e742-132">INPUTS</span></span>

### <span data-ttu-id="1e742-133">System.object</span><span class="sxs-lookup"><span data-stu-id="1e742-133">System.String</span></span>

## <span data-ttu-id="1e742-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1e742-134">OUTPUTS</span></span>

### <span data-ttu-id="1e742-135">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="1e742-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="1e742-136">筆記</span><span class="sxs-lookup"><span data-stu-id="1e742-136">NOTES</span></span>

## <span data-ttu-id="1e742-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="1e742-137">RELATED LINKS</span></span>

[<span data-ttu-id="1e742-138">AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1e742-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)

