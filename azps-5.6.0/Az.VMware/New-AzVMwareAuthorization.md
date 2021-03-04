---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/powershell/module/az.vmware/new-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/New-AzVMwareAuthorization.md
ms.openlocfilehash: 7c532f6aca8c959367d4e67725f36b44e4978840
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912142"
---
# <span data-ttu-id="704bf-101">New-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="704bf-101">New-AzVMWareAuthorization</span></span>

## <span data-ttu-id="704bf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="704bf-102">SYNOPSIS</span></span>
<span data-ttu-id="704bf-103">在私人雲端中建立或更新 ExpressRoute 回路授權</span><span class="sxs-lookup"><span data-stu-id="704bf-103">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="704bf-104">語法</span><span class="sxs-lookup"><span data-stu-id="704bf-104">SYNTAX</span></span>

```
New-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="704bf-105">描述</span><span class="sxs-lookup"><span data-stu-id="704bf-105">DESCRIPTION</span></span>
<span data-ttu-id="704bf-106">在私人雲端中建立或更新 ExpressRoute 回路授權</span><span class="sxs-lookup"><span data-stu-id="704bf-106">Create or update an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="704bf-107">例子</span><span class="sxs-lookup"><span data-stu-id="704bf-107">EXAMPLES</span></span>

### <span data-ttu-id="704bf-108">範例 1：建立自動化</span><span class="sxs-lookup"><span data-stu-id="704bf-108">Example 1: Create autorization</span></span>
```powershell
PS C:\> New-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group



Name           Type
----           ----
azps-test-auth Microsoft.AVS/privateClouds/authorizations
```

<span data-ttu-id="704bf-109">此 Cmdlet 在私人 `azps-test-auth` 雲端下建立授權 `azps-test-cloud`</span><span class="sxs-lookup"><span data-stu-id="704bf-109">This cmdlet creates authorization `azps-test-auth` under private cloud `azps-test-cloud`</span></span>

## <span data-ttu-id="704bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="704bf-110">PARAMETERS</span></span>

### <span data-ttu-id="704bf-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="704bf-111">-AsJob</span></span>
<span data-ttu-id="704bf-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="704bf-112">Run the command as a job</span></span>

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

### <span data-ttu-id="704bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704bf-113">-DefaultProfile</span></span>
<span data-ttu-id="704bf-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="704bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="704bf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="704bf-115">-Name</span></span>
<span data-ttu-id="704bf-116">專用雲端中的 ExpressRoute 回路授權名稱</span><span class="sxs-lookup"><span data-stu-id="704bf-116">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

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

### <span data-ttu-id="704bf-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="704bf-117">-NoWait</span></span>
<span data-ttu-id="704bf-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="704bf-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="704bf-119">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="704bf-119">-PrivateCloudName</span></span>
<span data-ttu-id="704bf-120">私人雲端的名稱。</span><span class="sxs-lookup"><span data-stu-id="704bf-120">The name of the private cloud.</span></span>

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

### <span data-ttu-id="704bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="704bf-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="704bf-122">The name of the resource group.</span></span>
<span data-ttu-id="704bf-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="704bf-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="704bf-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="704bf-124">-SubscriptionId</span></span>
<span data-ttu-id="704bf-125">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="704bf-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="704bf-126">-確認</span><span class="sxs-lookup"><span data-stu-id="704bf-126">-Confirm</span></span>
<span data-ttu-id="704bf-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="704bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704bf-128">-WhatIf</span></span>
<span data-ttu-id="704bf-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="704bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="704bf-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="704bf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704bf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704bf-131">CommonParameters</span></span>
<span data-ttu-id="704bf-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="704bf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704bf-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="704bf-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704bf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="704bf-134">INPUTS</span></span>

## <span data-ttu-id="704bf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="704bf-135">OUTPUTS</span></span>

### <span data-ttu-id="704bf-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span><span class="sxs-lookup"><span data-stu-id="704bf-136">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IExpressRouteAuthorization</span></span>

## <span data-ttu-id="704bf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="704bf-137">NOTES</span></span>

<span data-ttu-id="704bf-138">別名</span><span class="sxs-lookup"><span data-stu-id="704bf-138">ALIASES</span></span>

## <span data-ttu-id="704bf-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="704bf-139">RELATED LINKS</span></span>

