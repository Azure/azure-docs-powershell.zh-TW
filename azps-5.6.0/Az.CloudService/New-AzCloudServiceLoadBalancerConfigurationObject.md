---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 5d3acb8c03ceae44024ed8c6c52a8ee962c9861c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910533"
---
# <span data-ttu-id="5ddab-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="5ddab-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="5ddab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5ddab-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddab-103">為 LoadBalancerConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="5ddab-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="5ddab-104">語法</span><span class="sxs-lookup"><span data-stu-id="5ddab-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="5ddab-105">描述</span><span class="sxs-lookup"><span data-stu-id="5ddab-105">DESCRIPTION</span></span>
<span data-ttu-id="5ddab-106">為 LoadBalancerConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="5ddab-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="5ddab-107">例子</span><span class="sxs-lookup"><span data-stu-id="5ddab-107">EXAMPLES</span></span>

### <span data-ttu-id="5ddab-108">範例 1：建立負載平衡器組組物件</span><span class="sxs-lookup"><span data-stu-id="5ddab-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="5ddab-109">此命令會建立負載平衡器組組物件，用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="5ddab-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="5ddab-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="5ddab-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="5ddab-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ddab-111">PARAMETERS</span></span>

### <span data-ttu-id="5ddab-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ddab-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5ddab-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ddab-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="5ddab-114">若要建構，請參閱 FRONTENDIPCONFIGURATION 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5ddab-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ILoadBalancerFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddab-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ddab-115">-Name</span></span>
<span data-ttu-id="5ddab-116">LoadBalancerConfiguration 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ddab-116">Name of LoadBalancerConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ddab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddab-117">CommonParameters</span></span>
<span data-ttu-id="5ddab-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5ddab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddab-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ddab-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddab-120">輸入</span><span class="sxs-lookup"><span data-stu-id="5ddab-120">INPUTS</span></span>

## <span data-ttu-id="5ddab-121">輸出</span><span class="sxs-lookup"><span data-stu-id="5ddab-121">OUTPUTS</span></span>

### <span data-ttu-id="5ddab-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.LoadBalancerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ddab-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="5ddab-123">筆記</span><span class="sxs-lookup"><span data-stu-id="5ddab-123">NOTES</span></span>

<span data-ttu-id="5ddab-124">別名</span><span class="sxs-lookup"><span data-stu-id="5ddab-124">ALIASES</span></span>

<span data-ttu-id="5ddab-125">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5ddab-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ddab-126">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5ddab-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ddab-127">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5ddab-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ddab-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>：FrontendIPConfiguration。</span><span class="sxs-lookup"><span data-stu-id="5ddab-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="5ddab-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="5ddab-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="5ddab-130">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="5ddab-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="5ddab-131">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5ddab-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="5ddab-132">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="5ddab-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="5ddab-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ddab-133">RELATED LINKS</span></span>

