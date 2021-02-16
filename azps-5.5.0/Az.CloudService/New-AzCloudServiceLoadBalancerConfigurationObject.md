---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerConfigurationObject.md
ms.openlocfilehash: 6afabb94ae006cec122d7e89997be17c20e85b05
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138730"
---
# <span data-ttu-id="bc2d6-101">New-AzCloudServiceLoadBalancerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="bc2d6-101">New-AzCloudServiceLoadBalancerConfigurationObject</span></span>

## <span data-ttu-id="bc2d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc2d6-103">為 LoadBalancerConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="bc2d6-103">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="bc2d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc2d6-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerConfigurationObject
 [-FrontendIPConfiguration <ILoadBalancerFrontendIPConfiguration[]>] [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="bc2d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="bc2d6-105">DESCRIPTION</span></span>
<span data-ttu-id="bc2d6-106">為 LoadBalancerConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="bc2d6-106">Create a in-memory object for LoadBalancerConfiguration</span></span>

## <span data-ttu-id="bc2d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="bc2d6-107">EXAMPLES</span></span>

### <span data-ttu-id="bc2d6-108">範例1：建立負載平衡器設定物件</span><span class="sxs-lookup"><span data-stu-id="bc2d6-108">Example 1: Create load balancer configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIP.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="bc2d6-109">這個命令會建立用來建立或更新雲端服務的負載平衡器設定物件。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-109">This command creates load balancer configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="bc2d6-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="bc2d6-111">參數</span><span class="sxs-lookup"><span data-stu-id="bc2d6-111">PARAMETERS</span></span>

### <span data-ttu-id="bc2d6-112">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bc2d6-112">-FrontendIPConfiguration</span></span>
<span data-ttu-id="bc2d6-113">FrontendIPConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc2d6-113">FrontendIPConfiguration.</span></span>
<span data-ttu-id="bc2d6-114">若要建立，請參閱 FRONTENDIPCONFIGURATION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-114">To construct, see NOTES section for FRONTENDIPCONFIGURATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc2d6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc2d6-115">-Name</span></span>
<span data-ttu-id="bc2d6-116">LoadBalancerConfiguration 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-116">Name of LoadBalancerConfiguration.</span></span>

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

### <span data-ttu-id="bc2d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc2d6-117">CommonParameters</span></span>
<span data-ttu-id="bc2d6-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc2d6-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc2d6-120">輸入</span><span class="sxs-lookup"><span data-stu-id="bc2d6-120">INPUTS</span></span>

## <span data-ttu-id="bc2d6-121">輸出</span><span class="sxs-lookup"><span data-stu-id="bc2d6-121">OUTPUTS</span></span>

### <span data-ttu-id="bc2d6-122">LoadBalancerConfiguration （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-122">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerConfiguration</span></span>

## <span data-ttu-id="bc2d6-123">筆記</span><span class="sxs-lookup"><span data-stu-id="bc2d6-123">NOTES</span></span>

<span data-ttu-id="bc2d6-124">別名</span><span class="sxs-lookup"><span data-stu-id="bc2d6-124">ALIASES</span></span>

<span data-ttu-id="bc2d6-125">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bc2d6-125">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc2d6-126">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-126">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc2d6-127">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-127">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc2d6-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration [] >： FrontendIPConfiguration。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-128">FRONTENDIPCONFIGURATION <ILoadBalancerFrontendIPConfiguration[]>: FrontendIPConfiguration.</span></span>
  - <span data-ttu-id="bc2d6-129">`[Name <String>]`:</span><span class="sxs-lookup"><span data-stu-id="bc2d6-129">`[Name <String>]`:</span></span> 
  - <span data-ttu-id="bc2d6-130">`[PrivateIPAddress <String>]`：雲端服務所參照的私人 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="bc2d6-130">`[PrivateIPAddress <String>]`: The private IP address referenced by the cloud service.</span></span>
  - <span data-ttu-id="bc2d6-131">`[PublicIPAddressId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bc2d6-131">`[PublicIPAddressId <String>]`: Resource Id</span></span>
  - <span data-ttu-id="bc2d6-132">`[SubnetId <String>]`：資源識別碼</span><span class="sxs-lookup"><span data-stu-id="bc2d6-132">`[SubnetId <String>]`: Resource Id</span></span>

## <span data-ttu-id="bc2d6-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc2d6-133">RELATED LINKS</span></span>

