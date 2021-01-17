---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450226"
---
# <span data-ttu-id="98d46-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="98d46-101">Get-AzDelegation</span></span>

## <span data-ttu-id="98d46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="98d46-102">SYNOPSIS</span></span>
<span data-ttu-id="98d46-103">在指定的子網上取得委派 (或所有委派) 。</span><span class="sxs-lookup"><span data-stu-id="98d46-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="98d46-104">句法</span><span class="sxs-lookup"><span data-stu-id="98d46-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98d46-105">說明</span><span class="sxs-lookup"><span data-stu-id="98d46-105">DESCRIPTION</span></span>
<span data-ttu-id="98d46-106">**AzDelegation** Cmdlet 會從子網上取得命名委派。</span><span class="sxs-lookup"><span data-stu-id="98d46-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="98d46-107">如果沒有命名委派，它會在所提供的子網上傳回所有委派。</span><span class="sxs-lookup"><span data-stu-id="98d46-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="98d46-108">示例</span><span class="sxs-lookup"><span data-stu-id="98d46-108">EXAMPLES</span></span>

### <span data-ttu-id="98d46-109">1：檢索特定委派</span><span class="sxs-lookup"><span data-stu-id="98d46-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="98d46-110">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="98d46-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="98d46-111">第二行顯示名為「myDelegation」的委派的委派資訊。</span><span class="sxs-lookup"><span data-stu-id="98d46-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="98d46-112">2：檢索所有子網委派</span><span class="sxs-lookup"><span data-stu-id="98d46-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="98d46-113">第一行會檢索感興趣的子網。</span><span class="sxs-lookup"><span data-stu-id="98d46-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="98d46-114">第二行儲存 $delegations 變數中 _mySubnet_ 的所有委派清單。</span><span class="sxs-lookup"><span data-stu-id="98d46-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="98d46-115">參數</span><span class="sxs-lookup"><span data-stu-id="98d46-115">PARAMETERS</span></span>

### <span data-ttu-id="98d46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d46-116">-DefaultProfile</span></span>
<span data-ttu-id="98d46-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="98d46-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d46-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="98d46-118">-Name</span></span>
<span data-ttu-id="98d46-119">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="98d46-119">The name of the delegation</span></span>

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

### <span data-ttu-id="98d46-120">-子網</span><span class="sxs-lookup"><span data-stu-id="98d46-120">-Subnet</span></span>
<span data-ttu-id="98d46-121">子網上</span><span class="sxs-lookup"><span data-stu-id="98d46-121">The subnet</span></span>

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

### <span data-ttu-id="98d46-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d46-122">CommonParameters</span></span>
<span data-ttu-id="98d46-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="98d46-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d46-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="98d46-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d46-125">輸入</span><span class="sxs-lookup"><span data-stu-id="98d46-125">INPUTS</span></span>

### <span data-ttu-id="98d46-126">System.object</span><span class="sxs-lookup"><span data-stu-id="98d46-126">System.String</span></span>

### <span data-ttu-id="98d46-127">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="98d46-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="98d46-128">輸出</span><span class="sxs-lookup"><span data-stu-id="98d46-128">OUTPUTS</span></span>

### <span data-ttu-id="98d46-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="98d46-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="98d46-130">筆記</span><span class="sxs-lookup"><span data-stu-id="98d46-130">NOTES</span></span>

## <span data-ttu-id="98d46-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="98d46-131">RELATED LINKS</span></span>

<span data-ttu-id="98d46-132">[附加 AzDelegation](./Add-AzDelegation.md) 
[新-AzDelegation](./New-AzDelegation.md) 
[移除-AzDelegation](./Remove-AzDelegation.md) 
[AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="98d46-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
