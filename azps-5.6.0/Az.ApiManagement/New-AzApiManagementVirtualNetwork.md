---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: a714730a416d7554cba53e96428c9813fe4e720d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903713"
---
# <span data-ttu-id="30d30-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30d30-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="30d30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="30d30-102">SYNOPSIS</span></span>
<span data-ttu-id="30d30-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="30d30-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="30d30-104">語法</span><span class="sxs-lookup"><span data-stu-id="30d30-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30d30-105">描述</span><span class="sxs-lookup"><span data-stu-id="30d30-105">DESCRIPTION</span></span>
<span data-ttu-id="30d30-106">**New-AzApiManagementVirtualNetwork** Cmdlet 是建立 **PsApiManagementVirtualNetwork** 實例的協助者命令。</span><span class="sxs-lookup"><span data-stu-id="30d30-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="30d30-107">此命令與 **Set-AzApiManagement** 和 **New-AzApiManagement** Cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="30d30-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="30d30-108">例子</span><span class="sxs-lookup"><span data-stu-id="30d30-108">EXAMPLES</span></span>

### <span data-ttu-id="30d30-109">範例 1：建立虛擬網路，並更新現有的 APIM 服務至 VNET</span><span class="sxs-lookup"><span data-stu-id="30d30-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="30d30-110">此範例會建立一個虛擬網路，然後呼叫 **Set-AzApiManagement** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="30d30-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="30d30-111">範例 2：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="30d30-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="30d30-112">此範例會以模式將新的 APIM 服務建立為 `External` 虛擬網路</span><span class="sxs-lookup"><span data-stu-id="30d30-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="30d30-113">參數</span><span class="sxs-lookup"><span data-stu-id="30d30-113">PARAMETERS</span></span>

### <span data-ttu-id="30d30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30d30-114">-DefaultProfile</span></span>
<span data-ttu-id="30d30-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="30d30-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30d30-116">-子網ResourceId</span><span class="sxs-lookup"><span data-stu-id="30d30-116">-SubnetResourceId</span></span>
<span data-ttu-id="30d30-117">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="30d30-117">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30d30-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30d30-118">CommonParameters</span></span>
<span data-ttu-id="30d30-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="30d30-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30d30-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="30d30-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30d30-121">輸入</span><span class="sxs-lookup"><span data-stu-id="30d30-121">INPUTS</span></span>

### <span data-ttu-id="30d30-122">沒有</span><span class="sxs-lookup"><span data-stu-id="30d30-122">None</span></span>

## <span data-ttu-id="30d30-123">輸出</span><span class="sxs-lookup"><span data-stu-id="30d30-123">OUTPUTS</span></span>

### <span data-ttu-id="30d30-124">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30d30-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="30d30-125">筆記</span><span class="sxs-lookup"><span data-stu-id="30d30-125">NOTES</span></span>

## <span data-ttu-id="30d30-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="30d30-126">RELATED LINKS</span></span>

<span data-ttu-id="30d30-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
[New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="30d30-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

