---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0588929d8f45c04275e2d79823ed86c9db787060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908365"
---
# <span data-ttu-id="ab04e-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab04e-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ab04e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ab04e-102">SYNOPSIS</span></span>
<span data-ttu-id="ab04e-103">更新 JIT 網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="ab04e-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="ab04e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ab04e-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab04e-105">描述</span><span class="sxs-lookup"><span data-stu-id="ab04e-105">DESCRIPTION</span></span>
<span data-ttu-id="ab04e-106">更新 JIT 網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="ab04e-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="ab04e-107">例子</span><span class="sxs-lookup"><span data-stu-id="ab04e-107">EXAMPLES</span></span>

### <span data-ttu-id="ab04e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="ab04e-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="ab04e-109">使用新的 VM 規則更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="ab04e-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="ab04e-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab04e-110">PARAMETERS</span></span>

### <span data-ttu-id="ab04e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab04e-111">-DefaultProfile</span></span>
<span data-ttu-id="ab04e-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab04e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="ab04e-113">-Kind</span></span>
<span data-ttu-id="ab04e-114">Jit Network Access Policy Kind.</span><span class="sxs-lookup"><span data-stu-id="ab04e-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="ab04e-115">-位置</span><span class="sxs-lookup"><span data-stu-id="ab04e-115">-Location</span></span>
<span data-ttu-id="ab04e-116">位置。</span><span class="sxs-lookup"><span data-stu-id="ab04e-116">Location.</span></span>

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

### <span data-ttu-id="ab04e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab04e-117">-Name</span></span>
<span data-ttu-id="ab04e-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ab04e-118">Resource name.</span></span>

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

### <span data-ttu-id="ab04e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab04e-119">-ResourceGroupName</span></span>
<span data-ttu-id="ab04e-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ab04e-120">Resource group name.</span></span>

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

### <span data-ttu-id="ab04e-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ab04e-121">-VirtualMachine</span></span>
<span data-ttu-id="ab04e-122">虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ab04e-122">Virtual Machines.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab04e-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ab04e-123">-Confirm</span></span>
<span data-ttu-id="ab04e-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ab04e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab04e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab04e-125">-WhatIf</span></span>
<span data-ttu-id="ab04e-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab04e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab04e-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab04e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab04e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab04e-128">CommonParameters</span></span>
<span data-ttu-id="ab04e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ab04e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab04e-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab04e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab04e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ab04e-131">INPUTS</span></span>

### <span data-ttu-id="ab04e-132">沒有</span><span class="sxs-lookup"><span data-stu-id="ab04e-132">None</span></span>

## <span data-ttu-id="ab04e-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ab04e-133">OUTPUTS</span></span>

### <span data-ttu-id="ab04e-134">Microsoft.Azure.Commands.Security.models.JitNetworkAccesssPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab04e-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ab04e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ab04e-135">NOTES</span></span>

## <span data-ttu-id="ab04e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab04e-136">RELATED LINKS</span></span>
