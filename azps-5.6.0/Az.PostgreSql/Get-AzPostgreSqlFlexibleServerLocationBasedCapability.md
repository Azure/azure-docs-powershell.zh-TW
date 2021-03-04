---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/get-azpostgresqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: efe45da6cd5426fda3b301efd4daf2ef532e4c02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902357"
---
# <span data-ttu-id="362f1-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="362f1-101">Get-AzPostgreSqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="362f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="362f1-102">SYNOPSIS</span></span>
<span data-ttu-id="362f1-103">取得位置的可用 SKU 資訊</span><span class="sxs-lookup"><span data-stu-id="362f1-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="362f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="362f1-104">SYNTAX</span></span>

```
Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="362f1-105">描述</span><span class="sxs-lookup"><span data-stu-id="362f1-105">DESCRIPTION</span></span>
<span data-ttu-id="362f1-106">取得位置的可用 SKU 資訊</span><span class="sxs-lookup"><span data-stu-id="362f1-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="362f1-107">例子</span><span class="sxs-lookup"><span data-stu-id="362f1-107">EXAMPLES</span></span>

### <span data-ttu-id="362f1-108">範例 1：根據位置名稱取得位置功能</span><span class="sxs-lookup"><span data-stu-id="362f1-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFlexibleServerLocationBasedCapability -Location eastus

SKU              Tier            Memory vCore
---              ----            ------ -----
Standard_B1ms    Burstable         2048     1
Standard_B2s     Burstable         2048     2
Standard_D2s_v3  GeneralPurpose    4096     2
Standard_D4s_v3  GeneralPurpose    4096     4
Standard_D8s_v3  GeneralPurpose    4096     8
Standard_D16s_v3 GeneralPurpose    4096    16
Standard_D32s_v3 GeneralPurpose    4096    32
Standard_D48s_v3 GeneralPurpose    4096    48
Standard_D64s_v3 GeneralPurpose    4096    64
Standard_E2s_v3  MemoryOptimized   8192     2
Standard_E4s_v3  MemoryOptimized   8192     4
Standard_E8s_v3  MemoryOptimized   8192     8
Standard_E16s_v3 MemoryOptimized   8192    16
Standard_E32s_v3 MemoryOptimized   8192    32
Standard_E48s_v3 MemoryOptimized   8192    48
Standard_E64s_v3 MemoryOptimized   6912    64
```

<span data-ttu-id="362f1-109">此 Cmdlet 顯示提供位置的基本 SKU 資訊。</span><span class="sxs-lookup"><span data-stu-id="362f1-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="362f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="362f1-110">PARAMETERS</span></span>

### <span data-ttu-id="362f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362f1-111">-DefaultProfile</span></span>
<span data-ttu-id="362f1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="362f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362f1-113">-位置</span><span class="sxs-lookup"><span data-stu-id="362f1-113">-Location</span></span>
<span data-ttu-id="362f1-114">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="362f1-114">The name of the location.</span></span>

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

### <span data-ttu-id="362f1-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="362f1-115">-SubscriptionId</span></span>
<span data-ttu-id="362f1-116">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="362f1-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="362f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362f1-117">CommonParameters</span></span>
<span data-ttu-id="362f1-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="362f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362f1-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="362f1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362f1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="362f1-120">INPUTS</span></span>

## <span data-ttu-id="362f1-121">輸出</span><span class="sxs-lookup"><span data-stu-id="362f1-121">OUTPUTS</span></span>

### <span data-ttu-id="362f1-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="362f1-122">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20200214Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="362f1-123">筆記</span><span class="sxs-lookup"><span data-stu-id="362f1-123">NOTES</span></span>

<span data-ttu-id="362f1-124">別名</span><span class="sxs-lookup"><span data-stu-id="362f1-124">ALIASES</span></span>

## <span data-ttu-id="362f1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="362f1-125">RELATED LINKS</span></span>

