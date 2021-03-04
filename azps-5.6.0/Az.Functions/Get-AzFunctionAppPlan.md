---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: 786f3e406228eb7929993804a8cef84e7cae109e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906193"
---
# <span data-ttu-id="7848b-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="7848b-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="7848b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7848b-102">SYNOPSIS</span></span>
<span data-ttu-id="7848b-103">在訂閱中取得功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="7848b-104">語法</span><span class="sxs-lookup"><span data-stu-id="7848b-104">SYNTAX</span></span>

### <span data-ttu-id="7848b-105">GetAll (預設) </span><span class="sxs-lookup"><span data-stu-id="7848b-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7848b-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="7848b-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7848b-107">ByName</span><span class="sxs-lookup"><span data-stu-id="7848b-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7848b-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7848b-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="7848b-109">描述</span><span class="sxs-lookup"><span data-stu-id="7848b-109">DESCRIPTION</span></span>
<span data-ttu-id="7848b-110">在訂閱中取得功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="7848b-111">例子</span><span class="sxs-lookup"><span data-stu-id="7848b-111">EXAMPLES</span></span>

### <span data-ttu-id="7848b-112">範例 1：取得所有函數應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-112">Example 1: Get all function app plans.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium428118799    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium677505437    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium711892854    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium819994758    Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="7848b-113">此命令會獲得所有功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="7848b-114">範例 2：根據資源組名取得函數應用程式計畫。</span><span class="sxs-lookup"><span data-stu-id="7848b-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="7848b-115">此命令會按資源組名獲得函數應用程式計畫。</span><span class="sxs-lookup"><span data-stu-id="7848b-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="7848b-116">範例 3：取得給定訂閱的函數應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="7848b-117">此命令會針對所給訂閱獲得功能應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="7848b-118">範例 4：根據位置取得函數應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="7848b-119">此命令會按位置獲得函數應用程式方案。</span><span class="sxs-lookup"><span data-stu-id="7848b-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="7848b-120">參數</span><span class="sxs-lookup"><span data-stu-id="7848b-120">PARAMETERS</span></span>

### <span data-ttu-id="7848b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7848b-121">-DefaultProfile</span></span>
<span data-ttu-id="7848b-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7848b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7848b-123">-位置</span><span class="sxs-lookup"><span data-stu-id="7848b-123">-Location</span></span>
<span data-ttu-id="7848b-124">函數應用程式方案的位置。</span><span class="sxs-lookup"><span data-stu-id="7848b-124">The location of the function app plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7848b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7848b-125">-Name</span></span>
<span data-ttu-id="7848b-126">服務方案名稱。</span><span class="sxs-lookup"><span data-stu-id="7848b-126">The service plan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7848b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7848b-127">-ResourceGroupName</span></span>
<span data-ttu-id="7848b-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7848b-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7848b-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7848b-129">-SubscriptionId</span></span>
<span data-ttu-id="7848b-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="7848b-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="7848b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7848b-131">CommonParameters</span></span>
<span data-ttu-id="7848b-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7848b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7848b-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7848b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7848b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="7848b-134">INPUTS</span></span>

## <span data-ttu-id="7848b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7848b-135">OUTPUTS</span></span>

### <span data-ttu-id="7848b-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.models.Api20190801.IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7848b-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="7848b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7848b-137">NOTES</span></span>

<span data-ttu-id="7848b-138">別名</span><span class="sxs-lookup"><span data-stu-id="7848b-138">ALIASES</span></span>

## <span data-ttu-id="7848b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="7848b-139">RELATED LINKS</span></span>

