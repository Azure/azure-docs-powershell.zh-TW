---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 394975e341d52fb0067b420397189b0a8858cfcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134275"
---
# <span data-ttu-id="c3168-101">New-AzVMwareAuthorization</span><span class="sxs-lookup"><span data-stu-id="c3168-101">New-AzVMwareAuthorization</span></span>

## <span data-ttu-id="c3168-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3168-102">SYNOPSIS</span></span>
<span data-ttu-id="c3168-103">在私有雲端建立或更新 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="c3168-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="c3168-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3168-104">SYNTAX</span></span>

```
New-AzVMwareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c3168-105">說明</span><span class="sxs-lookup"><span data-stu-id="c3168-105">DESCRIPTION</span></span>
<span data-ttu-id="c3168-106">在私有雲端建立或更新 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="c3168-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="c3168-107">示例</span><span class="sxs-lookup"><span data-stu-id="c3168-107">EXAMPLES</span></span>

### <span data-ttu-id="c3168-108">範例1：建立 autorization</span><span class="sxs-lookup"><span data-stu-id="c3168-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMwareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="c3168-109">這個 Cmdlet 會 `azps-test-auth` 在私有雲端下建立授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="c3168-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="c3168-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3168-110">PARAMETERS</span></span>

### <span data-ttu-id="c3168-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3168-111">-AsJob</span></span>
<span data-ttu-id="c3168-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="c3168-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c3168-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3168-113">-DefaultProfile</span></span>
<span data-ttu-id="c3168-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3168-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3168-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3168-115">-Name</span></span>
<span data-ttu-id="c3168-116">私有雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="c3168-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3168-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c3168-117">-NoWait</span></span>
<span data-ttu-id="c3168-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="c3168-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c3168-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="c3168-119">-PrivateCloudName</span></span>
<span data-ttu-id="c3168-120">私有雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3168-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="c3168-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3168-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3168-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3168-122">The name of the resource group.</span></span>
<span data-ttu-id="c3168-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3168-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c3168-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3168-124">-SubscriptionId</span></span>
<span data-ttu-id="c3168-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c3168-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c3168-126">-確認</span><span class="sxs-lookup"><span data-stu-id="c3168-126">-Confirm</span></span>
<span data-ttu-id="c3168-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3168-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3168-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3168-128">-WhatIf</span></span>
<span data-ttu-id="c3168-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3168-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3168-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3168-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3168-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3168-131">CommonParameters</span></span>
<span data-ttu-id="c3168-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3168-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3168-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3168-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3168-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c3168-134">INPUTS</span></span>

## <span data-ttu-id="c3168-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c3168-135">OUTPUTS</span></span>

### <span data-ttu-id="c3168-136">IExpressRouteAuthorization 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="c3168-136">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="c3168-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c3168-137">NOTES</span></span>

<span data-ttu-id="c3168-138">別名</span><span class="sxs-lookup"><span data-stu-id="c3168-138">ALIASES</span></span>

## <span data-ttu-id="c3168-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3168-139">RELATED LINKS</span></span>

