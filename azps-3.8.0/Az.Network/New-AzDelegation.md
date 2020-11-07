---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966201"
---
# <span data-ttu-id="cc86e-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="cc86e-101">New-AzDelegation</span></span>

## <span data-ttu-id="cc86e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc86e-102">SYNOPSIS</span></span>
<span data-ttu-id="cc86e-103">建立服務委派。</span><span class="sxs-lookup"><span data-stu-id="cc86e-103">Creates a service delegation.</span></span>

## <span data-ttu-id="cc86e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc86e-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cc86e-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc86e-105">DESCRIPTION</span></span>
<span data-ttu-id="cc86e-106">**新的-AzDelegation** Cmdlet 會建立可新增至子網的服務委派。</span><span class="sxs-lookup"><span data-stu-id="cc86e-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="cc86e-107">示例</span><span class="sxs-lookup"><span data-stu-id="cc86e-107">EXAMPLES</span></span>

### <span data-ttu-id="cc86e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="cc86e-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="cc86e-109">第一個 Cmdlet 會建立可新增至子網的委派，並將它儲存在 $delegation 變數中。</span><span class="sxs-lookup"><span data-stu-id="cc86e-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="cc86e-110">第二個和第三個 Cmdlet 會檢索要委派的子網。</span><span class="sxs-lookup"><span data-stu-id="cc86e-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="cc86e-111">第四個 Cmdlet 會將建立的委派新增到感興趣的子網上，而最後的 Cmdlet 會將更新的設定傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="cc86e-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="cc86e-112">參數</span><span class="sxs-lookup"><span data-stu-id="cc86e-112">PARAMETERS</span></span>

### <span data-ttu-id="cc86e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc86e-113">-DefaultProfile</span></span>
<span data-ttu-id="cc86e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc86e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc86e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc86e-115">-Name</span></span>
<span data-ttu-id="cc86e-116">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="cc86e-116">The name of the delegation</span></span>

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

### <span data-ttu-id="cc86e-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cc86e-117">-ServiceName</span></span>
<span data-ttu-id="cc86e-118">應該委派子網之服務的名稱</span><span class="sxs-lookup"><span data-stu-id="cc86e-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="cc86e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc86e-119">CommonParameters</span></span>
<span data-ttu-id="cc86e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc86e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc86e-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc86e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc86e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="cc86e-122">INPUTS</span></span>

### <span data-ttu-id="cc86e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="cc86e-123">System.String</span></span>

## <span data-ttu-id="cc86e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="cc86e-124">OUTPUTS</span></span>

### <span data-ttu-id="cc86e-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="cc86e-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="cc86e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="cc86e-126">NOTES</span></span>

## <span data-ttu-id="cc86e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc86e-127">RELATED LINKS</span></span>

<span data-ttu-id="cc86e-128">[附加 AzDelegation](./Add-AzDelegation.md) 
[AzDelegation](./Get-AzDelegation.md) 
[移除-AzDelegation](./Remove-AzDelegation.md) 
[AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="cc86e-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>