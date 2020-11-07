---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625784"
---
# <span data-ttu-id="97a1a-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="97a1a-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="97a1a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="97a1a-103">從提供的子網上移除服務委派。</span><span class="sxs-lookup"><span data-stu-id="97a1a-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a1a-104">句法</span><span class="sxs-lookup"><span data-stu-id="97a1a-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a1a-105">說明</span><span class="sxs-lookup"><span data-stu-id="97a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="97a1a-106">**AzureRmDelegation** Cmdlet 會在子網中使用委派，並從該子網上移除已命名的委派。</span><span class="sxs-lookup"><span data-stu-id="97a1a-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="97a1a-107">示例</span><span class="sxs-lookup"><span data-stu-id="97a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="97a1a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="97a1a-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="97a1a-109">在這個範例中，在 _[新增委派至現有的子網]_ 下的第一個半形 () 與 [AzureRmDelegation](./Add-AzureRmDelegation.md)相同。</span><span class="sxs-lookup"><span data-stu-id="97a1a-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="97a1a-110">在第二部分中，前兩個 Cmdlet 會檢索感興趣的子網上，並重新整理本機複本與伺服器上的內容。</span><span class="sxs-lookup"><span data-stu-id="97a1a-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="97a1a-111">第三個 Cmdlet 會從 _mySubnet_ 中移除在前半部建立的委派，並將更新的子網儲存在 _$subnet_ 中。</span><span class="sxs-lookup"><span data-stu-id="97a1a-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="97a1a-112">最後一個 Cmdlet 會使用已移除的委派來補救伺服器。</span><span class="sxs-lookup"><span data-stu-id="97a1a-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="97a1a-113">參數</span><span class="sxs-lookup"><span data-stu-id="97a1a-113">PARAMETERS</span></span>

### <span data-ttu-id="97a1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a1a-114">-DefaultProfile</span></span>
<span data-ttu-id="97a1a-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97a1a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a1a-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="97a1a-116">-Name</span></span>
<span data-ttu-id="97a1a-117">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="97a1a-117">The name of the delegation</span></span>

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

### <span data-ttu-id="97a1a-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="97a1a-118">-ServiceName</span></span>
<span data-ttu-id="97a1a-119">應該委派子網之服務的名稱</span><span class="sxs-lookup"><span data-stu-id="97a1a-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="97a1a-120">-子網</span><span class="sxs-lookup"><span data-stu-id="97a1a-120">-Subnet</span></span>
<span data-ttu-id="97a1a-121">要從中移除委派的子網</span><span class="sxs-lookup"><span data-stu-id="97a1a-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="97a1a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a1a-122">CommonParameters</span></span>
<span data-ttu-id="97a1a-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97a1a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a1a-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97a1a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a1a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="97a1a-125">INPUTS</span></span>

### <span data-ttu-id="97a1a-126">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97a1a-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="97a1a-127">System.object</span><span class="sxs-lookup"><span data-stu-id="97a1a-127">System.String</span></span>
## <span data-ttu-id="97a1a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="97a1a-128">OUTPUTS</span></span>

### <span data-ttu-id="97a1a-129">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97a1a-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="97a1a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="97a1a-130">NOTES</span></span>

## <span data-ttu-id="97a1a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="97a1a-131">RELATED LINKS</span></span>

<span data-ttu-id="97a1a-132">[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[AzureRmDelegation](./Get-AzureRmDelegation.md) 
[新-AzureRmDelegation](./New-AzureRmDelegation.md) 
[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="97a1a-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
