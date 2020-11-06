---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: 72e3cf48f112c5e9bb07a8f7eb57dfe3d4c9ee07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448221"
---
# <span data-ttu-id="53770-101">Set-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="53770-101">Set-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="53770-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53770-102">SYNOPSIS</span></span>
<span data-ttu-id="53770-103">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="53770-103">Updates JIT network access policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53770-104">句法</span><span class="sxs-lookup"><span data-stu-id="53770-104">SYNTAX</span></span>

```
Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 -VirtualMachine <PSSecurityJitNetworkAccessPolicyVirtualMachine[]> -Kind <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53770-105">說明</span><span class="sxs-lookup"><span data-stu-id="53770-105">DESCRIPTION</span></span>
<span data-ttu-id="53770-106">更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="53770-106">Updates JIT network access policy.</span></span>

## <span data-ttu-id="53770-107">示例</span><span class="sxs-lookup"><span data-stu-id="53770-107">EXAMPLES</span></span>

### <span data-ttu-id="53770-108">範例1</span><span class="sxs-lookup"><span data-stu-id="53770-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default" -VirtualMachine $vmRules -Kind "Basic"

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {}
ProvisioningState : Succeeded
```

<span data-ttu-id="53770-109">使用新的 VM 規則更新 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="53770-109">Updates a JIT network access policy with new VM rules.</span></span>

## <span data-ttu-id="53770-110">參數</span><span class="sxs-lookup"><span data-stu-id="53770-110">PARAMETERS</span></span>

### <span data-ttu-id="53770-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53770-111">-DefaultProfile</span></span>
<span data-ttu-id="53770-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53770-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53770-113">類型</span><span class="sxs-lookup"><span data-stu-id="53770-113">-Kind</span></span>
<span data-ttu-id="53770-114">明示.</span><span class="sxs-lookup"><span data-stu-id="53770-114">Kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53770-115">-位置</span><span class="sxs-lookup"><span data-stu-id="53770-115">-Location</span></span>
<span data-ttu-id="53770-116">位於.</span><span class="sxs-lookup"><span data-stu-id="53770-116">Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53770-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="53770-117">-Name</span></span>
<span data-ttu-id="53770-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="53770-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53770-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53770-119">-ResourceGroupName</span></span>
<span data-ttu-id="53770-120">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="53770-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53770-121">-VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="53770-121">-VirtualMachine</span></span>
<span data-ttu-id="53770-122">虛擬電腦。</span><span class="sxs-lookup"><span data-stu-id="53770-122">Virutal Machines.</span></span>

```yaml
Type: PSSecurityJitNetworkAccessPolicyVirtualMachine[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53770-123">-確認</span><span class="sxs-lookup"><span data-stu-id="53770-123">-Confirm</span></span>
<span data-ttu-id="53770-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="53770-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53770-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53770-125">-WhatIf</span></span>
<span data-ttu-id="53770-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="53770-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53770-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53770-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53770-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53770-128">CommonParameters</span></span>
<span data-ttu-id="53770-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53770-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53770-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53770-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53770-131">輸入</span><span class="sxs-lookup"><span data-stu-id="53770-131">INPUTS</span></span>

### <span data-ttu-id="53770-132">System.object</span><span class="sxs-lookup"><span data-stu-id="53770-132">System.String</span></span>
<span data-ttu-id="53770-133">PSSecurityJitNetworkAccessPolicyVirtualMachine []. JitNetworkAccessPolicies. []</span><span class="sxs-lookup"><span data-stu-id="53770-133">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyVirtualMachine[]</span></span>

## <span data-ttu-id="53770-134">輸出</span><span class="sxs-lookup"><span data-stu-id="53770-134">OUTPUTS</span></span>

### <span data-ttu-id="53770-135">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="53770-135">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="53770-136">筆記</span><span class="sxs-lookup"><span data-stu-id="53770-136">NOTES</span></span>

## <span data-ttu-id="53770-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="53770-137">RELATED LINKS</span></span>
