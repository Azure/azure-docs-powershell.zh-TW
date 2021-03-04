---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 0feaa59a6af5610a7dbdef555c8baebdba9abe54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916049"
---
# <span data-ttu-id="a39ad-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a39ad-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="a39ad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a39ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ad-103">根據名稱或 NatGateway Id 或資源群組中所有 Nat 閘道資源，在資源群組中獲得 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="a39ad-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="a39ad-104">語法</span><span class="sxs-lookup"><span data-stu-id="a39ad-104">SYNTAX</span></span>

### <span data-ttu-id="a39ad-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a39ad-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a39ad-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39ad-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a39ad-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a39ad-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a39ad-108">描述</span><span class="sxs-lookup"><span data-stu-id="a39ad-108">DESCRIPTION</span></span>
<span data-ttu-id="a39ad-109">根據名稱或 NatGateway Id 或資源群組中所有 Nat 閘道資源，在資源群組中獲得 Nat 閘道資源。</span><span class="sxs-lookup"><span data-stu-id="a39ad-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="a39ad-110">例子</span><span class="sxs-lookup"><span data-stu-id="a39ad-110">EXAMPLES</span></span>

### <span data-ttu-id="a39ad-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a39ad-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="a39ad-112">參數</span><span class="sxs-lookup"><span data-stu-id="a39ad-112">PARAMETERS</span></span>

### <span data-ttu-id="a39ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ad-113">-DefaultProfile</span></span>
<span data-ttu-id="a39ad-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a39ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39ad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a39ad-115">-Name</span></span>
<span data-ttu-id="a39ad-116">nat 閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="a39ad-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="a39ad-118">nat 閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a39ad-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a39ad-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a39ad-119">-ResourceId</span></span>
<span data-ttu-id="a39ad-120">Nat 閘道識別碼</span><span class="sxs-lookup"><span data-stu-id="a39ad-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ad-121">CommonParameters</span></span>
<span data-ttu-id="a39ad-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a39ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ad-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a39ad-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ad-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a39ad-124">INPUTS</span></span>

### <span data-ttu-id="a39ad-125">System.String</span><span class="sxs-lookup"><span data-stu-id="a39ad-125">System.String</span></span>

## <span data-ttu-id="a39ad-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a39ad-126">OUTPUTS</span></span>

### <span data-ttu-id="a39ad-127">Microsoft.Azure.Commands.Network.models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="a39ad-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="a39ad-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a39ad-128">NOTES</span></span>

## <span data-ttu-id="a39ad-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a39ad-129">RELATED LINKS</span></span>
