---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911325"
---
# <span data-ttu-id="9c392-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="9c392-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="9c392-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c392-102">SYNOPSIS</span></span>
<span data-ttu-id="9c392-103">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="9c392-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="9c392-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c392-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c392-105">描述</span><span class="sxs-lookup"><span data-stu-id="9c392-105">DESCRIPTION</span></span>
<span data-ttu-id="9c392-106">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="9c392-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="9c392-107">例子</span><span class="sxs-lookup"><span data-stu-id="9c392-107">EXAMPLES</span></span>

### <span data-ttu-id="9c392-108">範例 1：使用儀表板範本更新儀表板定義</span><span class="sxs-lookup"><span data-stu-id="9c392-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="9c392-109">使用虛線範本檔案更新儀表板定義。</span><span class="sxs-lookup"><span data-stu-id="9c392-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="9c392-110">參數</span><span class="sxs-lookup"><span data-stu-id="9c392-110">PARAMETERS</span></span>

### <span data-ttu-id="9c392-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="9c392-111">-DashboardPath</span></span>
<span data-ttu-id="9c392-112">現有儀表板範本的路徑。</span><span class="sxs-lookup"><span data-stu-id="9c392-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="9c392-113">儀表板範本可以從入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="9c392-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="9c392-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c392-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="9c392-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c392-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c392-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c392-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="9c392-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c392-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c392-118">-確認</span><span class="sxs-lookup"><span data-stu-id="9c392-118">-Confirm</span></span>
<span data-ttu-id="9c392-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9c392-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c392-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c392-120">-WhatIf</span></span>
<span data-ttu-id="9c392-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c392-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c392-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c392-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c392-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c392-123">CommonParameters</span></span>
<span data-ttu-id="9c392-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c392-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c392-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c392-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c392-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9c392-126">INPUTS</span></span>

## <span data-ttu-id="9c392-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9c392-127">OUTPUTS</span></span>

### <span data-ttu-id="9c392-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="9c392-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="9c392-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9c392-129">NOTES</span></span>

<span data-ttu-id="9c392-130">別名</span><span class="sxs-lookup"><span data-stu-id="9c392-130">ALIASES</span></span>

## <span data-ttu-id="9c392-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c392-131">RELATED LINKS</span></span>

