---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/get-azredisenterprisecacheoperationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Get-AzRedisEnterpriseCacheOperationStatus.md
ms.openlocfilehash: 8416c18ac945eaab5ae9dbd758d2660c4f950417
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286652"
---
# <span data-ttu-id="5a13a-101">Get-AzRedisEnterpriseCacheOperationStatus</span><span class="sxs-lookup"><span data-stu-id="5a13a-101">Get-AzRedisEnterpriseCacheOperationStatus</span></span>

## <span data-ttu-id="5a13a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a13a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a13a-103">取得操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a13a-103">Gets the status of operation.</span></span>

## <span data-ttu-id="5a13a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a13a-104">SYNTAX</span></span>

```
Get-AzRedisEnterpriseCacheOperationStatus -Location <String> -OperationId <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5a13a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a13a-105">DESCRIPTION</span></span>
<span data-ttu-id="5a13a-106">取得操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a13a-106">Gets the status of operation.</span></span>

## <span data-ttu-id="5a13a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a13a-107">EXAMPLES</span></span>

### <span data-ttu-id="5a13a-108">範例1：取得操作狀態</span><span class="sxs-lookup"><span data-stu-id="5a13a-108">Example 1: Get operation status</span></span>
```powershell
PS C:\> Get-AzRedisEnterpriseCacheOperationStatus -Location "East US" -OperationId "6432a8f9-0fe6-4339-9303-772c92f35d02"

EndTime                           Name                                 StartTime                         Status
-------                           ----                                 ---------                         ------
2020-12-01T00:12:45.7107366+00:00 6432a8f9-0fe6-4339-9303-772c92f35d02 2020-12-01T00:04:35.7061294+00:00 Succeeded

```

<span data-ttu-id="5a13a-109">這個命令會取得操作的狀態。</span><span class="sxs-lookup"><span data-stu-id="5a13a-109">This command gets the status of an operation.</span></span>

## <span data-ttu-id="5a13a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a13a-110">PARAMETERS</span></span>

### <span data-ttu-id="5a13a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a13a-111">-DefaultProfile</span></span>
<span data-ttu-id="5a13a-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a13a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a13a-113">-位置</span><span class="sxs-lookup"><span data-stu-id="5a13a-113">-Location</span></span>
<span data-ttu-id="5a13a-114">操作所在的地區。</span><span class="sxs-lookup"><span data-stu-id="5a13a-114">The region the operation is in.</span></span>

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

### <span data-ttu-id="5a13a-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="5a13a-115">-OperationId</span></span>
<span data-ttu-id="5a13a-116">操作的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a13a-116">The operation's unique identifier.</span></span>

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

### <span data-ttu-id="5a13a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a13a-117">-SubscriptionId</span></span>
<span data-ttu-id="5a13a-118">取得可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="5a13a-118">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="5a13a-119">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="5a13a-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5a13a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a13a-120">CommonParameters</span></span>
<span data-ttu-id="5a13a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a13a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a13a-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a13a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a13a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="5a13a-123">INPUTS</span></span>

## <span data-ttu-id="5a13a-124">輸出</span><span class="sxs-lookup"><span data-stu-id="5a13a-124">OUTPUTS</span></span>

### <span data-ttu-id="5a13a-125">IOperationStatus （RedisEnterpriseCache）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="5a13a-125">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IOperationStatus</span></span>

## <span data-ttu-id="5a13a-126">筆記</span><span class="sxs-lookup"><span data-stu-id="5a13a-126">NOTES</span></span>

<span data-ttu-id="5a13a-127">別名</span><span class="sxs-lookup"><span data-stu-id="5a13a-127">ALIASES</span></span>

## <span data-ttu-id="5a13a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a13a-128">RELATED LINKS</span></span>

