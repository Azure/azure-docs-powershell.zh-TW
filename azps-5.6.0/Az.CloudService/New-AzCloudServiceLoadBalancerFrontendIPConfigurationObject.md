---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: 5628b7819789ba97ee56a0c69f65e371f9b35e7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910530"
---
# <span data-ttu-id="fd6a2-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="fd6a2-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="fd6a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="fd6a2-103">為 LoadBalancerFrontendIPConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="fd6a2-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="fd6a2-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd6a2-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd6a2-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd6a2-105">DESCRIPTION</span></span>
<span data-ttu-id="fd6a2-106">為 LoadBalancerFrontendIPConfiguration 建立記憶體內物件</span><span class="sxs-lookup"><span data-stu-id="fd6a2-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="fd6a2-107">例子</span><span class="sxs-lookup"><span data-stu-id="fd6a2-107">EXAMPLES</span></span>

### <span data-ttu-id="fd6a2-108">範例 1：建立負載平衡器前端 IP 組組物件</span><span class="sxs-lookup"><span data-stu-id="fd6a2-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="fd6a2-109">此命令會建立負載平衡器前端 IP 組組物件，用於建立或更新雲端服務。</span><span class="sxs-lookup"><span data-stu-id="fd6a2-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="fd6a2-110">詳情請參閱 New-AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="fd6a2-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="fd6a2-111">參數</span><span class="sxs-lookup"><span data-stu-id="fd6a2-111">PARAMETERS</span></span>

### <span data-ttu-id="fd6a2-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd6a2-112">-Name</span></span>
<span data-ttu-id="fd6a2-113">FrontendIpConfigration 的名稱。</span><span class="sxs-lookup"><span data-stu-id="fd6a2-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="fd6a2-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="fd6a2-114">-PublicIPAddressId</span></span>
<span data-ttu-id="fd6a2-115">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="fd6a2-115">Resource Id.</span></span>

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

### <span data-ttu-id="fd6a2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd6a2-116">CommonParameters</span></span>
<span data-ttu-id="fd6a2-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd6a2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd6a2-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd6a2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd6a2-119">輸入</span><span class="sxs-lookup"><span data-stu-id="fd6a2-119">INPUTS</span></span>

## <span data-ttu-id="fd6a2-120">輸出</span><span class="sxs-lookup"><span data-stu-id="fd6a2-120">OUTPUTS</span></span>

### <span data-ttu-id="fd6a2-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fd6a2-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="fd6a2-122">筆記</span><span class="sxs-lookup"><span data-stu-id="fd6a2-122">NOTES</span></span>

<span data-ttu-id="fd6a2-123">別名</span><span class="sxs-lookup"><span data-stu-id="fd6a2-123">ALIASES</span></span>

## <span data-ttu-id="fd6a2-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd6a2-124">RELATED LINKS</span></span>

