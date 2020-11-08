---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129926"
---
# <span data-ttu-id="c03cb-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c03cb-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c03cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c03cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c03cb-103">取得 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="c03cb-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="c03cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="c03cb-104">SYNTAX</span></span>

### <span data-ttu-id="c03cb-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c03cb-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c03cb-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="c03cb-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c03cb-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c03cb-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c03cb-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c03cb-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c03cb-109">說明</span><span class="sxs-lookup"><span data-stu-id="c03cb-109">DESCRIPTION</span></span>
<span data-ttu-id="c03cb-110">即時 (JIT) 網路存取原則可讓您定義原則，就能讓簡單的使用者建立到 VM 的臨時性網路連線。</span><span class="sxs-lookup"><span data-stu-id="c03cb-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="c03cb-111">原則定義哪些埠、通訊協定和來源 IP 位址可以要求與 VM 的連線，以及在連線自動關閉前的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="c03cb-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="c03cb-112">在原則中，您也可以看到與此原則建立的連線要求。</span><span class="sxs-lookup"><span data-stu-id="c03cb-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="c03cb-113">示例</span><span class="sxs-lookup"><span data-stu-id="c03cb-113">EXAMPLES</span></span>

### <span data-ttu-id="c03cb-114">範例1</span><span class="sxs-lookup"><span data-stu-id="c03cb-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="c03cb-115">取得訂閱上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="c03cb-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="c03cb-116">範例2</span><span class="sxs-lookup"><span data-stu-id="c03cb-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="c03cb-117">取得「myService1」資源群組上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="c03cb-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="c03cb-118">範例3</span><span class="sxs-lookup"><span data-stu-id="c03cb-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="c03cb-119">取得特定的 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="c03cb-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="c03cb-120">參數</span><span class="sxs-lookup"><span data-stu-id="c03cb-120">PARAMETERS</span></span>

### <span data-ttu-id="c03cb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03cb-121">-DefaultProfile</span></span>
<span data-ttu-id="c03cb-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c03cb-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c03cb-123">-位置</span><span class="sxs-lookup"><span data-stu-id="c03cb-123">-Location</span></span>
<span data-ttu-id="c03cb-124">位於.</span><span class="sxs-lookup"><span data-stu-id="c03cb-124">Location.</span></span>

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

### <span data-ttu-id="c03cb-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c03cb-125">-Name</span></span>
<span data-ttu-id="c03cb-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c03cb-126">Resource name.</span></span>

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

### <span data-ttu-id="c03cb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c03cb-127">-ResourceGroupName</span></span>
<span data-ttu-id="c03cb-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c03cb-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c03cb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c03cb-129">-ResourceId</span></span>
<span data-ttu-id="c03cb-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c03cb-130">Resource ID.</span></span>

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

### <span data-ttu-id="c03cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03cb-131">CommonParameters</span></span>
<span data-ttu-id="c03cb-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c03cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03cb-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c03cb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03cb-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c03cb-134">INPUTS</span></span>

### <span data-ttu-id="c03cb-135">System.object</span><span class="sxs-lookup"><span data-stu-id="c03cb-135">System.String</span></span>

## <span data-ttu-id="c03cb-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c03cb-136">OUTPUTS</span></span>

### <span data-ttu-id="c03cb-137">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="c03cb-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c03cb-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c03cb-138">NOTES</span></span>

## <span data-ttu-id="c03cb-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c03cb-139">RELATED LINKS</span></span>
