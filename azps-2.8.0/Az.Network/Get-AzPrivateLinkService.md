---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkService.md
ms.openlocfilehash: 9f40d9ce99db8640fcf98d48f8dc3920a8517b3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790065"
---
# <span data-ttu-id="49b3d-101">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="49b3d-101">Get-AzPrivateLinkService</span></span>

## <span data-ttu-id="49b3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="49b3d-103">取得私人連結服務</span><span class="sxs-lookup"><span data-stu-id="49b3d-103">Gets private link service</span></span>

## <span data-ttu-id="49b3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="49b3d-104">SYNTAX</span></span>

### <span data-ttu-id="49b3d-105">NoExpand (預設) </span><span class="sxs-lookup"><span data-stu-id="49b3d-105">NoExpand (Default)</span></span>
```
Get-AzPrivateLinkService [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49b3d-106">擴充</span><span class="sxs-lookup"><span data-stu-id="49b3d-106">Expand</span></span>
```
Get-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b3d-107">說明</span><span class="sxs-lookup"><span data-stu-id="49b3d-107">DESCRIPTION</span></span>
<span data-ttu-id="49b3d-108">**AzPrivateLinkService** Cmdlet 會取得一或多個私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="49b3d-108">The **Get-AzPrivateLinkService** cmdlet gets one or more private link services.</span></span>

## <span data-ttu-id="49b3d-109">示例</span><span class="sxs-lookup"><span data-stu-id="49b3d-109">EXAMPLES</span></span>

### <span data-ttu-id="49b3d-110">範例</span><span class="sxs-lookup"><span data-stu-id="49b3d-110">Example</span></span>
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

<span data-ttu-id="49b3d-111">這個 commandlet 會取得 [資源] 群組中的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="49b3d-111">This commandlet gets a private link service in the resource group.</span></span>

## <span data-ttu-id="49b3d-112">參數</span><span class="sxs-lookup"><span data-stu-id="49b3d-112">PARAMETERS</span></span>

### <span data-ttu-id="49b3d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b3d-113">-DefaultProfile</span></span>
<span data-ttu-id="49b3d-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49b3d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49b3d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="49b3d-115">-ExpandResource</span></span>
<span data-ttu-id="49b3d-116">要展開的資源參照。</span><span class="sxs-lookup"><span data-stu-id="49b3d-116">The resource reference to be expanded.</span></span>

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

### <span data-ttu-id="49b3d-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="49b3d-117">-Name</span></span>
<span data-ttu-id="49b3d-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="49b3d-118">The resource name.</span></span>

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

### <span data-ttu-id="49b3d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49b3d-119">-ResourceGroupName</span></span>
<span data-ttu-id="49b3d-120">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49b3d-120">The resource group name.</span></span>

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

### <span data-ttu-id="49b3d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b3d-121">CommonParameters</span></span>
<span data-ttu-id="49b3d-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49b3d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b3d-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="49b3d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b3d-124">輸入</span><span class="sxs-lookup"><span data-stu-id="49b3d-124">INPUTS</span></span>

### <span data-ttu-id="49b3d-125">System.object</span><span class="sxs-lookup"><span data-stu-id="49b3d-125">System.String</span></span>

## <span data-ttu-id="49b3d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="49b3d-126">OUTPUTS</span></span>

### <span data-ttu-id="49b3d-127">PSPrivateLinkService 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="49b3d-127">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="49b3d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="49b3d-128">NOTES</span></span>

## <span data-ttu-id="49b3d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="49b3d-129">RELATED LINKS</span></span>
