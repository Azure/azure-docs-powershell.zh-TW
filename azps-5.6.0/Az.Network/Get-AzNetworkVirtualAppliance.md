---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 3ca8c522e3aa4d31e5718d09fffe0ff22fd4cab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916029"
---
# <span data-ttu-id="58cd0-101">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="58cd0-101">Get-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="58cd0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58cd0-102">SYNOPSIS</span></span>
<span data-ttu-id="58cd0-103">取得或列出網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="58cd0-103">Get or List Network Virtual Appliances.</span></span>

## <span data-ttu-id="58cd0-104">語法</span><span class="sxs-lookup"><span data-stu-id="58cd0-104">SYNTAX</span></span>

### <span data-ttu-id="58cd0-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="58cd0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzNetworkVirtualAppliance [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58cd0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58cd0-106">ResourceIdParameterSet</span></span>
```
Get-AzNetworkVirtualAppliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58cd0-107">描述</span><span class="sxs-lookup"><span data-stu-id="58cd0-107">DESCRIPTION</span></span>
<span data-ttu-id="58cd0-108">這些Get-AzNetworkVirtualAppliance會獲得或列出網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="58cd0-108">The Get-AzNetworkVirtualAppliance commands gets or lists Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="58cd0-109">例子</span><span class="sxs-lookup"><span data-stu-id="58cd0-109">EXAMPLES</span></span>

### <span data-ttu-id="58cd0-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="58cd0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva                                                                                                                      

BootStrapConfigurationBlobs : {}
VirtualHub                  : Microsoft.Azure.Commands.Network.Models.PSResourceId
CloudInitConfigurationBlobs : {}
CloudInitConfiguration      : echo hi
VirtualApplianceAsn         : 1270
VirtualApplianceNics        : {privatenicipconfig, publicnicipconfig, privatenicipconfig, publicnicipconfig}
VirtualApplianceSites       : {}
ProvisioningState           : Succeeded
Identity                    :
NvaSku                      : Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
ResourceGroupName           : testrg
Location                    : eastus2
ResourceGuid                :
Type                        : Microsoft.Network/NetworkVirtualAppliances
Tag                         :
TagsTable                   :
Name                        : nva
Etag                        : 00000000-0000-0000-0000-000000000000
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva
```

<span data-ttu-id="58cd0-111">取得網路虛擬裝置資源。</span><span class="sxs-lookup"><span data-stu-id="58cd0-111">Get a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="58cd0-112">參數</span><span class="sxs-lookup"><span data-stu-id="58cd0-112">PARAMETERS</span></span>

### <span data-ttu-id="58cd0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cd0-113">-DefaultProfile</span></span>
<span data-ttu-id="58cd0-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58cd0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58cd0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="58cd0-115">-Name</span></span>
<span data-ttu-id="58cd0-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="58cd0-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58cd0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cd0-117">-ResourceGroupName</span></span>
<span data-ttu-id="58cd0-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="58cd0-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58cd0-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58cd0-119">-ResourceId</span></span>
<span data-ttu-id="58cd0-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="58cd0-120">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58cd0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cd0-121">CommonParameters</span></span>
<span data-ttu-id="58cd0-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58cd0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cd0-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58cd0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cd0-124">輸入</span><span class="sxs-lookup"><span data-stu-id="58cd0-124">INPUTS</span></span>

### <span data-ttu-id="58cd0-125">System.String</span><span class="sxs-lookup"><span data-stu-id="58cd0-125">System.String</span></span>

## <span data-ttu-id="58cd0-126">輸出</span><span class="sxs-lookup"><span data-stu-id="58cd0-126">OUTPUTS</span></span>

### <span data-ttu-id="58cd0-127">Microsoft.Azure.Commands.Network.models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="58cd0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="58cd0-128">筆記</span><span class="sxs-lookup"><span data-stu-id="58cd0-128">NOTES</span></span>

## <span data-ttu-id="58cd0-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="58cd0-129">RELATED LINKS</span></span>
