---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451844"
---
# <span data-ttu-id="a6338-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="a6338-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="a6338-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6338-102">SYNOPSIS</span></span>
<span data-ttu-id="a6338-103">建立服務委派。</span><span class="sxs-lookup"><span data-stu-id="a6338-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6338-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6338-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6338-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6338-105">DESCRIPTION</span></span>
<span data-ttu-id="a6338-106">**新的-AzureRmDelegation** Cmdlet 會建立可新增至子網的服務委派。</span><span class="sxs-lookup"><span data-stu-id="a6338-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="a6338-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6338-107">EXAMPLES</span></span>

### <span data-ttu-id="a6338-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a6338-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="a6338-109">第一個 Cmdlet 會建立可新增至子網的委派，並將它儲存在 $delegation 變數中。</span><span class="sxs-lookup"><span data-stu-id="a6338-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="a6338-110">第二個和第三個 Cmdlet 會檢索要委派的子網。</span><span class="sxs-lookup"><span data-stu-id="a6338-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="a6338-111">第四個 Cmdlet 會將建立的委派新增到感興趣的子網上，而最後的 Cmdlet 會將更新的設定傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="a6338-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="a6338-112">參數</span><span class="sxs-lookup"><span data-stu-id="a6338-112">PARAMETERS</span></span>

### <span data-ttu-id="a6338-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6338-113">-DefaultProfile</span></span>
<span data-ttu-id="a6338-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6338-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6338-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6338-115">-Name</span></span>
<span data-ttu-id="a6338-116">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="a6338-116">The name of the delegation</span></span>

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

### <span data-ttu-id="a6338-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a6338-117">-ServiceName</span></span>
<span data-ttu-id="a6338-118">應該委派子網之服務的名稱</span><span class="sxs-lookup"><span data-stu-id="a6338-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6338-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6338-119">CommonParameters</span></span>
<span data-ttu-id="a6338-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6338-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a6338-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6338-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6338-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a6338-122">INPUTS</span></span>

### <span data-ttu-id="a6338-123">System.object</span><span class="sxs-lookup"><span data-stu-id="a6338-123">System.String</span></span>

## <span data-ttu-id="a6338-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a6338-124">OUTPUTS</span></span>

### <span data-ttu-id="a6338-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a6338-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a6338-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a6338-126">NOTES</span></span>

## <span data-ttu-id="a6338-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6338-127">RELATED LINKS</span></span>
<span data-ttu-id="a6338-128">[附加 AzureRmDelegation](./Add-AzureRmDelegation.md) 
[AzureRmDelegation](./Get-AzureRmDelegation.md) 
[移除-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="a6338-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
