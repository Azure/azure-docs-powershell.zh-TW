---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Start-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Start-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 188d653f58644a359f20886e96791efa53ab7b2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791073"
---
# <span data-ttu-id="adccb-101">Start-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="adccb-101">Start-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="adccb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="adccb-102">SYNOPSIS</span></span>
<span data-ttu-id="adccb-103">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="adccb-103">Invokes a temporary network access request.</span></span>

## <span data-ttu-id="adccb-104">句法</span><span class="sxs-lookup"><span data-stu-id="adccb-104">SYNTAX</span></span>

### <span data-ttu-id="adccb-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="adccb-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adccb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="adccb-106">ResourceId</span></span>
```
Start-AzJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adccb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="adccb-107">InputObject</span></span>
```
Start-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adccb-108">說明</span><span class="sxs-lookup"><span data-stu-id="adccb-108">DESCRIPTION</span></span>
<span data-ttu-id="adccb-109">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="adccb-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="adccb-110">針對設定的 JIT 網路存取原則驗證要求，並視使用者的要求開啟網路連線。</span><span class="sxs-lookup"><span data-stu-id="adccb-110">The request is validated against the configured JIT network access policy and if permitted, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="adccb-111">該要求將會記錄在原則中供日後查看，且會在超過指定的持續時間之後終止。</span><span class="sxs-lookup"><span data-stu-id="adccb-111">The request will be logged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="adccb-112">示例</span><span class="sxs-lookup"><span data-stu-id="adccb-112">EXAMPLES</span></span>

### <span data-ttu-id="adccb-113">範例1</span><span class="sxs-lookup"><span data-stu-id="adccb-113">Example 1</span></span>
```powershell
PS C:\> Set-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="adccb-114">根據指定的連線要求資料開啟網路連線。</span><span class="sxs-lookup"><span data-stu-id="adccb-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="adccb-115">參數</span><span class="sxs-lookup"><span data-stu-id="adccb-115">PARAMETERS</span></span>

### <span data-ttu-id="adccb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adccb-116">-DefaultProfile</span></span>
<span data-ttu-id="adccb-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="adccb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adccb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adccb-118">-InputObject</span></span>
<span data-ttu-id="adccb-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="adccb-119">Input Object.</span></span>

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

### <span data-ttu-id="adccb-120">-位置</span><span class="sxs-lookup"><span data-stu-id="adccb-120">-Location</span></span>
<span data-ttu-id="adccb-121">位於.</span><span class="sxs-lookup"><span data-stu-id="adccb-121">Location.</span></span>

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

### <span data-ttu-id="adccb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="adccb-122">-Name</span></span>
<span data-ttu-id="adccb-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="adccb-123">Resource name.</span></span>

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

### <span data-ttu-id="adccb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adccb-124">-ResourceGroupName</span></span>
<span data-ttu-id="adccb-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="adccb-125">Resource group name.</span></span>

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

### <span data-ttu-id="adccb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adccb-126">-ResourceId</span></span>
<span data-ttu-id="adccb-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="adccb-127">Resource ID.</span></span>

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

### <span data-ttu-id="adccb-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="adccb-128">-VirtualMachine</span></span>
<span data-ttu-id="adccb-129">自動提供。</span><span class="sxs-lookup"><span data-stu-id="adccb-129">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="adccb-130">-確認</span><span class="sxs-lookup"><span data-stu-id="adccb-130">-Confirm</span></span>
<span data-ttu-id="adccb-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="adccb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adccb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adccb-132">-WhatIf</span></span>
<span data-ttu-id="adccb-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="adccb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adccb-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="adccb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adccb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adccb-135">CommonParameters</span></span>
<span data-ttu-id="adccb-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="adccb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adccb-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="adccb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adccb-138">輸入</span><span class="sxs-lookup"><span data-stu-id="adccb-138">INPUTS</span></span>

### <span data-ttu-id="adccb-139">System.object</span><span class="sxs-lookup"><span data-stu-id="adccb-139">System.String</span></span>

### <span data-ttu-id="adccb-140">PSSecurityJitNetworkAccessPolicyInitiateInputObject 中的 JitNetworkAccessPolicies （）</span><span class="sxs-lookup"><span data-stu-id="adccb-140">Microsoft.Azure.Commands.Security.Cmdlets.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateInputObject</span></span>

## <span data-ttu-id="adccb-141">輸出</span><span class="sxs-lookup"><span data-stu-id="adccb-141">OUTPUTS</span></span>

### <span data-ttu-id="adccb-142">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="adccb-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="adccb-143">筆記</span><span class="sxs-lookup"><span data-stu-id="adccb-143">NOTES</span></span>

## <span data-ttu-id="adccb-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="adccb-144">RELATED LINKS</span></span>
