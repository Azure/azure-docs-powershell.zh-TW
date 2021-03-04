---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 2b5cc008e96d12828d5f834fd5fa4a30f83ea70f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905910"
---
# <span data-ttu-id="020ee-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="020ee-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="020ee-102">簡介</span><span class="sxs-lookup"><span data-stu-id="020ee-102">SYNOPSIS</span></span>
<span data-ttu-id="020ee-103">獲得 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="020ee-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="020ee-104">語法</span><span class="sxs-lookup"><span data-stu-id="020ee-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="020ee-105">描述</span><span class="sxs-lookup"><span data-stu-id="020ee-105">DESCRIPTION</span></span>
<span data-ttu-id="020ee-106">此Get-AzDdosProtectionPlan Cmdlet 會獲得 DDoS 保護計劃。</span><span class="sxs-lookup"><span data-stu-id="020ee-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="020ee-107">例子</span><span class="sxs-lookup"><span data-stu-id="020ee-107">EXAMPLES</span></span>

### <span data-ttu-id="020ee-108">範例 1：取得特定的 DDoS 保護計劃</span><span class="sxs-lookup"><span data-stu-id="020ee-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="020ee-109">在這個案例中，我們需要同時指定 **ResourceGroupName** 和 **Name** 屬性，分別對應到資源群組和 DDoS 保護計劃的名稱。</span><span class="sxs-lookup"><span data-stu-id="020ee-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="020ee-110">範例 2：在資源群組中取得所有 DDoS 保護計劃</span><span class="sxs-lookup"><span data-stu-id="020ee-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="020ee-111">在此情境中，我們只會指定參數 **ResourceGroupName，** 以取得 DDoS 保護方案的清單。</span><span class="sxs-lookup"><span data-stu-id="020ee-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="020ee-112">範例 3：取得訂閱中所有的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="020ee-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="020ee-113">在此，我們不會指定任何參數，以取得訂閱中所有 DDoS 保護方案的清單。</span><span class="sxs-lookup"><span data-stu-id="020ee-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="020ee-114">範例 4：取得訂閱中所有的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="020ee-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="020ee-115">此 Cmdlet 會以「test」做為起始的所有 DdosProtectionPlans。</span><span class="sxs-lookup"><span data-stu-id="020ee-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="020ee-116">參數</span><span class="sxs-lookup"><span data-stu-id="020ee-116">PARAMETERS</span></span>

### <span data-ttu-id="020ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020ee-117">-DefaultProfile</span></span>
<span data-ttu-id="020ee-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="020ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020ee-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="020ee-119">-Name</span></span>
<span data-ttu-id="020ee-120">指定 DDoS 保護計劃的名稱。</span><span class="sxs-lookup"><span data-stu-id="020ee-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="020ee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020ee-121">-ResourceGroupName</span></span>
<span data-ttu-id="020ee-122">指定 DDoS 保護計劃資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="020ee-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="020ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020ee-123">CommonParameters</span></span>
<span data-ttu-id="020ee-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="020ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020ee-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="020ee-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020ee-126">輸入</span><span class="sxs-lookup"><span data-stu-id="020ee-126">INPUTS</span></span>

### <span data-ttu-id="020ee-127">System.String</span><span class="sxs-lookup"><span data-stu-id="020ee-127">System.String</span></span>

## <span data-ttu-id="020ee-128">輸出</span><span class="sxs-lookup"><span data-stu-id="020ee-128">OUTPUTS</span></span>

### <span data-ttu-id="020ee-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="020ee-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="020ee-130">筆記</span><span class="sxs-lookup"><span data-stu-id="020ee-130">NOTES</span></span>

## <span data-ttu-id="020ee-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="020ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="020ee-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="020ee-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="020ee-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="020ee-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="020ee-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="020ee-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="020ee-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="020ee-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="020ee-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="020ee-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)