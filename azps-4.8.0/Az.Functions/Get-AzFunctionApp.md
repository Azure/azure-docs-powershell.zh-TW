---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/get-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Get-AzFunctionApp.md
ms.openlocfilehash: 6a3a421f1da374db1cc08635891bdeec4375855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128714"
---
# <span data-ttu-id="6e692-101">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="6e692-101">Get-AzFunctionApp</span></span>

## <span data-ttu-id="6e692-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e692-102">SYNOPSIS</span></span>
<span data-ttu-id="6e692-103">取得訂閱中的函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e692-103">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="6e692-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e692-104">SYNTAX</span></span>

### <span data-ttu-id="6e692-105">GetAll (預設) </span><span class="sxs-lookup"><span data-stu-id="6e692-105">GetAll (Default)</span></span>
```
Get-AzFunctionApp [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e692-106">ByLocation</span><span class="sxs-lookup"><span data-stu-id="6e692-106">ByLocation</span></span>
```
Get-AzFunctionApp -Location <String> [-SubscriptionId <String[]>] [-IncludeSlot] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e692-107">ByName</span><span class="sxs-lookup"><span data-stu-id="6e692-107">ByName</span></span>
```
Get-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e692-108">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e692-108">ByResourceGroupName</span></span>
```
Get-AzFunctionApp [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-IncludeSlot]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6e692-109">說明</span><span class="sxs-lookup"><span data-stu-id="6e692-109">DESCRIPTION</span></span>
<span data-ttu-id="6e692-110">取得訂閱中的函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e692-110">Gets function apps in a subscription.</span></span>

## <span data-ttu-id="6e692-111">示例</span><span class="sxs-lookup"><span data-stu-id="6e692-111">EXAMPLES</span></span>

### <span data-ttu-id="6e692-112">範例1：取得所有的函數 app。</span><span class="sxs-lookup"><span data-stu-id="6e692-112">Example 1: Get all function apps.</span></span>
```powershell
PS C:\> Get-AzFunctionApp

Name                     Status  OSType  Runtime Location    AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------    -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US  CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
Functions1-Windows-Java  Running Windows Java    West Europe Premium1-WE    Functions-West-Europe1    fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6e692-113">範例2：依名稱取得函數 app。</span><span class="sxs-lookup"><span data-stu-id="6e692-113">Example 2: Get function apps by name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win -Name Functions1-Windows-DoNet

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6e692-114">範例3：依資源群組名稱取得函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e692-114">Example 3: Get function apps by resource group name.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -ResourceGroupName Functions-West-Europe-Win

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6e692-115">範例4：取得指定訂閱的函數應用程式。</span><span class="sxs-lookup"><span data-stu-id="6e692-115">Example 4: Get function apps for the given subscriptions.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -SubscriptionId fe16564a-d943-4bf8-8c28-cf01708c3f8b

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



### <span data-ttu-id="6e692-116">範例5：依位置取得函數 app。</span><span class="sxs-lookup"><span data-stu-id="6e692-116">Example 5: Get function apps by location.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Location "Central US"

Name                     Status  OSType  Runtime Location   AppServicePlan ResourceGroupName         SubscriptionId
----                     ------  ------  ------- --------   -------------- -----------------         --------------
Functions1-Windows-DoNet Running Windows DotNet  Central US CentralUSPlan  Functions-West-Europe-Win fe16564a-d943-4bf8-8c28-cf01708c3f8b
```



## <span data-ttu-id="6e692-117">參數</span><span class="sxs-lookup"><span data-stu-id="6e692-117">PARAMETERS</span></span>

### <span data-ttu-id="6e692-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e692-118">-DefaultProfile</span></span>
<span data-ttu-id="6e692-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e692-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e692-120">-IncludeSlot</span><span class="sxs-lookup"><span data-stu-id="6e692-120">-IncludeSlot</span></span>
<span data-ttu-id="6e692-121">用來指定是否要在結果中包含部署槽。</span><span class="sxs-lookup"><span data-stu-id="6e692-121">Use to specify whether to include deployment slots in results.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e692-122">-位置</span><span class="sxs-lookup"><span data-stu-id="6e692-122">-Location</span></span>
<span data-ttu-id="6e692-123">函數 app 的位置。</span><span class="sxs-lookup"><span data-stu-id="6e692-123">The location of the function app.</span></span>

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

### <span data-ttu-id="6e692-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e692-124">-Name</span></span>
<span data-ttu-id="6e692-125">函數應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e692-125">The name of the function app.</span></span>

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

### <span data-ttu-id="6e692-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e692-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e692-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6e692-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e692-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e692-128">-SubscriptionId</span></span>
<span data-ttu-id="6e692-129">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6e692-129">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="6e692-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e692-130">CommonParameters</span></span>
<span data-ttu-id="6e692-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e692-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e692-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6e692-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e692-133">輸入</span><span class="sxs-lookup"><span data-stu-id="6e692-133">INPUTS</span></span>

## <span data-ttu-id="6e692-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6e692-134">OUTPUTS</span></span>

### <span data-ttu-id="6e692-135">ISite 中的 Api20190801，然後再</span><span class="sxs-lookup"><span data-stu-id="6e692-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="6e692-136">筆記</span><span class="sxs-lookup"><span data-stu-id="6e692-136">NOTES</span></span>

<span data-ttu-id="6e692-137">別名</span><span class="sxs-lookup"><span data-stu-id="6e692-137">ALIASES</span></span>

## <span data-ttu-id="6e692-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e692-138">RELATED LINKS</span></span>

