---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverlocationbasedcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerLocationBasedCapability.md
ms.openlocfilehash: 02a3a95be4a6e4e44f20fa9a140ef690203e6d84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904641"
---
# <span data-ttu-id="47c22-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span><span class="sxs-lookup"><span data-stu-id="47c22-101">Get-AzMySqlFlexibleServerLocationBasedCapability</span></span>

## <span data-ttu-id="47c22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47c22-102">SYNOPSIS</span></span>
<span data-ttu-id="47c22-103">取得位置的可用 SKU 資訊</span><span class="sxs-lookup"><span data-stu-id="47c22-103">Get the available SKU information for the location</span></span>

## <span data-ttu-id="47c22-104">語法</span><span class="sxs-lookup"><span data-stu-id="47c22-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerLocationBasedCapability -Location <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="47c22-105">描述</span><span class="sxs-lookup"><span data-stu-id="47c22-105">DESCRIPTION</span></span>
<span data-ttu-id="47c22-106">取得位置的可用 SKU 資訊</span><span class="sxs-lookup"><span data-stu-id="47c22-106">Get the available SKU information for the location</span></span>

## <span data-ttu-id="47c22-107">例子</span><span class="sxs-lookup"><span data-stu-id="47c22-107">EXAMPLES</span></span>

### <span data-ttu-id="47c22-108">範例 1：根據位置名稱取得位置功能</span><span class="sxs-lookup"><span data-stu-id="47c22-108">Example 1: Get location capabilities by location name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerLocationBasedCapability -Location westus2
"Please refer to https://aka.ms/mysql-pricing for pricing details"

SKU               Tier            Memory vCore
---               ----            ------ -----
Standard_B1s      Burstable         1024     1
Standard_B1ms     Burstable         2048     1
Standard_B2s      Burstable         2048     2
Standard_D2ds_v4  GeneralPurpose    4096     2
Standard_D4ds_v4  GeneralPurpose    4096     4
Standard_D8ds_v4  GeneralPurpose    4096     8
Standard_D16ds_v4 GeneralPurpose    4096    16
Standard_D32ds_v4 GeneralPurpose    4096    32
Standard_D48ds_v4 GeneralPurpose    4096    48
Standard_D64ds_v4 GeneralPurpose    4096    64
Standard_E2ds_v4  MemoryOptimized   8192     2
Standard_E4ds_v4  MemoryOptimized   8192     4
Standard_E8ds_v4  MemoryOptimized   8192     8
Standard_E16ds_v4 MemoryOptimized   8192    16
Standard_E32ds_v4 MemoryOptimized   8192    32
Standard_E48ds_v4 MemoryOptimized   8192    48
Standard_E64ds_v4 MemoryOptimized   8192    64

```

<span data-ttu-id="47c22-109">此 Cmdlet 顯示提供位置的基本 SKU 資訊。</span><span class="sxs-lookup"><span data-stu-id="47c22-109">This cmdlet shows basic sku information of the provided location.</span></span>

## <span data-ttu-id="47c22-110">參數</span><span class="sxs-lookup"><span data-stu-id="47c22-110">PARAMETERS</span></span>

### <span data-ttu-id="47c22-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47c22-111">-DefaultProfile</span></span>
<span data-ttu-id="47c22-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47c22-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47c22-113">-位置</span><span class="sxs-lookup"><span data-stu-id="47c22-113">-Location</span></span>
<span data-ttu-id="47c22-114">位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c22-114">The name of the location.</span></span>

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

### <span data-ttu-id="47c22-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47c22-115">-SubscriptionId</span></span>
<span data-ttu-id="47c22-116">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="47c22-116">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="47c22-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47c22-117">CommonParameters</span></span>
<span data-ttu-id="47c22-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47c22-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47c22-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47c22-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47c22-120">輸入</span><span class="sxs-lookup"><span data-stu-id="47c22-120">INPUTS</span></span>

## <span data-ttu-id="47c22-121">輸出</span><span class="sxs-lookup"><span data-stu-id="47c22-121">OUTPUTS</span></span>

### <span data-ttu-id="47c22-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span><span class="sxs-lookup"><span data-stu-id="47c22-122">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.ICapabilityProperties</span></span>

## <span data-ttu-id="47c22-123">筆記</span><span class="sxs-lookup"><span data-stu-id="47c22-123">NOTES</span></span>

<span data-ttu-id="47c22-124">別名</span><span class="sxs-lookup"><span data-stu-id="47c22-124">ALIASES</span></span>

## <span data-ttu-id="47c22-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="47c22-125">RELATED LINKS</span></span>

