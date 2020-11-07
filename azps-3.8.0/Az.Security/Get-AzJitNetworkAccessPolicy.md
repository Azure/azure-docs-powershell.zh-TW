---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c54f3df57739b4a68620aa1f7f3d700746369a60
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958423"
---
# <span data-ttu-id="ab982-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ab982-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ab982-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab982-102">SYNOPSIS</span></span>
<span data-ttu-id="ab982-103">取得 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="ab982-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="ab982-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab982-104">SYNTAX</span></span>

### <span data-ttu-id="ab982-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ab982-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab982-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="ab982-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab982-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="ab982-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab982-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab982-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab982-109">說明</span><span class="sxs-lookup"><span data-stu-id="ab982-109">DESCRIPTION</span></span>
<span data-ttu-id="ab982-110">即時 (JIT) 網路存取原則可讓您定義原則，就能讓簡單的使用者建立到 VM 的臨時性網路連線。</span><span class="sxs-lookup"><span data-stu-id="ab982-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="ab982-111">原則定義哪些埠、通訊協定和來源 IP 位址可以要求與 VM 的連線，以及在連線自動關閉前的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="ab982-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="ab982-112">在原則中，您也可以看到與此原則建立的連線要求。</span><span class="sxs-lookup"><span data-stu-id="ab982-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="ab982-113">示例</span><span class="sxs-lookup"><span data-stu-id="ab982-113">EXAMPLES</span></span>

### <span data-ttu-id="ab982-114">範例1</span><span class="sxs-lookup"><span data-stu-id="ab982-114">Example 1</span></span>
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

<span data-ttu-id="ab982-115">取得訂閱上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="ab982-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="ab982-116">範例2</span><span class="sxs-lookup"><span data-stu-id="ab982-116">Example 2</span></span>
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

<span data-ttu-id="ab982-117">取得「myService1」資源群組上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="ab982-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="ab982-118">範例3</span><span class="sxs-lookup"><span data-stu-id="ab982-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="ab982-119">取得特定的 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="ab982-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="ab982-120">參數</span><span class="sxs-lookup"><span data-stu-id="ab982-120">PARAMETERS</span></span>

### <span data-ttu-id="ab982-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab982-121">-DefaultProfile</span></span>
<span data-ttu-id="ab982-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab982-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab982-123">-位置</span><span class="sxs-lookup"><span data-stu-id="ab982-123">-Location</span></span>
<span data-ttu-id="ab982-124">位於.</span><span class="sxs-lookup"><span data-stu-id="ab982-124">Location.</span></span>

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

### <span data-ttu-id="ab982-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab982-125">-Name</span></span>
<span data-ttu-id="ab982-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ab982-126">Resource name.</span></span>

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

### <span data-ttu-id="ab982-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab982-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab982-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ab982-128">Resource group name.</span></span>

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

### <span data-ttu-id="ab982-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab982-129">-ResourceId</span></span>
<span data-ttu-id="ab982-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ab982-130">Resource ID.</span></span>

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

### <span data-ttu-id="ab982-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab982-131">CommonParameters</span></span>
<span data-ttu-id="ab982-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab982-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab982-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab982-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab982-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ab982-134">INPUTS</span></span>

### <span data-ttu-id="ab982-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ab982-135">System.String</span></span>

## <span data-ttu-id="ab982-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ab982-136">OUTPUTS</span></span>

### <span data-ttu-id="ab982-137">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="ab982-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="ab982-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ab982-138">NOTES</span></span>

## <span data-ttu-id="ab982-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab982-139">RELATED LINKS</span></span>
