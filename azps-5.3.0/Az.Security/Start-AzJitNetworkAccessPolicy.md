---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 0efde69aec3b30c58aee8c42aeb1703215219c2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448603"
---
# <span data-ttu-id="a0acd-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a0acd-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a0acd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0acd-102">SYNOPSIS</span></span>
<span data-ttu-id="a0acd-103">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="a0acd-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="a0acd-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0acd-104">SYNTAX</span></span>

### <span data-ttu-id="a0acd-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="a0acd-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0acd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0acd-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0acd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a0acd-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0acd-108">說明</span><span class="sxs-lookup"><span data-stu-id="a0acd-108">DESCRIPTION</span></span>
<span data-ttu-id="a0acd-109">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="a0acd-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="a0acd-110">針對設定的 JIT 網路存取原則驗證要求，並視使用者的要求開啟網路連線。</span><span class="sxs-lookup"><span data-stu-id="a0acd-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="a0acd-111">該要求將會記錄在原則中供日後查看，且會在超過指定的持續時間之後終止。</span><span class="sxs-lookup"><span data-stu-id="a0acd-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="a0acd-112">示例</span><span class="sxs-lookup"><span data-stu-id="a0acd-112">EXAMPLES</span></span>

### <span data-ttu-id="a0acd-113">範例1</span><span class="sxs-lookup"><span data-stu-id="a0acd-113">Example 1</span></span>
```powershell
$MyResource = Get-AzResource -Id /subscriptions/xxxxxxx-xxxxx-xxxxx-xxxxxxx/resourceGroups/PolicyDemo/providers/Microsoft.Compute/virtualMachines/PolicyDemoVM1
$JitPolicy = (@{
        id    = $MyResource.ResourceId; 
        ports = (@{
                number                     = 22
                endTimeUtc                 = Get-Date (Get-Date -AsUTC).AddHours(1) -Format O
                allowedSourceAddressPrefix = @($MyPublicIP) 
            })
    })
$ActivationVM = @($JitPolicy)
Start-AzJitNetworkAccessPolicy -ResourceGroupName $($MyResource.ResourceGroupName) -Location $MyResource.Location -Name "default" -VirtualMachine $ActivationVM

```

<span data-ttu-id="a0acd-114">從我的公用 IP 開啟1小時透過埠22的網路連線 (不會顯示) 。</span><span class="sxs-lookup"><span data-stu-id="a0acd-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="a0acd-115">參數</span><span class="sxs-lookup"><span data-stu-id="a0acd-115">PARAMETERS</span></span>

### <span data-ttu-id="a0acd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0acd-116">-DefaultProfile</span></span>
<span data-ttu-id="a0acd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0acd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0acd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0acd-118">-InputObject</span></span>
<span data-ttu-id="a0acd-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="a0acd-119">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-120">-位置</span><span class="sxs-lookup"><span data-stu-id="a0acd-120">-Location</span></span>
<span data-ttu-id="a0acd-121">位於.</span><span class="sxs-lookup"><span data-stu-id="a0acd-121">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a0acd-122">-Name</span></span>
<span data-ttu-id="a0acd-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a0acd-123">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0acd-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0acd-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="a0acd-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0acd-126">-ResourceId</span></span>
<span data-ttu-id="a0acd-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a0acd-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a0acd-128">-VirtualMachine</span></span>
<span data-ttu-id="a0acd-129">自動提供。</span><span class="sxs-lookup"><span data-stu-id="a0acd-129">Automatic Provisioning.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0acd-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a0acd-130">-Confirm</span></span>
<span data-ttu-id="a0acd-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0acd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0acd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0acd-132">-WhatIf</span></span>
<span data-ttu-id="a0acd-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0acd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0acd-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0acd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0acd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0acd-135">CommonParameters</span></span>
<span data-ttu-id="a0acd-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0acd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0acd-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a0acd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0acd-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a0acd-138">INPUTS</span></span>

### <span data-ttu-id="a0acd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a0acd-139">System.String</span></span>

### <span data-ttu-id="a0acd-140">PSSecurityJitNetworkAccessPolicyInitiateInputObject 中的 JitNetworkAccessPolicies （）</span><span class="sxs-lookup"><span data-stu-id="a0acd-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="a0acd-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a0acd-141">OUTPUTS</span></span>

### <span data-ttu-id="a0acd-142">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="a0acd-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="a0acd-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a0acd-143">NOTES</span></span>

## <span data-ttu-id="a0acd-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0acd-144">RELATED LINKS</span></span>
