---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 67ec6bdcce5121c2a80e1f76ea1081f249f15682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448597"
---
# <span data-ttu-id="9c93c-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9c93c-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="9c93c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c93c-102">SYNOPSIS</span></span>
<span data-ttu-id="9c93c-103">取得 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9c93c-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c93c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c93c-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c93c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c93c-105">DESCRIPTION</span></span>
<span data-ttu-id="9c93c-106">**AzureRmRedisCacheKey** Cmdlet 會取得 Azure Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9c93c-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="9c93c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9c93c-107">EXAMPLES</span></span>

### <span data-ttu-id="9c93c-108">範例1：取得 Redis 快取的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="9c93c-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="9c93c-109">這個命令會取得名為 MyCacheKey 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9c93c-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="9c93c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c93c-110">PARAMETERS</span></span>

### <span data-ttu-id="9c93c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c93c-111">-DefaultProfile</span></span>
<span data-ttu-id="9c93c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c93c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c93c-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c93c-113">-Name</span></span>
<span data-ttu-id="9c93c-114">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c93c-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="9c93c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c93c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9c93c-116">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c93c-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="9c93c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c93c-117">CommonParameters</span></span>
<span data-ttu-id="9c93c-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c93c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c93c-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c93c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c93c-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9c93c-120">INPUTS</span></span>

### <span data-ttu-id="9c93c-121">所有</span><span class="sxs-lookup"><span data-stu-id="9c93c-121">None</span></span>
<span data-ttu-id="9c93c-122">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c93c-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="9c93c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="9c93c-123">OUTPUTS</span></span>

### <span data-ttu-id="9c93c-124">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="9c93c-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="9c93c-125">這個 Cmdlet 會傳回 Redis 快取的主要和次要便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="9c93c-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="9c93c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9c93c-126">NOTES</span></span>

## <span data-ttu-id="9c93c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c93c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c93c-128">新-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9c93c-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


