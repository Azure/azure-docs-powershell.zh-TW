---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: ee678b905eba891543399c9130a8ef034daf2a16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906197"
---
# <span data-ttu-id="d7b7e-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d7b7e-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="d7b7e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d7b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b7e-103">在訂閱中獲得功能應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="d7b7e-104">語法</span><span class="sxs-lookup"><span data-stu-id="d7b7e-104">SYNTAX</span></span>

### <span data-ttu-id="d7b7e-105">GetAll (預設) </span><span class="sxs-lookup"><span data-stu-id="d7b7e-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7b7e-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="d7b7e-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7b7e-107">ByName</span><span class="sxs-lookup"><span data-stu-id="d7b7e-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d7b7e-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b7e-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d7b7e-109">描述</span><span class="sxs-lookup"><span data-stu-id="d7b7e-109">DESCRIPTION</span></span>
<span data-ttu-id="d7b7e-110">在訂閱中獲得功能應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="d7b7e-111">例子</span><span class="sxs-lookup"><span data-stu-id="d7b7e-111">EXAMPLES</span></span>

### <span data-ttu-id="d7b7e-112">範例 1：取得所有函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7b7e-113">範例 2：按名稱取得函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7b7e-114">範例 3：根據資源組名取得函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7b7e-115">範例 4：取得給定訂閱的函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="d7b7e-116">範例 5：根據位置取得函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="d7b7e-117">參數</span><span class="sxs-lookup"><span data-stu-id="d7b7e-117">PARAMETERS</span></span>

### <span data-ttu-id="d7b7e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b7e-118">-DefaultProfile</span></span>
<span data-ttu-id="d7b7e-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7b7e-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="d7b7e-120">-IncludeSlot</span></span>
<span data-ttu-id="d7b7e-121">指定是否要在結果中納入部署時段。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7b7e-122">-位置</span><span class="sxs-lookup"><span data-stu-id="d7b7e-122">-Location</span></span>
<span data-ttu-id="d7b7e-123">函數應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-123">The location of the function app.</span></span>

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

### <span data-ttu-id="d7b7e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d7b7e-124">-Name</span></span>
<span data-ttu-id="d7b7e-125">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-125">The name of the function app.</span></span>

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

### <span data-ttu-id="d7b7e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7b7e-126">-ResourceGroupName</span></span>
<span data-ttu-id="d7b7e-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7b7e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7b7e-128">-SubscriptionId</span></span>
<span data-ttu-id="d7b7e-129">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="d7b7e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b7e-130">CommonParameters</span></span>
<span data-ttu-id="d7b7e-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d7b7e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b7e-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7b7e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b7e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="d7b7e-133">INPUTS</span></span>

## <span data-ttu-id="d7b7e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d7b7e-134">OUTPUTS</span></span>

### <span data-ttu-id="d7b7e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="d7b7e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="d7b7e-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d7b7e-136">NOTES</span></span>

<span data-ttu-id="d7b7e-137">別名</span><span class="sxs-lookup"><span data-stu-id="d7b7e-137">ALIASES</span></span>

## <span data-ttu-id="d7b7e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d7b7e-138">RELATED LINKS</span></span>

