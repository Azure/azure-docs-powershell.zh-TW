---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceLoadBalancerFrontendIPConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject.md
ms.openlocfilehash: cdd983e2ede5cd06c3b9b00805b337eac5b73a9b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136578"
---
# <span data-ttu-id="300df-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="300df-101">New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject</span></span>

## <span data-ttu-id="300df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="300df-102">SYNOPSIS</span></span>
<span data-ttu-id="300df-103">為 LoadBalancerFrontendIPConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="300df-103">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="300df-104">句法</span><span class="sxs-lookup"><span data-stu-id="300df-104">SYNTAX</span></span>

```
New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject [-Name <String>] [-PublicIPAddressId <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="300df-105">說明</span><span class="sxs-lookup"><span data-stu-id="300df-105">DESCRIPTION</span></span>
<span data-ttu-id="300df-106">為 LoadBalancerFrontendIPConfiguration 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="300df-106">Create a in-memory object for LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="300df-107">示例</span><span class="sxs-lookup"><span data-stu-id="300df-107">EXAMPLES</span></span>

### <span data-ttu-id="300df-108">範例1：建立負載平衡器前端 IP 設定物件</span><span class="sxs-lookup"><span data-stu-id="300df-108">Example 1: Create load balancer frontend IP configuration object</span></span>
```powershell
PS C:\> $publicIP = Get-AzPublicIpAddress -ResourceGroupName 'ContosoOrg' -Name 'ContosoPublicIP'
PS C:\> $feIpConfig = New-AzCloudServiceLoadBalancerFrontendIPConfigurationObject -Name 'ContosoFe' -PublicIPAddressId $publicIp.Id
PS C:\> $loadBalancerConfig = New-AzCloudServiceLoadBalancerConfigurationObject -Name 'ContosoLB' -FrontendIPConfiguration $feIpConfig
```

<span data-ttu-id="300df-109">這個命令會建立用來建立或更新雲端服務的負載等化器前端 IP 設定物件。</span><span class="sxs-lookup"><span data-stu-id="300df-109">This command creates load balancer frontend IP configuration object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="300df-110">如需詳細資訊，請參閱新 AzCloudService。</span><span class="sxs-lookup"><span data-stu-id="300df-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="300df-111">參數</span><span class="sxs-lookup"><span data-stu-id="300df-111">PARAMETERS</span></span>

### <span data-ttu-id="300df-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="300df-112">-Name</span></span>
<span data-ttu-id="300df-113">FrontendIpConfigration 的名稱。</span><span class="sxs-lookup"><span data-stu-id="300df-113">Name of FrontendIpConfigration.</span></span>

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

### <span data-ttu-id="300df-114">-PublicIPAddressId</span><span class="sxs-lookup"><span data-stu-id="300df-114">-PublicIPAddressId</span></span>
<span data-ttu-id="300df-115">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="300df-115">Resource Id.</span></span>

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

### <span data-ttu-id="300df-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300df-116">CommonParameters</span></span>
<span data-ttu-id="300df-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="300df-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300df-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="300df-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300df-119">輸入</span><span class="sxs-lookup"><span data-stu-id="300df-119">INPUTS</span></span>

## <span data-ttu-id="300df-120">輸出</span><span class="sxs-lookup"><span data-stu-id="300df-120">OUTPUTS</span></span>

### <span data-ttu-id="300df-121">LoadBalancerFrontendIPConfiguration （CloudService）。 Api20201001Preview。</span><span class="sxs-lookup"><span data-stu-id="300df-121">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.LoadBalancerFrontendIPConfiguration</span></span>

## <span data-ttu-id="300df-122">筆記</span><span class="sxs-lookup"><span data-stu-id="300df-122">NOTES</span></span>

<span data-ttu-id="300df-123">別名</span><span class="sxs-lookup"><span data-stu-id="300df-123">ALIASES</span></span>

## <span data-ttu-id="300df-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="300df-124">RELATED LINKS</span></span>

