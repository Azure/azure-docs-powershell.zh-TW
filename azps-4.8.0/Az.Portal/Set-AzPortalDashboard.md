---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135737"
---
# <span data-ttu-id="5a52c-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="5a52c-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="5a52c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a52c-102">SYNOPSIS</span></span>
<span data-ttu-id="5a52c-103">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="5a52c-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="5a52c-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a52c-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5a52c-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a52c-105">DESCRIPTION</span></span>
<span data-ttu-id="5a52c-106">建立或更新儀表板。</span><span class="sxs-lookup"><span data-stu-id="5a52c-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="5a52c-107">示例</span><span class="sxs-lookup"><span data-stu-id="5a52c-107">EXAMPLES</span></span>

### <span data-ttu-id="5a52c-108">範例1：使用儀表板範本更新儀表板定義</span><span class="sxs-lookup"><span data-stu-id="5a52c-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="5a52c-109">使用 dashbaord 範本檔來更新儀表板定義。</span><span class="sxs-lookup"><span data-stu-id="5a52c-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="5a52c-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a52c-110">PARAMETERS</span></span>

### <span data-ttu-id="5a52c-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="5a52c-111">-DashboardPath</span></span>
<span data-ttu-id="5a52c-112">現有儀表板範本的路徑。</span><span class="sxs-lookup"><span data-stu-id="5a52c-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="5a52c-113">儀表板範本可能會從入口網站下載。</span><span class="sxs-lookup"><span data-stu-id="5a52c-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="5a52c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a52c-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="5a52c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a52c-115">-Name</span></span>


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

### <span data-ttu-id="5a52c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a52c-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="5a52c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a52c-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="5a52c-118">-確認</span><span class="sxs-lookup"><span data-stu-id="5a52c-118">-Confirm</span></span>
<span data-ttu-id="5a52c-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5a52c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a52c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a52c-120">-WhatIf</span></span>
<span data-ttu-id="5a52c-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5a52c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a52c-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5a52c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a52c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a52c-123">CommonParameters</span></span>
<span data-ttu-id="5a52c-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a52c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a52c-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a52c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a52c-126">輸入</span><span class="sxs-lookup"><span data-stu-id="5a52c-126">INPUTS</span></span>

## <span data-ttu-id="5a52c-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5a52c-127">OUTPUTS</span></span>

### <span data-ttu-id="5a52c-128">[Api201901Preview. IDashboard] （）</span><span class="sxs-lookup"><span data-stu-id="5a52c-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="5a52c-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5a52c-129">NOTES</span></span>

<span data-ttu-id="5a52c-130">別名</span><span class="sxs-lookup"><span data-stu-id="5a52c-130">ALIASES</span></span>

## <span data-ttu-id="5a52c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a52c-131">RELATED LINKS</span></span>

