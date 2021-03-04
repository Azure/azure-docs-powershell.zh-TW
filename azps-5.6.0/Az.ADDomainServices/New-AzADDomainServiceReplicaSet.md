---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.ADDomainServices/new-AzADDomainServiceReplicaSet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainServiceReplicaSet.md
ms.openlocfilehash: ad11cbe364cd4d9cd8a667fd40a6a1d438f1aed4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910569"
---
# <span data-ttu-id="1de8f-101">New-AzADDomainServiceReplicaSet</span><span class="sxs-lookup"><span data-stu-id="1de8f-101">New-AzADDomainServiceReplicaSet</span></span>

## <span data-ttu-id="1de8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1de8f-102">SYNOPSIS</span></span>
<span data-ttu-id="1de8f-103">為複本集建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="1de8f-103">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="1de8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="1de8f-104">SYNTAX</span></span>

```
New-AzADDomainServiceReplicaSet [-Location <String>] [-SubnetId <String>] [<CommonParameters>]
```

## <span data-ttu-id="1de8f-105">描述</span><span class="sxs-lookup"><span data-stu-id="1de8f-105">DESCRIPTION</span></span>
<span data-ttu-id="1de8f-106">為複本集建立記憶體中的物件</span><span class="sxs-lookup"><span data-stu-id="1de8f-106">Create a in-memory object for ReplicaSet</span></span>

## <span data-ttu-id="1de8f-107">例子</span><span class="sxs-lookup"><span data-stu-id="1de8f-107">EXAMPLES</span></span>

### <span data-ttu-id="1de8f-108">範例 1：建立 AdDomain 的複本集</span><span class="sxs-lookup"><span data-stu-id="1de8f-108">Example 1: Create ReplicaSet for AdDomain</span></span>
```powershell
PS C:\> New-AzADDomainServiceReplicaSet -Location eastus -SubnetId /subscriptions/**********-****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/Microsoft.Network/virtualNetworks/yourinttest/subnets/default

DomainControllerIPAddress ExternalAccessIPAddress HealthLastEvaluated Location ServiceStatus SubnetId
------------------------- ----------------------- ------------------- -------- ------------- --------
                                                                      eastus                 /subscriptions/****
                                                                      ****-****-****-****-**********/resourceGroups/youriADDomain-rg-test/providers/M…
```

<span data-ttu-id="1de8f-109">建立 AdDomain 的複本集</span><span class="sxs-lookup"><span data-stu-id="1de8f-109">Create ReplicaSet for AdDomain</span></span>

## <span data-ttu-id="1de8f-110">參數</span><span class="sxs-lookup"><span data-stu-id="1de8f-110">PARAMETERS</span></span>

### <span data-ttu-id="1de8f-111">-位置</span><span class="sxs-lookup"><span data-stu-id="1de8f-111">-Location</span></span>
<span data-ttu-id="1de8f-112">虛擬網路位置。</span><span class="sxs-lookup"><span data-stu-id="1de8f-112">Virtual network location.</span></span>

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

### <span data-ttu-id="1de8f-113">-子網Id</span><span class="sxs-lookup"><span data-stu-id="1de8f-113">-SubnetId</span></span>
<span data-ttu-id="1de8f-114">網域服務將部署在的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="1de8f-114">The name of the virtual network that Domain Services will be deployed on.</span></span>
<span data-ttu-id="1de8f-115">網域服務將部署之子網的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1de8f-115">The id of the subnet that Domain Services will be deployed on.</span></span>
<span data-ttu-id="1de8f-116">/virtualNetwork/vnetName/子網/子網名稱。</span><span class="sxs-lookup"><span data-stu-id="1de8f-116">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

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

### <span data-ttu-id="1de8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de8f-117">CommonParameters</span></span>
<span data-ttu-id="1de8f-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1de8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de8f-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1de8f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de8f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="1de8f-120">INPUTS</span></span>

## <span data-ttu-id="1de8f-121">輸出</span><span class="sxs-lookup"><span data-stu-id="1de8f-121">OUTPUTS</span></span>

### <span data-ttu-id="1de8f-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.models.Api202001.複本集</span><span class="sxs-lookup"><span data-stu-id="1de8f-122">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.ReplicaSet</span></span>

## <span data-ttu-id="1de8f-123">筆記</span><span class="sxs-lookup"><span data-stu-id="1de8f-123">NOTES</span></span>

<span data-ttu-id="1de8f-124">別名</span><span class="sxs-lookup"><span data-stu-id="1de8f-124">ALIASES</span></span>

## <span data-ttu-id="1de8f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="1de8f-125">RELATED LINKS</span></span>

