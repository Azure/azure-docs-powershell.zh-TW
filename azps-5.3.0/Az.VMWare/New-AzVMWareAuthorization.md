---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/New-AzVMWareAuthorization.md
ms.openlocfilehash: b1e8ca1e5140470524ec83656ef0042bafa494b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287391"
---
# <span data-ttu-id="9ea03-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="9ea03-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="9ea03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ea03-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea03-103">在私有雲端建立或更新 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="9ea03-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9ea03-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ea03-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9ea03-105">說明</span><span class="sxs-lookup"><span data-stu-id="9ea03-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea03-106">在私有雲端建立或更新 ExpressRoute 線路授權</span><span class="sxs-lookup"><span data-stu-id="9ea03-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="9ea03-107">示例</span><span class="sxs-lookup"><span data-stu-id="9ea03-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea03-108">範例1：建立 autorization</span><span class="sxs-lookup"><span data-stu-id="9ea03-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="9ea03-109">這個 Cmdlet 會 `azps-test-auth` 在私有雲端下建立授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="9ea03-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="9ea03-110">參數</span><span class="sxs-lookup"><span data-stu-id="9ea03-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea03-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ea03-111">-AsJob</span></span>
<span data-ttu-id="9ea03-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9ea03-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9ea03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea03-113">-DefaultProfile</span></span>
<span data-ttu-id="9ea03-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9ea03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ea03-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ea03-115">-Name</span></span>
<span data-ttu-id="9ea03-116">私有雲端中 ExpressRoute 線路授權的名稱</span><span class="sxs-lookup"><span data-stu-id="9ea03-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="9ea03-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9ea03-117">-NoWait</span></span>
<span data-ttu-id="9ea03-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9ea03-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9ea03-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="9ea03-119">-PrivateCloudName</span></span>
<span data-ttu-id="9ea03-120">私有雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ea03-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="9ea03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea03-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ea03-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ea03-122">The name of the resource group.</span></span>
<span data-ttu-id="9ea03-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9ea03-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9ea03-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ea03-124">-SubscriptionId</span></span>
<span data-ttu-id="9ea03-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="9ea03-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9ea03-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9ea03-126">-Confirm</span></span>
<span data-ttu-id="9ea03-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9ea03-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ea03-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ea03-128">-WhatIf</span></span>
<span data-ttu-id="9ea03-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9ea03-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ea03-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9ea03-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ea03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea03-131">CommonParameters</span></span>
<span data-ttu-id="9ea03-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ea03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea03-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ea03-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea03-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9ea03-134">INPUTS</span></span>

## <span data-ttu-id="9ea03-135">輸出</span><span class="sxs-lookup"><span data-stu-id="9ea03-135">OUTPUTS</span></span>

### <span data-ttu-id="9ea03-136">IExpressRouteAuthorization 中的 Api20200320 （）。</span><span class="sxs-lookup"><span data-stu-id="9ea03-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="9ea03-137">筆記</span><span class="sxs-lookup"><span data-stu-id="9ea03-137">NOTES</span></span>

<span data-ttu-id="9ea03-138">別名</span><span class="sxs-lookup"><span data-stu-id="9ea03-138">ALIASES</span></span>

## <span data-ttu-id="9ea03-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ea03-139">RELATED LINKS</span></span>

