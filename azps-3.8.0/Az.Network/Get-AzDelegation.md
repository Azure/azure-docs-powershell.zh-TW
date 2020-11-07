---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 213c6616a143f7be64454f6538fac5d5c89afd54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966314"
---
# <span data-ttu-id="fd664-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="fd664-101">Get-AzDelegation</span></span>

## <span data-ttu-id="fd664-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd664-102">SYNOPSIS</span></span>
<span data-ttu-id="fd664-103">在指定的子網上取得委派 (或所有委派) 。</span><span class="sxs-lookup"><span data-stu-id="fd664-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="fd664-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd664-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fd664-105">說明</span><span class="sxs-lookup"><span data-stu-id="fd664-105">DESCRIPTION</span></span>
<span data-ttu-id="fd664-106">**AzDelegation** Cmdlet 會從子網上取得命名委派。</span><span class="sxs-lookup"><span data-stu-id="fd664-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="fd664-107">如果沒有命名委派，它會在所提供的子網上傳回所有委派。</span><span class="sxs-lookup"><span data-stu-id="fd664-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="fd664-108">示例</span><span class="sxs-lookup"><span data-stu-id="fd664-108">EXAMPLES</span></span>

### <span data-ttu-id="fd664-109">1：檢索特定委派</span><span class="sxs-lookup"><span data-stu-id="fd664-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="fd664-110">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="fd664-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="fd664-111">第二行顯示名為「myDelegation」的委派的委派資訊。</span><span class="sxs-lookup"><span data-stu-id="fd664-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="fd664-112">2：檢索所有子網委派</span><span class="sxs-lookup"><span data-stu-id="fd664-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="fd664-113">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="fd664-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="fd664-114">第二行儲存 $delegations 變數中 _mySubnet_ 的所有委派清單。</span><span class="sxs-lookup"><span data-stu-id="fd664-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="fd664-115">參數</span><span class="sxs-lookup"><span data-stu-id="fd664-115">PARAMETERS</span></span>

### <span data-ttu-id="fd664-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd664-116">-DefaultProfile</span></span>
<span data-ttu-id="fd664-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd664-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd664-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd664-118">-Name</span></span>
<span data-ttu-id="fd664-119">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="fd664-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd664-120">-子網</span><span class="sxs-lookup"><span data-stu-id="fd664-120">-Subnet</span></span>
<span data-ttu-id="fd664-121">子網上</span><span class="sxs-lookup"><span data-stu-id="fd664-121">The subnet</span></span>

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

### <span data-ttu-id="fd664-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd664-122">CommonParameters</span></span>
<span data-ttu-id="fd664-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd664-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd664-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fd664-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd664-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fd664-125">INPUTS</span></span>

### <span data-ttu-id="fd664-126">System.object</span><span class="sxs-lookup"><span data-stu-id="fd664-126">System.String</span></span>

### <span data-ttu-id="fd664-127">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fd664-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="fd664-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fd664-128">OUTPUTS</span></span>

### <span data-ttu-id="fd664-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="fd664-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="fd664-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fd664-130">NOTES</span></span>

## <span data-ttu-id="fd664-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd664-131">RELATED LINKS</span></span>

<span data-ttu-id="fd664-132">[附加 AzDelegation](./Add-AzDelegation.md) 
[新-AzDelegation](./New-AzDelegation.md) 
[移除-AzDelegation](./Remove-AzDelegation.md) 
[AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="fd664-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>