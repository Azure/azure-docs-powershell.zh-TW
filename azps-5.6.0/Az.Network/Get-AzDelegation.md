---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: cbb560b04219b0a77c9158afe3b76b1b9461cdb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905909"
---
# <span data-ttu-id="03dfd-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="03dfd-101">Get-AzDelegation</span></span>

## <span data-ttu-id="03dfd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="03dfd-103">取得委派 (或所有位於) 子網上的委派。</span><span class="sxs-lookup"><span data-stu-id="03dfd-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="03dfd-104">語法</span><span class="sxs-lookup"><span data-stu-id="03dfd-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03dfd-105">描述</span><span class="sxs-lookup"><span data-stu-id="03dfd-105">DESCRIPTION</span></span>
<span data-ttu-id="03dfd-106">**Get-AzDelegation** Cmdlet 會從子網取得命名委派。</span><span class="sxs-lookup"><span data-stu-id="03dfd-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="03dfd-107">如果沒有命名委派，它會在提供子網上，會返回所有委派。</span><span class="sxs-lookup"><span data-stu-id="03dfd-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="03dfd-108">例子</span><span class="sxs-lookup"><span data-stu-id="03dfd-108">EXAMPLES</span></span>

### <span data-ttu-id="03dfd-109">1：正在取回特定委派</span><span class="sxs-lookup"><span data-stu-id="03dfd-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="03dfd-110">第一行會取回感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="03dfd-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="03dfd-111">第二行顯示稱為「myDelegation」之委派的委派資訊。</span><span class="sxs-lookup"><span data-stu-id="03dfd-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="03dfd-112">2：取回所有子網的子網</span><span class="sxs-lookup"><span data-stu-id="03dfd-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="03dfd-113">第一行會取回感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="03dfd-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="03dfd-114">第二行會儲存 _mySubnet_ 上所有活動的清單，$delegations變數。</span><span class="sxs-lookup"><span data-stu-id="03dfd-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="03dfd-115">參數</span><span class="sxs-lookup"><span data-stu-id="03dfd-115">PARAMETERS</span></span>

### <span data-ttu-id="03dfd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03dfd-116">-DefaultProfile</span></span>
<span data-ttu-id="03dfd-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03dfd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03dfd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="03dfd-118">-Name</span></span>
<span data-ttu-id="03dfd-119">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="03dfd-119">The name of the delegation</span></span>

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

### <span data-ttu-id="03dfd-120">-子網</span><span class="sxs-lookup"><span data-stu-id="03dfd-120">-Subnet</span></span>
<span data-ttu-id="03dfd-121">子網</span><span class="sxs-lookup"><span data-stu-id="03dfd-121">The subnet</span></span>

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

### <span data-ttu-id="03dfd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03dfd-122">CommonParameters</span></span>
<span data-ttu-id="03dfd-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03dfd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03dfd-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03dfd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03dfd-125">輸入</span><span class="sxs-lookup"><span data-stu-id="03dfd-125">INPUTS</span></span>

### <span data-ttu-id="03dfd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="03dfd-126">System.String</span></span>

### <span data-ttu-id="03dfd-127">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="03dfd-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="03dfd-128">輸出</span><span class="sxs-lookup"><span data-stu-id="03dfd-128">OUTPUTS</span></span>

### <span data-ttu-id="03dfd-129">Microsoft.Azure.Commands.Network.Models.PSD標記法</span><span class="sxs-lookup"><span data-stu-id="03dfd-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="03dfd-130">筆記</span><span class="sxs-lookup"><span data-stu-id="03dfd-130">NOTES</span></span>

## <span data-ttu-id="03dfd-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="03dfd-131">RELATED LINKS</span></span>

<span data-ttu-id="03dfd-132">[Add-AzDelegation](./Add-AzDelegation.md) 
[New-AzDelegation](./New-AzDelegation.md) 
[Remove-AzDelegation](./Remove-AzDelegation.md) 
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="03dfd-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
