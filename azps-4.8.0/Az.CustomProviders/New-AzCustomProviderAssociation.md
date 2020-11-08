---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: ae630f053f6267a49477118786cf70b65782d68e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128499"
---
# <span data-ttu-id="bc9b0-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="bc9b0-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="bc9b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="bc9b0-103">建立或更新關聯性。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-103">Create or update an association.</span></span>

## <span data-ttu-id="bc9b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc9b0-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc9b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc9b0-105">DESCRIPTION</span></span>
<span data-ttu-id="bc9b0-106">建立或更新關聯性。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-106">Create or update an association.</span></span>

## <span data-ttu-id="bc9b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc9b0-107">EXAMPLES</span></span>

### <span data-ttu-id="bc9b0-108">範例1：建立自訂提供者關聯</span><span class="sxs-lookup"><span data-stu-id="bc9b0-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="bc9b0-109">建立自訂提供者關聯，必須正確地將關聯的目標 provioder 設定為「關聯」的路由</span><span class="sxs-lookup"><span data-stu-id="bc9b0-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="bc9b0-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc9b0-110">PARAMETERS</span></span>

### <span data-ttu-id="bc9b0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc9b0-111">-AsJob</span></span>
<span data-ttu-id="bc9b0-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="bc9b0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="bc9b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc9b0-113">-DefaultProfile</span></span>
<span data-ttu-id="bc9b0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc9b0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc9b0-115">-Name</span></span>
<span data-ttu-id="bc9b0-116">關聯的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-116">The name of the association.</span></span>

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

### <span data-ttu-id="bc9b0-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bc9b0-117">-NoWait</span></span>
<span data-ttu-id="bc9b0-118">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="bc9b0-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bc9b0-119">-範圍</span><span class="sxs-lookup"><span data-stu-id="bc9b0-119">-Scope</span></span>
<span data-ttu-id="bc9b0-120">關聯的範圍。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-120">The scope of the association.</span></span>
<span data-ttu-id="bc9b0-121">範圍可以是任何有效的 REST 資源實例。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="bc9b0-122">例如，針對虛擬機器資源使用 "/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}"。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

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

### <span data-ttu-id="bc9b0-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bc9b0-123">-TargetResourceId</span></span>
<span data-ttu-id="bc9b0-124">此關聯之目標資源的 REST 資源實例。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="bc9b0-125">-確認</span><span class="sxs-lookup"><span data-stu-id="bc9b0-125">-Confirm</span></span>
<span data-ttu-id="bc9b0-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc9b0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc9b0-127">-WhatIf</span></span>
<span data-ttu-id="bc9b0-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc9b0-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc9b0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc9b0-130">CommonParameters</span></span>
<span data-ttu-id="bc9b0-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc9b0-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc9b0-133">輸入</span><span class="sxs-lookup"><span data-stu-id="bc9b0-133">INPUTS</span></span>

## <span data-ttu-id="bc9b0-134">輸出</span><span class="sxs-lookup"><span data-stu-id="bc9b0-134">OUTPUTS</span></span>

### <span data-ttu-id="bc9b0-135">IAssociation （CustomProviders）。 Api20180901Preview。</span><span class="sxs-lookup"><span data-stu-id="bc9b0-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="bc9b0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="bc9b0-136">NOTES</span></span>

<span data-ttu-id="bc9b0-137">別名</span><span class="sxs-lookup"><span data-stu-id="bc9b0-137">ALIASES</span></span>

## <span data-ttu-id="bc9b0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc9b0-138">RELATED LINKS</span></span>
