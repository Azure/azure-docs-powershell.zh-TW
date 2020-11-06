---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 30a237f0f87286be8f6cd18e804d80850df7a8be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457512"
---
# <span data-ttu-id="1ccf0-101">New-AzureRmApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1ccf0-101">New-AzureRmApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1ccf0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ccf0-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccf0-103">建立 PsApiManagementVirtualNetwork 的實例。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ccf0-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ccf0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ccf0-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ccf0-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccf0-106">**新的-AzureRmApiManagementVirtualNetwork** Cmdlet 是協助程式命令，可建立 **PsApiManagementVirtualNetwork** 的實例。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-106">The **New-AzureRmApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="1ccf0-107">此命令與 **AzureRmApiManagementDeployment** Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-107">This command is used with **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="1ccf0-108">示例</span><span class="sxs-lookup"><span data-stu-id="1ccf0-108">EXAMPLES</span></span>

### <span data-ttu-id="1ccf0-109">範例1：建立虛擬網路</span><span class="sxs-lookup"><span data-stu-id="1ccf0-109">Example 1: Create a virtual network</span></span>
```
PS C:\>$vnetName = "myvnet"
PS C:\>$subnetName = "default"
PS C:\>$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.1.0/24
PS C:\>$vnet = New-AzureRmvirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $location -AddressPrefix 10.0.0.0/16 -Subnet $subnet

# Create a Virtual Network Object
PS C:\>$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location $location -SubnetResourceId $vnet.Subnets[0].Id

# Get the service
PS C:\>$service = Get-AzureRmApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName    
PS C:\>$service.VirtualNetwork = $virtualNetwork
PS C:\>$service.VpnType = "External"

# Update the Deployment with Virtual Network
PS C:\>Update-AzureRmApiManagementDeployment -ApiManagement $service
```

<span data-ttu-id="1ccf0-110">這個範例會建立一個虛擬網路，然後呼叫 **AzureRmApiManagementDeployment** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-110">This example creates a virtual network and then calls the **Update-AzureRmApiManagementDeployment** cmdlet.</span></span>

## <span data-ttu-id="1ccf0-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ccf0-111">PARAMETERS</span></span>

### <span data-ttu-id="1ccf0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccf0-112">-DefaultProfile</span></span>
<span data-ttu-id="1ccf0-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf0-114">-位置</span><span class="sxs-lookup"><span data-stu-id="1ccf0-114">-Location</span></span>
<span data-ttu-id="1ccf0-115">指定 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-115">Specifies the location amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1ccf0-116">若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="1ccf0-116">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf0-117">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="1ccf0-117">-SubnetResourceId</span></span>
<span data-ttu-id="1ccf0-118">指定虛擬網路的子網資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-118">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccf0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccf0-119">CommonParameters</span></span>
<span data-ttu-id="1ccf0-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccf0-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccf0-122">輸入</span><span class="sxs-lookup"><span data-stu-id="1ccf0-122">INPUTS</span></span>

### <span data-ttu-id="1ccf0-123">所有</span><span class="sxs-lookup"><span data-stu-id="1ccf0-123">None</span></span>
<span data-ttu-id="1ccf0-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1ccf0-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1ccf0-125">OUTPUTS</span></span>

### <span data-ttu-id="1ccf0-126">PsApiManagementVirtualNetwork 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="1ccf0-126">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1ccf0-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1ccf0-127">NOTES</span></span>

## <span data-ttu-id="1ccf0-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ccf0-128">RELATED LINKS</span></span>

[<span data-ttu-id="1ccf0-129">更新-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="1ccf0-129">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)

