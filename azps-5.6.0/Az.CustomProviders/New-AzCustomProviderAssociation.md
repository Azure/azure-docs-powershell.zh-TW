---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914130"
---
# <span data-ttu-id="537b2-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="537b2-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="537b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="537b2-102">SYNOPSIS</span></span>
<span data-ttu-id="537b2-103">建立或更新關聯。</span><span class="sxs-lookup"><span data-stu-id="537b2-103">Create or update an association.</span></span>

## <span data-ttu-id="537b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="537b2-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="537b2-105">描述</span><span class="sxs-lookup"><span data-stu-id="537b2-105">DESCRIPTION</span></span>
<span data-ttu-id="537b2-106">建立或更新關聯。</span><span class="sxs-lookup"><span data-stu-id="537b2-106">Create or update an association.</span></span>

## <span data-ttu-id="537b2-107">例子</span><span class="sxs-lookup"><span data-stu-id="537b2-107">EXAMPLES</span></span>

### <span data-ttu-id="537b2-108">範例 1：建立自訂提供者關聯</span><span class="sxs-lookup"><span data-stu-id="537b2-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="537b2-109">建立自訂提供者關聯，關聯的目標提供者必須正確配置「關聯」路由</span><span class="sxs-lookup"><span data-stu-id="537b2-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="537b2-110">參數</span><span class="sxs-lookup"><span data-stu-id="537b2-110">PARAMETERS</span></span>

### <span data-ttu-id="537b2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="537b2-111">-AsJob</span></span>
<span data-ttu-id="537b2-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="537b2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="537b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="537b2-113">-DefaultProfile</span></span>
<span data-ttu-id="537b2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="537b2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="537b2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="537b2-115">-Name</span></span>
<span data-ttu-id="537b2-116">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="537b2-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537b2-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="537b2-117">-NoWait</span></span>
<span data-ttu-id="537b2-118">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="537b2-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="537b2-119">-範圍</span><span class="sxs-lookup"><span data-stu-id="537b2-119">-Scope</span></span>
<span data-ttu-id="537b2-120">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="537b2-120">The scope of the association.</span></span>
<span data-ttu-id="537b2-121">範圍可以是任何有效的 REST 資源實例。</span><span class="sxs-lookup"><span data-stu-id="537b2-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="537b2-122">例如，針對虛擬機器資源使用 '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}'。</span><span class="sxs-lookup"><span data-stu-id="537b2-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="537b2-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="537b2-123">-TargetResourceId</span></span>
<span data-ttu-id="537b2-124">此關聯目標資源的 REST 資源實例。</span><span class="sxs-lookup"><span data-stu-id="537b2-124">The REST resource instance of the target resource for this association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="537b2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="537b2-125">-Confirm</span></span>
<span data-ttu-id="537b2-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="537b2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="537b2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="537b2-127">-WhatIf</span></span>
<span data-ttu-id="537b2-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="537b2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="537b2-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="537b2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="537b2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="537b2-130">CommonParameters</span></span>
<span data-ttu-id="537b2-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="537b2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="537b2-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="537b2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="537b2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="537b2-133">INPUTS</span></span>

## <span data-ttu-id="537b2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="537b2-134">OUTPUTS</span></span>

### <span data-ttu-id="537b2-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="537b2-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="537b2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="537b2-136">NOTES</span></span>

<span data-ttu-id="537b2-137">別名</span><span class="sxs-lookup"><span data-stu-id="537b2-137">ALIASES</span></span>

## <span data-ttu-id="537b2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="537b2-138">RELATED LINKS</span></span>

