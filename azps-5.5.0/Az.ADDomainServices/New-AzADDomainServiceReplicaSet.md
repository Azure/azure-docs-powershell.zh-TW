---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: f95c4148afa3f317914dabe968376e0e86913dcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127311"
---
# <span data-ttu-id="08509-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="08509-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="08509-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08509-102">SYNOPSIS</span></span>
<span data-ttu-id="08509-103">為 ReplicaSet 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="08509-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="08509-104">句法</span><span class="sxs-lookup"><span data-stu-id="08509-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="08509-105">說明</span><span class="sxs-lookup"><span data-stu-id="08509-105">DESCRIPTION</span></span>
<span data-ttu-id="08509-106">為 ReplicaSet 建立記憶體內建物件</span><span class="sxs-lookup"><span data-stu-id="08509-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="08509-107">示例</span><span class="sxs-lookup"><span data-stu-id="08509-107">EXAMPLES</span></span>

### <span data-ttu-id="08509-108">範例1：建立 AdDomain 的 ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="08509-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="08509-109">建立 AdDomain 的 ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="08509-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="08509-110">參數</span><span class="sxs-lookup"><span data-stu-id="08509-110">PARAMETERS</span></span>

### <span data-ttu-id="08509-111">-位置</span><span class="sxs-lookup"><span data-stu-id="08509-111">-Location</span></span>
<span data-ttu-id="08509-112">虛擬網路位置。</span><span class="sxs-lookup"><span data-stu-id="08509-112">Virtual network location.</span></span>

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

### <span data-ttu-id="08509-113">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="08509-113">-SubnetId</span></span>
<span data-ttu-id="08509-114">您要在其上部署網域服務的虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="08509-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="08509-115">要在其上部署網域服務的子網之 id。</span><span class="sxs-lookup"><span data-stu-id="08509-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="08509-116">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="08509-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="08509-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08509-117">CommonParameters</span></span>
<span data-ttu-id="08509-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08509-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08509-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="08509-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08509-120">輸入</span><span class="sxs-lookup"><span data-stu-id="08509-120">INPUTS</span></span>

## <span data-ttu-id="08509-121">輸出</span><span class="sxs-lookup"><span data-stu-id="08509-121">OUTPUTS</span></span>

### <span data-ttu-id="08509-122">ReplicaSet （ADDomainServices）。 Api202001。</span><span class="sxs-lookup"><span data-stu-id="08509-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="08509-123">筆記</span><span class="sxs-lookup"><span data-stu-id="08509-123">NOTES</span></span>

<span data-ttu-id="08509-124">別名</span><span class="sxs-lookup"><span data-stu-id="08509-124">ALIASES</span></span>

## <span data-ttu-id="08509-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="08509-125">RELATED LINKS</span></span>

