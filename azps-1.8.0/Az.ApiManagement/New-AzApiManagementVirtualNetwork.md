---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: 496e65438a2c0ef5f09bbf961535eaa842062f25
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400887"
---
# <span data-ttu-id="23355-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23355-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="23355-102">簡介</span><span class="sxs-lookup"><span data-stu-id="23355-102">SYNOPSIS</span></span>
<span data-ttu-id="23355-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="23355-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="23355-104">語法</span><span class="sxs-lookup"><span data-stu-id="23355-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23355-105">描述</span><span class="sxs-lookup"><span data-stu-id="23355-105">DESCRIPTION</span></span>
<span data-ttu-id="23355-106">**New-AzApiManagementVirtualNetwork** Cmdlet 是建立 **PsApiManagementVirtualNetwork** 實例的協助者命令。</span><span class="sxs-lookup"><span data-stu-id="23355-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="23355-107">此命令與 **Set-AzApiManagement** Cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="23355-107">This command is used with **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="23355-108">例子</span><span class="sxs-lookup"><span data-stu-id="23355-108">EXAMPLES</span></span>

### <span data-ttu-id="23355-109">範例 1：建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="23355-109">Example 1: Create a virtual network</span></span>
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
PS C:\>Set-AzApiManagement -ApiManagement $service
```

<span data-ttu-id="23355-110">此範例會建立一個虛擬網路，然後呼叫 **Set-AzApiManagement** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23355-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="23355-111">參數</span><span class="sxs-lookup"><span data-stu-id="23355-111">PARAMETERS</span></span>

### <span data-ttu-id="23355-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23355-112">-DefaultProfile</span></span>
<span data-ttu-id="23355-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="23355-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23355-114">-子網ResourceId</span><span class="sxs-lookup"><span data-stu-id="23355-114">-SubnetResourceId</span></span>
<span data-ttu-id="23355-115">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="23355-115">Specifies the subnet resource ID of the virtual network.</span></span>

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

### <span data-ttu-id="23355-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23355-116">CommonParameters</span></span>
<span data-ttu-id="23355-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="23355-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23355-118">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="23355-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23355-119">輸入</span><span class="sxs-lookup"><span data-stu-id="23355-119">INPUTS</span></span>

### <span data-ttu-id="23355-120">沒有</span><span class="sxs-lookup"><span data-stu-id="23355-120">None</span></span>

## <span data-ttu-id="23355-121">輸出</span><span class="sxs-lookup"><span data-stu-id="23355-121">OUTPUTS</span></span>

### <span data-ttu-id="23355-122">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23355-122">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="23355-123">筆記</span><span class="sxs-lookup"><span data-stu-id="23355-123">NOTES</span></span>

## <span data-ttu-id="23355-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="23355-124">RELATED LINKS</span></span>

[<span data-ttu-id="23355-125">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="23355-125">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

