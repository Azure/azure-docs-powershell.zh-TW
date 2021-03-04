---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 980b680130ca319612bbbf28e787ebd99c4bf8bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907053"
---
# <span data-ttu-id="c0ff5-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0ff5-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c0ff5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ff5-103">取得 JIT 網路存取政策</span><span class="sxs-lookup"><span data-stu-id="c0ff5-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="c0ff5-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0ff5-104">SYNTAX</span></span>

### <span data-ttu-id="c0ff5-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c0ff5-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ff5-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="c0ff5-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ff5-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c0ff5-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0ff5-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ff5-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ff5-109">描述</span><span class="sxs-lookup"><span data-stu-id="c0ff5-109">DESCRIPTION</span></span>
<span data-ttu-id="c0ff5-110">在時間 (JIT) 網路存取策略中，您可以定義允許簡單使用者建立與 VM 的暫時網路連接之策略。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="c0ff5-111">此政策會定義哪些埠、通訊協定和來源 IP 位址可以要求與 VM 建立連接，以及自動關閉連接前的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="c0ff5-112">在策略中，您也可以看到此策略所提出之連接要求。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="c0ff5-113">例子</span><span class="sxs-lookup"><span data-stu-id="c0ff5-113">EXAMPLES</span></span>

### <span data-ttu-id="c0ff5-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="c0ff5-114">Example 1</span></span>
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

<span data-ttu-id="c0ff5-115">取得訂閱上的所有 JIT 網路存取權</span><span class="sxs-lookup"><span data-stu-id="c0ff5-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="c0ff5-116">範例 2</span><span class="sxs-lookup"><span data-stu-id="c0ff5-116">Example 2</span></span>
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

<span data-ttu-id="c0ff5-117">取得 「myService1」資源群組上的所有 JIT 網路存取權</span><span class="sxs-lookup"><span data-stu-id="c0ff5-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="c0ff5-118">範例 3</span><span class="sxs-lookup"><span data-stu-id="c0ff5-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="c0ff5-119">取得特定的 JIT 網路存取策略</span><span class="sxs-lookup"><span data-stu-id="c0ff5-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="c0ff5-120">參數</span><span class="sxs-lookup"><span data-stu-id="c0ff5-120">PARAMETERS</span></span>

### <span data-ttu-id="c0ff5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ff5-121">-DefaultProfile</span></span>
<span data-ttu-id="c0ff5-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ff5-123">-位置</span><span class="sxs-lookup"><span data-stu-id="c0ff5-123">-Location</span></span>
<span data-ttu-id="c0ff5-124">位置。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-124">Location.</span></span>

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

### <span data-ttu-id="c0ff5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0ff5-125">-Name</span></span>
<span data-ttu-id="c0ff5-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-126">Resource name.</span></span>

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

### <span data-ttu-id="c0ff5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ff5-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0ff5-128">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-128">Resource group name.</span></span>

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

### <span data-ttu-id="c0ff5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ff5-129">-ResourceId</span></span>
<span data-ttu-id="c0ff5-130">jit Network Access Policy 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-130">The resource id of the jit Network Access Policy resource.</span></span>

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

### <span data-ttu-id="c0ff5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ff5-131">CommonParameters</span></span>
<span data-ttu-id="c0ff5-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0ff5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ff5-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ff5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ff5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c0ff5-134">INPUTS</span></span>

### <span data-ttu-id="c0ff5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ff5-135">System.String</span></span>

## <span data-ttu-id="c0ff5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c0ff5-136">OUTPUTS</span></span>

### <span data-ttu-id="c0ff5-137">Microsoft.Azure.Commands.Security.models.JitNetworkAccesssPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c0ff5-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="c0ff5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="c0ff5-138">NOTES</span></span>

## <span data-ttu-id="c0ff5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0ff5-139">RELATED LINKS</span></span>
