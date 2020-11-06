---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Start-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 62dccdc3b55caa5d63036ed3298caa5a01514342
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452720"
---
# <span data-ttu-id="03a6a-101">Start-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03a6a-101">Start-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="03a6a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="03a6a-103">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="03a6a-103">Invokes a temporary network access request.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03a6a-104">句法</span><span class="sxs-lookup"><span data-stu-id="03a6a-104">SYNTAX</span></span>

### <span data-ttu-id="03a6a-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="03a6a-105">ResourceGroupLevelResource (Default)</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a6a-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="03a6a-106">ResourceId</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -VirtualMachine <PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03a6a-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="03a6a-107">InputObject</span></span>
```
Start-AzureRmJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicyInitiateInputObject>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03a6a-108">說明</span><span class="sxs-lookup"><span data-stu-id="03a6a-108">DESCRIPTION</span></span>
<span data-ttu-id="03a6a-109">調用暫時的網路存取要求。</span><span class="sxs-lookup"><span data-stu-id="03a6a-109">Invokes a temporary network access request.</span></span>
<span data-ttu-id="03a6a-110">針對設定的 JIT 網路存取原則驗證要求，如果 permittet，則會根據使用者的要求開啟網路連線。</span><span class="sxs-lookup"><span data-stu-id="03a6a-110">The request is validated against the configured JIT network access policy and if permittet, opens up a network connection according to the user's request.</span></span>
<span data-ttu-id="03a6a-111">此要求將會在原則中 loged，以供日後查看，並會在超過指定的持續時間時終止。</span><span class="sxs-lookup"><span data-stu-id="03a6a-111">The request will be loged in the policy for later review and will be terminated when the specified duration will be exceeded.</span></span>

## <span data-ttu-id="03a6a-112">示例</span><span class="sxs-lookup"><span data-stu-id="03a6a-112">EXAMPLES</span></span>

### <span data-ttu-id="03a6a-113">範例1</span><span class="sxs-lookup"><span data-stu-id="03a6a-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -Kind "Basic" -VirtualMachine $vms

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.S
                    ecurity/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.
                    Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="03a6a-114">根據指定的連線要求資料開啟網路連線。</span><span class="sxs-lookup"><span data-stu-id="03a6a-114">Opens up a network connection according to the specified connection request data.</span></span>

## <span data-ttu-id="03a6a-115">參數</span><span class="sxs-lookup"><span data-stu-id="03a6a-115">PARAMETERS</span></span>

### <span data-ttu-id="03a6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a6a-116">-DefaultProfile</span></span>
<span data-ttu-id="03a6a-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03a6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03a6a-118">-InputObject</span></span>
<span data-ttu-id="03a6a-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="03a6a-119">Input Object.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-120">-位置</span><span class="sxs-lookup"><span data-stu-id="03a6a-120">-Location</span></span>
<span data-ttu-id="03a6a-121">位於.</span><span class="sxs-lookup"><span data-stu-id="03a6a-121">Location.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="03a6a-122">-Name</span></span>
<span data-ttu-id="03a6a-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="03a6a-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03a6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="03a6a-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="03a6a-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03a6a-126">-ResourceId</span></span>
<span data-ttu-id="03a6a-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="03a6a-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-128">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="03a6a-128">-VirtualMachine</span></span>
<span data-ttu-id="03a6a-129">自動提供。</span><span class="sxs-lookup"><span data-stu-id="03a6a-129">Automatic Provisioning.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]
Parameter Sets: ResourceGroupLevelResource, ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="03a6a-130">-Confirm</span></span>
<span data-ttu-id="03a6a-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03a6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03a6a-132">-WhatIf</span></span>
<span data-ttu-id="03a6a-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03a6a-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03a6a-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03a6a-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03a6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a6a-135">CommonParameters</span></span>
<span data-ttu-id="03a6a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03a6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a6a-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03a6a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a6a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="03a6a-138">INPUTS</span></span>

### <span data-ttu-id="03a6a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="03a6a-139">System.String</span></span>
<span data-ttu-id="03a6a-140">PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine []. JitNetworkAccessPolicies. []</span><span class="sxs-lookup"><span data-stu-id="03a6a-140">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyInitiateVirtualMachine[]</span></span>

## <span data-ttu-id="03a6a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="03a6a-141">OUTPUTS</span></span>

### <span data-ttu-id="03a6a-142">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="03a6a-142">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="03a6a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="03a6a-143">NOTES</span></span>

## <span data-ttu-id="03a6a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="03a6a-144">RELATED LINKS</span></span>
