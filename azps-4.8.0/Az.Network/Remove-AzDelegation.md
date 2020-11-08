---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970324"
---
# <span data-ttu-id="7dc3d-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="7dc3d-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="7dc3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dc3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc3d-103">從提供的子網上移除服務委派。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="7dc3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dc3d-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dc3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="7dc3d-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc3d-106">**AzDelegation** Cmdlet 會在子網中使用委派，並從該子網上移除已命名的委派。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="7dc3d-107">示例</span><span class="sxs-lookup"><span data-stu-id="7dc3d-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc3d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7dc3d-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="7dc3d-109">在這個範例中，在 _[新增委派至現有的子網]_ 下的第一個半形 () 與 [AzDelegation](./Add-AzDelegation.md)相同。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="7dc3d-110">在第二部分中，前兩個 Cmdlet 會檢索感興趣的子網上，並重新整理本機複本與伺服器上的內容。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="7dc3d-111">第三個 Cmdlet 會從 _mySubnet_ 中移除在前半部建立的委派，並將更新的子網儲存在 _$subnet_ 中。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="7dc3d-112">最後一個 Cmdlet 會使用已移除的委派來補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="7dc3d-113">參數</span><span class="sxs-lookup"><span data-stu-id="7dc3d-113">PARAMETERS</span></span>

### <span data-ttu-id="7dc3d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc3d-114">-DefaultProfile</span></span>
<span data-ttu-id="7dc3d-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dc3d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dc3d-116">-Name</span></span>
<span data-ttu-id="7dc3d-117">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="7dc3d-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc3d-118">-子網</span><span class="sxs-lookup"><span data-stu-id="7dc3d-118">-Subnet</span></span>
<span data-ttu-id="7dc3d-119">要從中移除委派的子網</span><span class="sxs-lookup"><span data-stu-id="7dc3d-119">The subnet from which to remove the delegation</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc3d-120">CommonParameters</span></span>
<span data-ttu-id="7dc3d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc3d-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dc3d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc3d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="7dc3d-123">INPUTS</span></span>

### <span data-ttu-id="7dc3d-124">System.object</span><span class="sxs-lookup"><span data-stu-id="7dc3d-124">System.String</span></span>

### <span data-ttu-id="7dc3d-125">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7dc3d-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7dc3d-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7dc3d-126">OUTPUTS</span></span>

### <span data-ttu-id="7dc3d-127">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="7dc3d-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="7dc3d-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7dc3d-128">NOTES</span></span>

## <span data-ttu-id="7dc3d-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dc3d-129">RELATED LINKS</span></span>

<span data-ttu-id="7dc3d-130">[附加 AzDelegation](./Add-AzDelegation.md) 
[AzDelegation](./Get-AzDelegation.md) 
[新-AzDelegation](./New-AzDelegation.md) 
[AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="7dc3d-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>