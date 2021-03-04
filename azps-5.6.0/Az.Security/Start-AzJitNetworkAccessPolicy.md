---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 674f88a30ea036fc496cd6931b3d856a20a25c0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910618"
---
# <span data-ttu-id="ea534-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea534-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ea534-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ea534-102">SYNOPSIS</span></span>
<span data-ttu-id="ea534-103">會要求暫時網路存取。</span><span class="sxs-lookup"><span data-stu-id="ea534-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="ea534-104">語法</span><span class="sxs-lookup"><span data-stu-id="ea534-104">SYNTAX</span></span>

### <span data-ttu-id="ea534-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="ea534-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea534-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea534-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea534-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ea534-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea534-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea534-108">DESCRIPTION</span></span>
<span data-ttu-id="ea534-109">會要求暫時網路存取。</span><span class="sxs-lookup"><span data-stu-id="ea534-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="ea534-110">已根據已配置的 JIT 網路存取策略驗證要求，如果允許，會根據使用者的要求開啟網路連接。</span><span class="sxs-lookup"><span data-stu-id="ea534-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="ea534-111">要求會記錄在政策中，供日後審查，並將于超過指定的期間時終止。</span><span class="sxs-lookup"><span data-stu-id="ea534-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="ea534-112">例子</span><span class="sxs-lookup"><span data-stu-id="ea534-112">EXAMPLES</span></span>

### <span data-ttu-id="ea534-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="ea534-113">Example 1</span></span>
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

<span data-ttu-id="ea534-114">從我的公用 IP 埠 22 開啟網路連接 1 小時， (未) 。</span><span class="sxs-lookup"><span data-stu-id="ea534-114">Opens up a network connection for 1 hour over port 22 from my public IP (not shown).</span></span>

## <span data-ttu-id="ea534-115">參數</span><span class="sxs-lookup"><span data-stu-id="ea534-115">PARAMETERS</span></span>

### <span data-ttu-id="ea534-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea534-116">-DefaultProfile</span></span>
<span data-ttu-id="ea534-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ea534-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea534-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea534-118">-InputObject</span></span>
<span data-ttu-id="ea534-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="ea534-119">Input Object.</span></span>

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

### <span data-ttu-id="ea534-120">-位置</span><span class="sxs-lookup"><span data-stu-id="ea534-120">-Location</span></span>
<span data-ttu-id="ea534-121">位置。</span><span class="sxs-lookup"><span data-stu-id="ea534-121">Location.</span></span>

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

### <span data-ttu-id="ea534-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="ea534-122">-Name</span></span>
<span data-ttu-id="ea534-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ea534-123">Resource name.</span></span>

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

### <span data-ttu-id="ea534-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea534-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea534-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ea534-125">Resource group name.</span></span>

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

### <span data-ttu-id="ea534-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea534-126">-ResourceId</span></span>
<span data-ttu-id="ea534-127">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ea534-127">Resource ID.</span></span>

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

### <span data-ttu-id="ea534-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ea534-128">-VirtualMachine</span></span>
<span data-ttu-id="ea534-129">自動提供。</span><span class="sxs-lookup"><span data-stu-id="ea534-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="ea534-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ea534-130">-Confirm</span></span>
<span data-ttu-id="ea534-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ea534-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea534-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea534-132">-WhatIf</span></span>
<span data-ttu-id="ea534-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ea534-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea534-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ea534-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea534-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea534-135">CommonParameters</span></span>
<span data-ttu-id="ea534-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ea534-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea534-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ea534-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea534-138">輸入</span><span class="sxs-lookup"><span data-stu-id="ea534-138">INPUTS</span></span>

### <span data-ttu-id="ea534-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ea534-139">System.String</span></span>

### <span data-ttu-id="ea534-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span><span class="sxs-lookup"><span data-stu-id="ea534-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="ea534-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ea534-141">OUTPUTS</span></span>

### <span data-ttu-id="ea534-142">Microsoft.Azure.Commands.Security.models.JitNetworkAccesssPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ea534-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ea534-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ea534-143">NOTES</span></span>

## <span data-ttu-id="ea534-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea534-144">RELATED LINKS</span></span>
