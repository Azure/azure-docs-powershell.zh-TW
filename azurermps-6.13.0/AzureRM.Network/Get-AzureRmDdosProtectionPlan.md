---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624889"
---
# <span data-ttu-id="e4392-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e4392-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="e4392-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4392-102">SYNOPSIS</span></span>
<span data-ttu-id="e4392-103">取得 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="e4392-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4392-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4392-104">SYNTAX</span></span>

### <span data-ttu-id="e4392-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="e4392-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4392-106">清單</span><span class="sxs-lookup"><span data-stu-id="e4392-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4392-107">說明</span><span class="sxs-lookup"><span data-stu-id="e4392-107">DESCRIPTION</span></span>
<span data-ttu-id="e4392-108">Get-AzureRmDdosProtectionPlan Cmdlet 會取得 DDoS 保護方案。</span><span class="sxs-lookup"><span data-stu-id="e4392-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="e4392-109">示例</span><span class="sxs-lookup"><span data-stu-id="e4392-109">EXAMPLES</span></span>

### <span data-ttu-id="e4392-110">範例1：取得特定的 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="e4392-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="e4392-111">在這種情況下，我們需要指定 **ResourceGroupName** 和 **Name** 屬性，分別對應到 [資源] 群組和 DDoS 保護方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4392-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="e4392-112">範例2：取得資源群組中的所有 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="e4392-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="e4392-113">在這種情況下，我們只會指定參數 **ResourceGroupName** 來取得 DDoS 保護方案清單。</span><span class="sxs-lookup"><span data-stu-id="e4392-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="e4392-114">範例2：取得訂閱中的所有 DDoS 保護方案</span><span class="sxs-lookup"><span data-stu-id="e4392-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="e4392-115">在這裡，我們不會指定任何參數以取得訂閱中的所有 DDoS 保護方案清單。</span><span class="sxs-lookup"><span data-stu-id="e4392-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="e4392-116">參數</span><span class="sxs-lookup"><span data-stu-id="e4392-116">PARAMETERS</span></span>

### <span data-ttu-id="e4392-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4392-117">-DefaultProfile</span></span>
<span data-ttu-id="e4392-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e4392-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4392-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4392-119">-Name</span></span>
<span data-ttu-id="e4392-120">指定 DDoS 保護方案的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4392-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4392-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4392-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4392-122">指定 DDoS 保護方案資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4392-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4392-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4392-123">CommonParameters</span></span>
<span data-ttu-id="e4392-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4392-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4392-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4392-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4392-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e4392-126">INPUTS</span></span>

### <span data-ttu-id="e4392-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e4392-127">System.String</span></span>

## <span data-ttu-id="e4392-128">輸出</span><span class="sxs-lookup"><span data-stu-id="e4392-128">OUTPUTS</span></span>

### <span data-ttu-id="e4392-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e4392-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="e4392-130">筆記</span><span class="sxs-lookup"><span data-stu-id="e4392-130">NOTES</span></span>

## <span data-ttu-id="e4392-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4392-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4392-132">新-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e4392-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="e4392-133">移除-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="e4392-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="e4392-134">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4392-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e4392-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4392-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e4392-136">AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4392-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
