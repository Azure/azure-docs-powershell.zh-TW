---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279867"
---
# <span data-ttu-id="0492a-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0492a-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="0492a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0492a-102">SYNOPSIS</span></span>
<span data-ttu-id="0492a-103">取得 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0492a-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="0492a-104">句法</span><span class="sxs-lookup"><span data-stu-id="0492a-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0492a-105">說明</span><span class="sxs-lookup"><span data-stu-id="0492a-105">DESCRIPTION</span></span>
<span data-ttu-id="0492a-106">**AzRedisCacheKey** Cmdlet 會取得 Azure Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0492a-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="0492a-107">示例</span><span class="sxs-lookup"><span data-stu-id="0492a-107">EXAMPLES</span></span>

### <span data-ttu-id="0492a-108">範例1：取得 Redis 快取的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="0492a-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="0492a-109">這個命令會取得名為 MyCacheKey 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0492a-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="0492a-110">參數</span><span class="sxs-lookup"><span data-stu-id="0492a-110">PARAMETERS</span></span>

### <span data-ttu-id="0492a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0492a-111">-DefaultProfile</span></span>
<span data-ttu-id="0492a-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0492a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0492a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0492a-113">-Name</span></span>
<span data-ttu-id="0492a-114">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="0492a-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="0492a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0492a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0492a-116">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0492a-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="0492a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0492a-117">CommonParameters</span></span>
<span data-ttu-id="0492a-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0492a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0492a-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0492a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0492a-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0492a-120">INPUTS</span></span>

### <span data-ttu-id="0492a-121">System.object</span><span class="sxs-lookup"><span data-stu-id="0492a-121">System.String</span></span>

## <span data-ttu-id="0492a-122">輸出</span><span class="sxs-lookup"><span data-stu-id="0492a-122">OUTPUTS</span></span>

### <span data-ttu-id="0492a-123">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="0492a-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="0492a-124">筆記</span><span class="sxs-lookup"><span data-stu-id="0492a-124">NOTES</span></span>

## <span data-ttu-id="0492a-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="0492a-125">RELATED LINKS</span></span>

[<span data-ttu-id="0492a-126">新-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="0492a-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


