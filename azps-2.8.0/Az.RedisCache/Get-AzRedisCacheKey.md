---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 96eed93e4020384b0c989a05f549aa21f5482493
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792300"
---
# <span data-ttu-id="5eda3-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="5eda3-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="5eda3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5eda3-102">SYNOPSIS</span></span>
<span data-ttu-id="5eda3-103">取得 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5eda3-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="5eda3-104">句法</span><span class="sxs-lookup"><span data-stu-id="5eda3-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5eda3-105">說明</span><span class="sxs-lookup"><span data-stu-id="5eda3-105">DESCRIPTION</span></span>
<span data-ttu-id="5eda3-106">**AzRedisCacheKey** Cmdlet 會取得 Azure Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5eda3-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="5eda3-107">示例</span><span class="sxs-lookup"><span data-stu-id="5eda3-107">EXAMPLES</span></span>

### <span data-ttu-id="5eda3-108">範例1：取得 Redis 快取的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="5eda3-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="5eda3-109">這個命令會取得名為 MyCacheKey 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="5eda3-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="5eda3-110">參數</span><span class="sxs-lookup"><span data-stu-id="5eda3-110">PARAMETERS</span></span>

### <span data-ttu-id="5eda3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eda3-111">-DefaultProfile</span></span>
<span data-ttu-id="5eda3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5eda3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eda3-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="5eda3-113">-Name</span></span>
<span data-ttu-id="5eda3-114">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="5eda3-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="5eda3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eda3-115">-ResourceGroupName</span></span>
<span data-ttu-id="5eda3-116">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5eda3-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="5eda3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eda3-117">CommonParameters</span></span>
<span data-ttu-id="5eda3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5eda3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eda3-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5eda3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eda3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5eda3-120">INPUTS</span></span>

### <span data-ttu-id="5eda3-121">System.object</span><span class="sxs-lookup"><span data-stu-id="5eda3-121">System.String</span></span>

## <span data-ttu-id="5eda3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="5eda3-122">OUTPUTS</span></span>

### <span data-ttu-id="5eda3-123">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="5eda3-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="5eda3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="5eda3-124">NOTES</span></span>

## <span data-ttu-id="5eda3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="5eda3-125">RELATED LINKS</span></span>

[<span data-ttu-id="5eda3-126">新-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="5eda3-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


