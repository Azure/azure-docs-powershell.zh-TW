---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452776"
---
# <span data-ttu-id="65e99-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="65e99-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="65e99-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65e99-102">SYNOPSIS</span></span>
<span data-ttu-id="65e99-103">在指定的子網上取得委派 (或所有委派) 。</span><span class="sxs-lookup"><span data-stu-id="65e99-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e99-104">句法</span><span class="sxs-lookup"><span data-stu-id="65e99-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65e99-105">說明</span><span class="sxs-lookup"><span data-stu-id="65e99-105">DESCRIPTION</span></span>
<span data-ttu-id="65e99-106">**AzureRmDelegation** Cmdlet 會從子網上取得命名委派。</span><span class="sxs-lookup"><span data-stu-id="65e99-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="65e99-107">如果沒有命名委派，它會在所提供的子網上傳回所有委派。</span><span class="sxs-lookup"><span data-stu-id="65e99-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="65e99-108">示例</span><span class="sxs-lookup"><span data-stu-id="65e99-108">EXAMPLES</span></span>

### <span data-ttu-id="65e99-109">1：檢索特定委派</span><span class="sxs-lookup"><span data-stu-id="65e99-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="65e99-110">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="65e99-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="65e99-111">第二行顯示名為「myDelegation」的委派的委派資訊。</span><span class="sxs-lookup"><span data-stu-id="65e99-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="65e99-112">2：檢索所有子網委派</span><span class="sxs-lookup"><span data-stu-id="65e99-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="65e99-113">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="65e99-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="65e99-114">第二行儲存 $delegations 變數中 _mySubnet_ 的所有委派清單。</span><span class="sxs-lookup"><span data-stu-id="65e99-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="65e99-115">參數</span><span class="sxs-lookup"><span data-stu-id="65e99-115">PARAMETERS</span></span>

### <span data-ttu-id="65e99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e99-116">-DefaultProfile</span></span>
<span data-ttu-id="65e99-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="65e99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65e99-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="65e99-118">-Name</span></span>
<span data-ttu-id="65e99-119">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="65e99-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65e99-120">-子網</span><span class="sxs-lookup"><span data-stu-id="65e99-120">-Subnet</span></span>
<span data-ttu-id="65e99-121">子網上</span><span class="sxs-lookup"><span data-stu-id="65e99-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65e99-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e99-122">CommonParameters</span></span>
<span data-ttu-id="65e99-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65e99-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="65e99-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65e99-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e99-125">輸入</span><span class="sxs-lookup"><span data-stu-id="65e99-125">INPUTS</span></span>

### <span data-ttu-id="65e99-126">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="65e99-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="65e99-127">輸出</span><span class="sxs-lookup"><span data-stu-id="65e99-127">OUTPUTS</span></span>

### <span data-ttu-id="65e99-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="65e99-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="65e99-129">筆記</span><span class="sxs-lookup"><span data-stu-id="65e99-129">NOTES</span></span>

## <span data-ttu-id="65e99-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="65e99-130">RELATED LINKS</span></span>
<span data-ttu-id="65e99-131">[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[新-AzureRmDelegation](./New-AzureRmDelegation.md) 
[移除-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="65e99-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
