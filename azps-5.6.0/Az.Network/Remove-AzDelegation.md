---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 65149a0a52bc1bbb696b78033ec38670db97da48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912709"
---
# <span data-ttu-id="69bda-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="69bda-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="69bda-102">簡介</span><span class="sxs-lookup"><span data-stu-id="69bda-102">SYNOPSIS</span></span>
<span data-ttu-id="69bda-103">從提供的子網移除服務委派。</span><span class="sxs-lookup"><span data-stu-id="69bda-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="69bda-104">語法</span><span class="sxs-lookup"><span data-stu-id="69bda-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69bda-105">描述</span><span class="sxs-lookup"><span data-stu-id="69bda-105">DESCRIPTION</span></span>
<span data-ttu-id="69bda-106">**Remove-AzDelegation** Cmdlet 會採用子網與子網，並從該子網移除已命名的委派。</span><span class="sxs-lookup"><span data-stu-id="69bda-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="69bda-107">例子</span><span class="sxs-lookup"><span data-stu-id="69bda-107">EXAMPLES</span></span>

### <span data-ttu-id="69bda-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="69bda-108">Example 1</span></span>
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

<span data-ttu-id="69bda-109">在此範例中，在「新增 (委派至現有子網 _」_ 下找到的上半) [與 Add-AzDelegation 相同](./Add-AzDelegation.md)。</span><span class="sxs-lookup"><span data-stu-id="69bda-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="69bda-110">在後半部，前兩個 Cmdlet 會取回感興趣的子網，以伺服器內容重新組織本機複本。</span><span class="sxs-lookup"><span data-stu-id="69bda-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="69bda-111">第三個 Cmdlet 會移除上半部從 _mySubnet_ 建立委派，並儲存更新後的子網 _$subnet。_</span><span class="sxs-lookup"><span data-stu-id="69bda-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="69bda-112">最終的 Cmdlet 會以移除的委派補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="69bda-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="69bda-113">參數</span><span class="sxs-lookup"><span data-stu-id="69bda-113">PARAMETERS</span></span>

### <span data-ttu-id="69bda-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bda-114">-DefaultProfile</span></span>
<span data-ttu-id="69bda-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="69bda-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bda-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="69bda-116">-Name</span></span>
<span data-ttu-id="69bda-117">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="69bda-117">The name of the delegation</span></span>

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

### <span data-ttu-id="69bda-118">-子網</span><span class="sxs-lookup"><span data-stu-id="69bda-118">-Subnet</span></span>
<span data-ttu-id="69bda-119">移除委派的子網</span><span class="sxs-lookup"><span data-stu-id="69bda-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="69bda-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bda-120">CommonParameters</span></span>
<span data-ttu-id="69bda-121">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="69bda-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bda-122">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="69bda-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bda-123">輸入</span><span class="sxs-lookup"><span data-stu-id="69bda-123">INPUTS</span></span>

### <span data-ttu-id="69bda-124">System.String</span><span class="sxs-lookup"><span data-stu-id="69bda-124">System.String</span></span>

### <span data-ttu-id="69bda-125">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="69bda-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="69bda-126">輸出</span><span class="sxs-lookup"><span data-stu-id="69bda-126">OUTPUTS</span></span>

### <span data-ttu-id="69bda-127">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="69bda-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="69bda-128">筆記</span><span class="sxs-lookup"><span data-stu-id="69bda-128">NOTES</span></span>

## <span data-ttu-id="69bda-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="69bda-129">RELATED LINKS</span></span>

<span data-ttu-id="69bda-130">[Add-AzDelegation](./Add-AzDelegation.md) 
[Get-AzDelegation](./Get-AzDelegation.md) 
[New-AzDelegation](./New-AzDelegation.md) 
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="69bda-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>