---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286659"
---
# <span data-ttu-id="45393-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="45393-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="45393-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45393-102">SYNOPSIS</span></span>
<span data-ttu-id="45393-103">取得 Redis 快取的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="45393-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="45393-104">句法</span><span class="sxs-lookup"><span data-stu-id="45393-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45393-105">說明</span><span class="sxs-lookup"><span data-stu-id="45393-105">DESCRIPTION</span></span>
<span data-ttu-id="45393-106">**AzRedisCacheKey** Cmdlet 會取得 Azure Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="45393-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="45393-107">示例</span><span class="sxs-lookup"><span data-stu-id="45393-107">EXAMPLES</span></span>

### <span data-ttu-id="45393-108">範例1：取得 Redis 快取的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="45393-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="45393-109">這個命令會取得名為 MyCacheKey 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="45393-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="45393-110">參數</span><span class="sxs-lookup"><span data-stu-id="45393-110">PARAMETERS</span></span>

### <span data-ttu-id="45393-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45393-111">-DefaultProfile</span></span>
<span data-ttu-id="45393-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45393-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45393-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="45393-113">-Name</span></span>
<span data-ttu-id="45393-114">指定 Redis 快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="45393-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="45393-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45393-115">-ResourceGroupName</span></span>
<span data-ttu-id="45393-116">指定包含 Redis 快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45393-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="45393-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45393-117">CommonParameters</span></span>
<span data-ttu-id="45393-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45393-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45393-119">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45393-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45393-120">輸入</span><span class="sxs-lookup"><span data-stu-id="45393-120">INPUTS</span></span>

### <span data-ttu-id="45393-121">System.object</span><span class="sxs-lookup"><span data-stu-id="45393-121">System.String</span></span>

## <span data-ttu-id="45393-122">輸出</span><span class="sxs-lookup"><span data-stu-id="45393-122">OUTPUTS</span></span>

### <span data-ttu-id="45393-123">RedisAccessKeys 中的 Redis。</span><span class="sxs-lookup"><span data-stu-id="45393-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="45393-124">筆記</span><span class="sxs-lookup"><span data-stu-id="45393-124">NOTES</span></span>

## <span data-ttu-id="45393-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="45393-125">RELATED LINKS</span></span>

[<span data-ttu-id="45393-126">新-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="45393-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


