---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: 729f89742c7dd3249124f2d2404ab85f08db0e86
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789645"
---
# <span data-ttu-id="f3352-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f3352-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="f3352-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3352-102">SYNOPSIS</span></span>
<span data-ttu-id="f3352-103">取得 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="f3352-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="f3352-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3352-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3352-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3352-105">DESCRIPTION</span></span>
<span data-ttu-id="f3352-106">Get-AzDdosProtectionPlan Cmdlet 會取得 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="f3352-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="f3352-107">示例</span><span class="sxs-lookup"><span data-stu-id="f3352-107">EXAMPLES</span></span>

### <span data-ttu-id="f3352-108">範例1：取得特定的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="f3352-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="f3352-109">在這種情況下，我們需要指定 **ResourceGroupName** 和 **Name** 屬性，分別對應到 [資源] 群組和 DDoS 保護方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3352-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="f3352-110">範例2：取得資源群組中的所有 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="f3352-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="f3352-111">在這種情況下，我們只會指定參數 **ResourceGroupName** 來取得 DDoS 保護方案清單。</span><span class="sxs-lookup"><span data-stu-id="f3352-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="f3352-112">範例3：取得訂閱中的所有 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="f3352-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="f3352-113">在這裡，我們不會指定任何參數以取得訂閱中的所有 DDoS 保護方案清單。</span><span class="sxs-lookup"><span data-stu-id="f3352-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="f3352-114">範例4：取得訂閱中的所有 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="f3352-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="f3352-115">這個 Cmdlet 會傳回以「test」開頭的所有 DdosProtectionPlans。</span><span class="sxs-lookup"><span data-stu-id="f3352-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="f3352-116">參數</span><span class="sxs-lookup"><span data-stu-id="f3352-116">PARAMETERS</span></span>

### <span data-ttu-id="f3352-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3352-117">-DefaultProfile</span></span>
<span data-ttu-id="f3352-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3352-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3352-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f3352-119">-Name</span></span>
<span data-ttu-id="f3352-120">指定 DDoS 保護方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3352-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="f3352-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3352-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3352-122">指定 DDoS 保護方案資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3352-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="f3352-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3352-123">CommonParameters</span></span>
<span data-ttu-id="f3352-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3352-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3352-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f3352-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3352-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f3352-126">INPUTS</span></span>

### <span data-ttu-id="f3352-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f3352-127">System.String</span></span>

## <span data-ttu-id="f3352-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f3352-128">OUTPUTS</span></span>

### <span data-ttu-id="f3352-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f3352-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="f3352-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f3352-130">NOTES</span></span>

## <span data-ttu-id="f3352-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3352-131">RELATED LINKS</span></span>

[<span data-ttu-id="f3352-132">新-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f3352-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="f3352-133">移除-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="f3352-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="f3352-134">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3352-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f3352-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3352-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="f3352-136">AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f3352-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)