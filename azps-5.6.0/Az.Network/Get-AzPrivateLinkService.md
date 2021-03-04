---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 8b2e8902257566256ed41c38c90c31cb430d12d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902462"
---
# <span data-ttu-id="152b8-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="152b8-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="152b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="152b8-102">SYNOPSIS</span></span>
<span data-ttu-id="152b8-103">獲得私人連結服務</span><span class="sxs-lookup"><span data-stu-id="152b8-103">Gets private link service</span></span>

## <span data-ttu-id="152b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="152b8-104">SYNTAX</span></span>

### <span data-ttu-id="152b8-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="152b8-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="152b8-106">擴大</span><span class="sxs-lookup"><span data-stu-id="152b8-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="152b8-107">描述</span><span class="sxs-lookup"><span data-stu-id="152b8-107">DESCRIPTION</span></span>
<span data-ttu-id="152b8-108">**Get-AzPrivateLinkService** Cmdlet 會取得一或多個私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="152b8-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="152b8-109">例子</span><span class="sxs-lookup"><span data-stu-id="152b8-109">EXAMPLES</span></span>

### <span data-ttu-id="152b8-110">例子</span><span class="sxs-lookup"><span data-stu-id="152b8-110">Example</span></span>
```
Get-AzPrivateLinkService -Name MyPLS -ResourceGroupName TestResourceGroup

Name                                 : MyPLS
ResourceGroupName                    : TestResourceGroup
Id                                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/prov
                                       iders/Microsoft.Network/privateLinkServices/MyPLS
Location                             : eastus2euap
Type                                 : Microsoft.Network/privateLinkServices
Etag                                 : W/"00000000-0000-0000-0000-000000000000"
Tag                                  : {}
ProvisioningState                    : Succeeded
Visibility                           : 
AutoApproval                         : 
Alias                                :
LoadBalancerFrontendIpConfigurations : []
IpConfigurations                     : [
                                         {
                                           "PrivateIPAddress": "10.0.2.5",
                                           "PrivateIPAllocationMethod": "Static",
                                           "ProvisioningState": "Failed",
                                           "PrivateIPAddressVersion": "IPv4",
                                           "Name": "IP-Config",
                                           "Subnet": {
                                             "Delegations": [],
                                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/
                                       TestResourceGroup/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/backendSubne
                                       t",
                                             "ServiceAssociationLinks": []
                                           }
                                         }
                                       ]
PrivateEndpointConnections           : []
NetworkInterfaces                    : [
                                         {
                                           "TapConfigurations": [],
                                           "HostedWorkloads": [],
                                           "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/networkInterfaces/mytestinterface"
                                         }
                                       ]
```

<span data-ttu-id="152b8-111">這個命令小命令會獲得資源群組中的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="152b8-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="152b8-112">參數</span><span class="sxs-lookup"><span data-stu-id="152b8-112">PARAMETERS</span></span>

### <span data-ttu-id="152b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="152b8-113">-DefaultProfile</span></span>
<span data-ttu-id="152b8-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="152b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="152b8-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="152b8-115">-ExpandResource</span></span>
<span data-ttu-id="152b8-116">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="152b8-116">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152b8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="152b8-117">-Name</span></span>
<span data-ttu-id="152b8-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="152b8-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="152b8-120">資源組名。</span><span class="sxs-lookup"><span data-stu-id="152b8-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="152b8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152b8-121">CommonParameters</span></span>
<span data-ttu-id="152b8-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="152b8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152b8-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="152b8-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152b8-124">輸入</span><span class="sxs-lookup"><span data-stu-id="152b8-124">INPUTS</span></span>

### <span data-ttu-id="152b8-125">System.String</span><span class="sxs-lookup"><span data-stu-id="152b8-125">System.String</span></span>

## <span data-ttu-id="152b8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="152b8-126">OUTPUTS</span></span>

### <span data-ttu-id="152b8-127">Microsoft.Azure.Commands.Network.models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="152b8-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="152b8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="152b8-128">NOTES</span></span>

## <span data-ttu-id="152b8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="152b8-129">RELATED LINKS</span></span>
