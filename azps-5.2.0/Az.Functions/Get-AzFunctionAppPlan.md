---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionAppPlan.md
ms.openlocfilehash: d08d050253842e13967d001889e1b7d1b331ce17
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275968"
---
# <span data-ttu-id="605a6-101">Get-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="605a6-101">Get-AzFunctionAppPlan</span></span>

## <span data-ttu-id="605a6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="605a6-102">SYNOPSIS</span></span>
<span data-ttu-id="605a6-103">在訂閱中取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-103">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="605a6-104">句法</span><span class="sxs-lookup"><span data-stu-id="605a6-104">SYNTAX</span></span>

### <span data-ttu-id="605a6-105">GetAll (預設) </span><span class="sxs-lookup"><span data-stu-id="605a6-105">GetAll (Default)</span></span>
```
Get-AzFunctionAppPlan [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="605a6-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="605a6-106">ByLocation</span></span>
```
Get-AzFunctionAppPlan -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="605a6-107">ByName</span><span class="sxs-lookup"><span data-stu-id="605a6-107">ByName</span></span>
```
Get-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="605a6-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605a6-108">ByResourceGroupName</span></span>
```
Get-AzFunctionAppPlan [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="605a6-109">說明</span><span class="sxs-lookup"><span data-stu-id="605a6-109">DESCRIPTION</span></span>
<span data-ttu-id="605a6-110">在訂閱中取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-110">Get function apps plans in a subscription.</span></span>

## <span data-ttu-id="605a6-111">示例</span><span class="sxs-lookup"><span data-stu-id="605a6-111">EXAMPLES</span></span>

### <span data-ttu-id="605a6-112">範例1：取得所有的函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-112">Example 1: Get all function app plans.</span></span>
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

<span data-ttu-id="605a6-113">這個命令會取得所有的函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-113">This command gets all function app plans.</span></span>

### <span data-ttu-id="605a6-114">範例2：透過資源群組名稱取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-114">Example 2: Get function app plans by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -ResourceGroupName "West Europe"

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Linux-Premium   Linux      ElasticPremium EP1     West Europe Func99-West-Europe-Linux-Premium fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
Func99-Windows-Premium1680894595   Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="605a6-115">這個命令會透過資源群組名稱來取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-115">This command gets function app plans by resource group name.</span></span>

### <span data-ttu-id="605a6-116">範例3：取得指定訂閱的函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-116">Example 3: Get function app plans for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8z

Name                               WorkerType SkuTier        SkuName Location    ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------    -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     West Europe Func99-West-Europe-Win-Premium   fe16564a-d943-4bf8-8c28-cf01708c3f8z
```

<span data-ttu-id="605a6-117">這個命令會針對給定的訂閱取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-117">This command gets function app plans for the given subscriptions.</span></span>

### <span data-ttu-id="605a6-118">範例4：透過位置取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-118">Example 4: Get function app plans by location.</span></span>
```powershell
PS C:\> Get-AzFunctionAppPlan -Location "Central US"

Name                               WorkerType SkuTier        SkuName Location   ResourceGroupName                SubscriptionId
----                               ---------- -------        ------- --------   -----------------                --------------
Func99-West-Europe-Windows-Premium Windows    ElasticPremium EP1     Central US Func99-West-Europe-Win-Premium   3r16564a-d943-4bf8-8c28-cf01708c3f8b
```

<span data-ttu-id="605a6-119">這個命令會透過位置來取得函數 app 方案。</span><span class="sxs-lookup"><span data-stu-id="605a6-119">This command gets function app plans by location.</span></span>

## <span data-ttu-id="605a6-120">參數</span><span class="sxs-lookup"><span data-stu-id="605a6-120">PARAMETERS</span></span>

### <span data-ttu-id="605a6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="605a6-121">-DefaultProfile</span></span>
<span data-ttu-id="605a6-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="605a6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="605a6-123">-位置</span><span class="sxs-lookup"><span data-stu-id="605a6-123">-Location</span></span>
<span data-ttu-id="605a6-124">函數 app 方案的位置。</span><span class="sxs-lookup"><span data-stu-id="605a6-124">The location of the function app plan.</span></span>

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

### <span data-ttu-id="605a6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="605a6-125">-Name</span></span>
<span data-ttu-id="605a6-126">服務方案名稱。</span><span class="sxs-lookup"><span data-stu-id="605a6-126">The service plan name.</span></span>

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

### <span data-ttu-id="605a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="605a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="605a6-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="605a6-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="605a6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="605a6-129">-SubscriptionId</span></span>
<span data-ttu-id="605a6-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="605a6-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="605a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="605a6-131">CommonParameters</span></span>
<span data-ttu-id="605a6-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="605a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="605a6-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="605a6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="605a6-134">輸入</span><span class="sxs-lookup"><span data-stu-id="605a6-134">INPUTS</span></span>

## <span data-ttu-id="605a6-135">輸出</span><span class="sxs-lookup"><span data-stu-id="605a6-135">OUTPUTS</span></span>

### <span data-ttu-id="605a6-136">IAppServicePlan 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="605a6-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="605a6-137">筆記</span><span class="sxs-lookup"><span data-stu-id="605a6-137">NOTES</span></span>

<span data-ttu-id="605a6-138">別名</span><span class="sxs-lookup"><span data-stu-id="605a6-138">ALIASES</span></span>

## <span data-ttu-id="605a6-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="605a6-139">RELATED LINKS</span></span>

