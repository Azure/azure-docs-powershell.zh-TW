---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: fd2662af291b8c5c3372f27a3de89f7e18bfd35e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914650"
---
# <span data-ttu-id="fa5f4-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="fa5f4-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="fa5f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fa5f4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5f4-103">獲得作業狀態。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-103">Gets the status of operation.</span></span>

## <span data-ttu-id="fa5f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="fa5f4-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fa5f4-105">描述</span><span class="sxs-lookup"><span data-stu-id="fa5f4-105">DESCRIPTION</span></span>
<span data-ttu-id="fa5f4-106">獲得作業狀態。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-106">Gets the status of operation.</span></span>

## <span data-ttu-id="fa5f4-107">例子</span><span class="sxs-lookup"><span data-stu-id="fa5f4-107">EXAMPLES</span></span>

### <span data-ttu-id="fa5f4-108">範例 1：取得作業狀態</span><span class="sxs-lookup"><span data-stu-id="fa5f4-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="fa5f4-109">此命令會獲得作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="fa5f4-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa5f4-110">PARAMETERS</span></span>

### <span data-ttu-id="fa5f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5f4-111">-DefaultProfile</span></span>
<span data-ttu-id="fa5f4-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5f4-113">-位置</span><span class="sxs-lookup"><span data-stu-id="fa5f4-113">-Location</span></span>
<span data-ttu-id="fa5f4-114">作業的地區。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-114">The region the operation is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5f4-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="fa5f4-115">-OperationId</span></span>
<span data-ttu-id="fa5f4-116">作業的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-116">The operation's unique identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5f4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa5f4-117">-SubscriptionId</span></span>
<span data-ttu-id="fa5f4-118">獲得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa5f4-119">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5f4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5f4-120">CommonParameters</span></span>
<span data-ttu-id="fa5f4-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fa5f4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5f4-122">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa5f4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5f4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="fa5f4-123">INPUTS</span></span>

## <span data-ttu-id="fa5f4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="fa5f4-124">OUTPUTS</span></span>

### <span data-ttu-id="fa5f4-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.models.Api20201001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="fa5f4-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="fa5f4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="fa5f4-126">NOTES</span></span>

<span data-ttu-id="fa5f4-127">別名</span><span class="sxs-lookup"><span data-stu-id="fa5f4-127">ALIASES</span></span>

## <span data-ttu-id="fa5f4-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa5f4-128">RELATED LINKS</span></span>

