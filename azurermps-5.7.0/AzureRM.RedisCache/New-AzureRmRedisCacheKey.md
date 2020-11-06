---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444400"
---
# <span data-ttu-id="d6de9-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d6de9-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="d6de9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6de9-102">SYNOPSIS</span></span>
<span data-ttu-id="d6de9-103">再生 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d6de9-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6de9-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6de9-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6de9-105">說明</span><span class="sxs-lookup"><span data-stu-id="d6de9-105">DESCRIPTION</span></span>
<span data-ttu-id="d6de9-106">**新的-AzureRmRedisCacheKey** Cmdlet 會再生 Azure Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d6de9-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="d6de9-107">示例</span><span class="sxs-lookup"><span data-stu-id="d6de9-107">EXAMPLES</span></span>

### <span data-ttu-id="d6de9-108">範例1：重新產生主鍵</span><span class="sxs-lookup"><span data-stu-id="d6de9-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="d6de9-109">這個命令會再生 Redis 快取的主鍵。</span><span class="sxs-lookup"><span data-stu-id="d6de9-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="d6de9-110">範例2：重新產生次要金鑰</span><span class="sxs-lookup"><span data-stu-id="d6de9-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="d6de9-111">這個命令會重新產生 Redis 快取的輔助鍵。</span><span class="sxs-lookup"><span data-stu-id="d6de9-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="d6de9-112">參數</span><span class="sxs-lookup"><span data-stu-id="d6de9-112">PARAMETERS</span></span>

### <span data-ttu-id="d6de9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6de9-113">-DefaultProfile</span></span>
<span data-ttu-id="d6de9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6de9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6de9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d6de9-115">-Force</span></span>
<span data-ttu-id="d6de9-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d6de9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6de9-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="d6de9-117">-KeyType</span></span>
<span data-ttu-id="d6de9-118">指定是否要重新產生主要或次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="d6de9-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="d6de9-119">有效值為：主要、次要。</span><span class="sxs-lookup"><span data-stu-id="d6de9-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6de9-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6de9-120">-Name</span></span>
<span data-ttu-id="d6de9-121">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6de9-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="d6de9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6de9-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6de9-123">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6de9-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6de9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d6de9-124">-Confirm</span></span>
<span data-ttu-id="d6de9-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6de9-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6de9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6de9-126">-WhatIf</span></span>
<span data-ttu-id="d6de9-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6de9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6de9-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6de9-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6de9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6de9-129">CommonParameters</span></span>
<span data-ttu-id="d6de9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6de9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6de9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d6de9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6de9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d6de9-132">INPUTS</span></span>

### <span data-ttu-id="d6de9-133">所有</span><span class="sxs-lookup"><span data-stu-id="d6de9-133">None</span></span>
<span data-ttu-id="d6de9-134">您可以依名稱將輸入管到這個 Cmdlet，但不能依值進行。</span><span class="sxs-lookup"><span data-stu-id="d6de9-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="d6de9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d6de9-135">OUTPUTS</span></span>

### <span data-ttu-id="d6de9-136">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="d6de9-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="d6de9-137">這個 Cmdlet 會傳回 Redis 快取的主要和次要存取金鑰。</span><span class="sxs-lookup"><span data-stu-id="d6de9-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="d6de9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d6de9-138">NOTES</span></span>

## <span data-ttu-id="d6de9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6de9-139">RELATED LINKS</span></span>

[<span data-ttu-id="d6de9-140">AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="d6de9-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)

