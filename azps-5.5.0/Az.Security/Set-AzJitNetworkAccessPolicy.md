---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 83aca2353102b85fd138422f249464b59a8666ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142540"
---
# <span data-ttu-id="78123-101">Set-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="78123-101">Set-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="78123-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78123-102">SYNOPSIS</span></span>
<span data-ttu-id="78123-103">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="78123-103">Updates JIT network access policy.</span></span>

## <span data-ttu-id="78123-104">句法</span><span class="sxs-lookup"><span data-stu-id="78123-104">SYNTAX</span></span>

```
Set-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78123-105">說明</span><span class="sxs-lookup"><span data-stu-id="78123-105">DESCRIPTION</span></span>
<span data-ttu-id="78123-106">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="78123-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="78123-107">示例</span><span class="sxs-lookup"><span data-stu-id="78123-107">EXAMPLES</span></span>

### <span data-ttu-id="78123-108">範例1</span><span class="sxs-lookup"><span data-stu-id="78123-108">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="78123-109">使用新的 VM 規則更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="78123-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="78123-110">參數</span><span class="sxs-lookup"><span data-stu-id="78123-110">PARAMETERS</span></span>

### <span data-ttu-id="78123-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78123-111">-DefaultProfile</span></span>
<span data-ttu-id="78123-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78123-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78123-113">類型</span><span class="sxs-lookup"><span data-stu-id="78123-113">-Kind</span></span>
<span data-ttu-id="78123-114">Jit 網路存取原則類型。</span><span class="sxs-lookup"><span data-stu-id="78123-114">Jit Network Access Policy Kind.</span></span>

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

### <span data-ttu-id="78123-115">-位置</span><span class="sxs-lookup"><span data-stu-id="78123-115">-Location</span></span>
<span data-ttu-id="78123-116">位於.</span><span class="sxs-lookup"><span data-stu-id="78123-116">Location.</span></span>

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

### <span data-ttu-id="78123-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="78123-117">-Name</span></span>
<span data-ttu-id="78123-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="78123-118">Resource name.</span></span>

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

### <span data-ttu-id="78123-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78123-119">-ResourceGroupName</span></span>
<span data-ttu-id="78123-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="78123-120">Resource group name.</span></span>

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

### <span data-ttu-id="78123-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="78123-121">-VirtualMachine</span></span>
<span data-ttu-id="78123-122">虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="78123-122">Virtual Machines.</span></span>

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

### <span data-ttu-id="78123-123">-確認</span><span class="sxs-lookup"><span data-stu-id="78123-123">-Confirm</span></span>
<span data-ttu-id="78123-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="78123-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78123-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78123-125">-WhatIf</span></span>
<span data-ttu-id="78123-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="78123-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78123-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="78123-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78123-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78123-128">CommonParameters</span></span>
<span data-ttu-id="78123-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78123-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78123-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78123-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78123-131">輸入</span><span class="sxs-lookup"><span data-stu-id="78123-131">INPUTS</span></span>

### <span data-ttu-id="78123-132">所有</span><span class="sxs-lookup"><span data-stu-id="78123-132">None</span></span>

## <span data-ttu-id="78123-133">輸出</span><span class="sxs-lookup"><span data-stu-id="78123-133">OUTPUTS</span></span>

### <span data-ttu-id="78123-134">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="78123-134">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="78123-135">筆記</span><span class="sxs-lookup"><span data-stu-id="78123-135">NOTES</span></span>

## <span data-ttu-id="78123-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="78123-136">RELATED LINKS</span></span>
