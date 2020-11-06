---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445472"
---
# <span data-ttu-id="18626-101">Get-AzureRmJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="18626-101">Get-AzureRmJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="18626-102">摘要</span><span class="sxs-lookup"><span data-stu-id="18626-102">SYNOPSIS</span></span>
<span data-ttu-id="18626-103">取得 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="18626-103">Gets the JIT network access policies</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18626-104">句法</span><span class="sxs-lookup"><span data-stu-id="18626-104">SYNTAX</span></span>

### <span data-ttu-id="18626-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="18626-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18626-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="18626-106">ResourceGroupScope</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="18626-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="18626-107">ResourceGroupLevelResource</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18626-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="18626-108">ResourceId</span></span>
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="18626-109">說明</span><span class="sxs-lookup"><span data-stu-id="18626-109">DESCRIPTION</span></span>
<span data-ttu-id="18626-110">即時 (JIT) 網路存取原則可讓您定義原則，就能讓簡單的使用者建立到 VM 的臨時性網路連線。</span><span class="sxs-lookup"><span data-stu-id="18626-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="18626-111">原則定義哪些埠、通訊協定和來源 IP 位址可以要求與 VM 的連線，以及在連線自動關閉前的最大持續時間。</span><span class="sxs-lookup"><span data-stu-id="18626-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="18626-112">在原則中，您也可以看到與此原則建立的連線要求。</span><span class="sxs-lookup"><span data-stu-id="18626-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="18626-113">示例</span><span class="sxs-lookup"><span data-stu-id="18626-113">EXAMPLES</span></span>

### <span data-ttu-id="18626-114">範例1</span><span class="sxs-lookup"><span data-stu-id="18626-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
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

<span data-ttu-id="18626-115">取得訂閱上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="18626-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="18626-116">範例2</span><span class="sxs-lookup"><span data-stu-id="18626-116">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
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

<span data-ttu-id="18626-117">取得「myService1」資源群組上的所有 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="18626-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="18626-118">範例3</span><span class="sxs-lookup"><span data-stu-id="18626-118">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="18626-119">取得特定的 JIT 網路存取原則</span><span class="sxs-lookup"><span data-stu-id="18626-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="18626-120">參數</span><span class="sxs-lookup"><span data-stu-id="18626-120">PARAMETERS</span></span>

### <span data-ttu-id="18626-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18626-121">-DefaultProfile</span></span>
<span data-ttu-id="18626-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="18626-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18626-123">-位置</span><span class="sxs-lookup"><span data-stu-id="18626-123">-Location</span></span>
<span data-ttu-id="18626-124">位於.</span><span class="sxs-lookup"><span data-stu-id="18626-124">Location.</span></span>

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

### <span data-ttu-id="18626-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="18626-125">-Name</span></span>
<span data-ttu-id="18626-126">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="18626-126">Resource name.</span></span>

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

### <span data-ttu-id="18626-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18626-127">-ResourceGroupName</span></span>
<span data-ttu-id="18626-128">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="18626-128">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18626-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18626-129">-ResourceId</span></span>
<span data-ttu-id="18626-130">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="18626-130">Resource ID.</span></span>

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

### <span data-ttu-id="18626-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18626-131">CommonParameters</span></span>
<span data-ttu-id="18626-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="18626-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18626-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="18626-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18626-134">輸入</span><span class="sxs-lookup"><span data-stu-id="18626-134">INPUTS</span></span>

### <span data-ttu-id="18626-135">System.object</span><span class="sxs-lookup"><span data-stu-id="18626-135">System.String</span></span>

## <span data-ttu-id="18626-136">輸出</span><span class="sxs-lookup"><span data-stu-id="18626-136">OUTPUTS</span></span>

### <span data-ttu-id="18626-137">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="18626-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="18626-138">筆記</span><span class="sxs-lookup"><span data-stu-id="18626-138">NOTES</span></span>

## <span data-ttu-id="18626-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="18626-139">RELATED LINKS</span></span>
