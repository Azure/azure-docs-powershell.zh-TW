---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 1d5f230070f8b8c269137e07b04af970f314d564
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910925"
---
# <span data-ttu-id="647bb-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="647bb-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="647bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="647bb-102">SYNOPSIS</span></span>
<span data-ttu-id="647bb-103">取得 Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="647bb-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="647bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="647bb-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="647bb-105">描述</span><span class="sxs-lookup"><span data-stu-id="647bb-105">DESCRIPTION</span></span>
<span data-ttu-id="647bb-106">**Get-AzRedisCacheKey** Cmdlet 會取得 Azure Redis Cache 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="647bb-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="647bb-107">例子</span><span class="sxs-lookup"><span data-stu-id="647bb-107">EXAMPLES</span></span>

### <span data-ttu-id="647bb-108">範例 1：取得 Redis Cache 的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="647bb-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="647bb-109">此命令會取得名為 MyCacheKey 的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="647bb-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="647bb-110">參數</span><span class="sxs-lookup"><span data-stu-id="647bb-110">PARAMETERS</span></span>

### <span data-ttu-id="647bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="647bb-111">-DefaultProfile</span></span>
<span data-ttu-id="647bb-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="647bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="647bb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="647bb-113">-Name</span></span>
<span data-ttu-id="647bb-114">指定 Redis Cache 的名稱。</span><span class="sxs-lookup"><span data-stu-id="647bb-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="647bb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="647bb-115">-ResourceGroupName</span></span>
<span data-ttu-id="647bb-116">指定包含 Redis Cache 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="647bb-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="647bb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="647bb-117">CommonParameters</span></span>
<span data-ttu-id="647bb-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="647bb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="647bb-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="647bb-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="647bb-120">輸入</span><span class="sxs-lookup"><span data-stu-id="647bb-120">INPUTS</span></span>

### <span data-ttu-id="647bb-121">System.String</span><span class="sxs-lookup"><span data-stu-id="647bb-121">System.String</span></span>

## <span data-ttu-id="647bb-122">輸出</span><span class="sxs-lookup"><span data-stu-id="647bb-122">OUTPUTS</span></span>

### <span data-ttu-id="647bb-123">Microsoft.Azure.management.Redis.models.RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="647bb-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="647bb-124">筆記</span><span class="sxs-lookup"><span data-stu-id="647bb-124">NOTES</span></span>

## <span data-ttu-id="647bb-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="647bb-125">RELATED LINKS</span></span>

[<span data-ttu-id="647bb-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="647bb-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


