---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: e82c540b946408671c424a1f86d3266a7e6d6906
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127183"
---
# <span data-ttu-id="2a4f3-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2a4f3-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2a4f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4f3-103">取得 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="2a4f3-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="2a4f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a4f3-104">SYNTAX</span></span>

### <span data-ttu-id="2a4f3-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="2a4f3-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4f3-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="2a4f3-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a4f3-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="2a4f3-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4f3-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4f3-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a4f3-109">說明</span><span class="sxs-lookup"><span data-stu-id="2a4f3-109">DESCRIPTION</span></span>
<span data-ttu-id="2a4f3-110">即時 (JIT) 網路存取原則可讓您定義原則，就能讓簡單的使用者建立到 VM 的臨時性網路連線。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="2a4f3-111">原則定義哪些埠、通訊協定和來源 IP 位址可以要求與 VM 的連線，以及在連線自動關閉前的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="2a4f3-112">在原則中，您也可以看到與此原則建立的連線要求。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="2a4f3-113">示例</span><span class="sxs-lookup"><span data-stu-id="2a4f3-113">EXAMPLES</span></span>

### <span data-ttu-id="2a4f3-114">範例1</span><span class="sxs-lookup"><span data-stu-id="2a4f3-114">Example 1</span></span>
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

<span data-ttu-id="2a4f3-115">取得訂閱上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="2a4f3-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="2a4f3-116">範例2</span><span class="sxs-lookup"><span data-stu-id="2a4f3-116">Example 2</span></span>
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

<span data-ttu-id="2a4f3-117">取得「myService1」資源群組上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="2a4f3-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="2a4f3-118">範例3</span><span class="sxs-lookup"><span data-stu-id="2a4f3-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="2a4f3-119">取得特定的 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="2a4f3-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="2a4f3-120">參數</span><span class="sxs-lookup"><span data-stu-id="2a4f3-120">PARAMETERS</span></span>

### <span data-ttu-id="2a4f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4f3-121">-DefaultProfile</span></span>
<span data-ttu-id="2a4f3-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4f3-123">-位置</span><span class="sxs-lookup"><span data-stu-id="2a4f3-123">-Location</span></span>
<span data-ttu-id="2a4f3-124">位於.</span><span class="sxs-lookup"><span data-stu-id="2a4f3-124">Location.</span></span>

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

### <span data-ttu-id="2a4f3-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a4f3-125">-Name</span></span>
<span data-ttu-id="2a4f3-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-126">Resource name.</span></span>

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

### <span data-ttu-id="2a4f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a4f3-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-128">Resource group name.</span></span>

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

### <span data-ttu-id="2a4f3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4f3-129">-ResourceId</span></span>
<span data-ttu-id="2a4f3-130">Jit 網路存取原則資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="2a4f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4f3-131">CommonParameters</span></span>
<span data-ttu-id="2a4f3-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4f3-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4f3-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2a4f3-134">INPUTS</span></span>

### <span data-ttu-id="2a4f3-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2a4f3-135">System.String</span></span>

## <span data-ttu-id="2a4f3-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2a4f3-136">OUTPUTS</span></span>

### <span data-ttu-id="2a4f3-137">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="2a4f3-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="2a4f3-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2a4f3-138">NOTES</span></span>

## <span data-ttu-id="2a4f3-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a4f3-139">RELATED LINKS</span></span>
