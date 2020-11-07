---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 67020f99129dfa920aa1bbc5e22ac59c16affb32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788890"
---
# <span data-ttu-id="c804a-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c804a-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c804a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c804a-102">SYNOPSIS</span></span>
<span data-ttu-id="c804a-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="c804a-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="c804a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c804a-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c804a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c804a-105">DESCRIPTION</span></span>
<span data-ttu-id="c804a-106">**新的-AzApiManagementVirtualNetwork** Cmdlet 是協助程式命令，可建立 **PsApiManagementVirtualNetwork** 的實例。</span><span class="sxs-lookup"><span data-stu-id="c804a-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="c804a-107">此命令與 **AzApiManagementDeployment** Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c804a-107">This command is used with **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="c804a-108">示例</span><span class="sxs-lookup"><span data-stu-id="c804a-108">EXAMPLES</span></span>

### <span data-ttu-id="c804a-109">範例1：建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c804a-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="c804a-110">這個範例會建立一個虛擬網路，然後呼叫 **AzApiManagementDeployment** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c804a-110">This example creates a virtual network and then calls the **Update-AzApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="c804a-111">參數</span><span class="sxs-lookup"><span data-stu-id="c804a-111">PARAMETERS</span></span>

### <span data-ttu-id="c804a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c804a-112">-DefaultProfile</span></span>
<span data-ttu-id="c804a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c804a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c804a-114">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="c804a-114">-SubnetResourceId</span></span>
<span data-ttu-id="c804a-115">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c804a-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="c804a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c804a-116">CommonParameters</span></span>
<span data-ttu-id="c804a-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c804a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c804a-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c804a-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c804a-119">輸入</span><span class="sxs-lookup"><span data-stu-id="c804a-119">INPUTS</span></span>

### <span data-ttu-id="c804a-120">所有</span><span class="sxs-lookup"><span data-stu-id="c804a-120">None</span></span>

## <span data-ttu-id="c804a-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c804a-121">OUTPUTS</span></span>

### <span data-ttu-id="c804a-122">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="c804a-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c804a-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c804a-123">NOTES</span></span>

## <span data-ttu-id="c804a-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c804a-124">RELATED LINKS</span></span>

[<span data-ttu-id="c804a-125">更新-AzApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c804a-125">Update-AzApiManagementDeployment</span></span>](./Update-AzApiManagementDeployment.md)

