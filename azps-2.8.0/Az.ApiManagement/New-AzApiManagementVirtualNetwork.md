---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 8833d6380c14c3b2e9b9c53657602f9f3cbfd1af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613956"
---
# <span data-ttu-id="23c74-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23c74-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="23c74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23c74-102">SYNOPSIS</span></span>
<span data-ttu-id="23c74-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="23c74-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="23c74-104">句法</span><span class="sxs-lookup"><span data-stu-id="23c74-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23c74-105">說明</span><span class="sxs-lookup"><span data-stu-id="23c74-105">DESCRIPTION</span></span>
<span data-ttu-id="23c74-106">**新的-AzApiManagementVirtualNetwork** Cmdlet 是協助程式命令，可建立 **PsApiManagementVirtualNetwork** 的實例。</span><span class="sxs-lookup"><span data-stu-id="23c74-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="23c74-107">此命令與 **AzApiManagement** 和 **AzApiManagement** Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="23c74-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="23c74-108">示例</span><span class="sxs-lookup"><span data-stu-id="23c74-108">EXAMPLES</span></span>

### <span data-ttu-id="23c74-109">範例1：建立虛擬網路，並將現有的 APIM 服務更新到 VNET</span><span class="sxs-lookup"><span data-stu-id="23c74-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="23c74-110">這個範例會建立一個虛擬網路，然後呼叫 **AzApiManagement** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23c74-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="23c74-111">範例2：為外部虛擬網路建立 API 管理服務</span><span class="sxs-lookup"><span data-stu-id="23c74-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="23c74-112">這個範例會在模式中建立新的 APIM 服務至虛擬網路 `External`</span><span class="sxs-lookup"><span data-stu-id="23c74-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="23c74-113">參數</span><span class="sxs-lookup"><span data-stu-id="23c74-113">PARAMETERS</span></span>

### <span data-ttu-id="23c74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c74-114">-DefaultProfile</span></span>
<span data-ttu-id="23c74-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23c74-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23c74-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="23c74-116">-SubnetResourceId</span></span>
<span data-ttu-id="23c74-117">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="23c74-117">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="23c74-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c74-118">CommonParameters</span></span>
<span data-ttu-id="23c74-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23c74-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c74-120">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23c74-120">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c74-121">輸入</span><span class="sxs-lookup"><span data-stu-id="23c74-121">INPUTS</span></span>

### <span data-ttu-id="23c74-122">所有</span><span class="sxs-lookup"><span data-stu-id="23c74-122">None</span></span>

## <span data-ttu-id="23c74-123">輸出</span><span class="sxs-lookup"><span data-stu-id="23c74-123">OUTPUTS</span></span>

### <span data-ttu-id="23c74-124">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="23c74-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="23c74-125">筆記</span><span class="sxs-lookup"><span data-stu-id="23c74-125">NOTES</span></span>

## <span data-ttu-id="23c74-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="23c74-126">RELATED LINKS</span></span>

<span data-ttu-id="23c74-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
[新-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="23c74-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

