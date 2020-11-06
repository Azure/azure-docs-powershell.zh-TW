---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453688"
---
# <span data-ttu-id="43066-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="43066-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="43066-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43066-102">SYNOPSIS</span></span>
<span data-ttu-id="43066-103">新增委派至子網。</span><span class="sxs-lookup"><span data-stu-id="43066-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43066-104">句法</span><span class="sxs-lookup"><span data-stu-id="43066-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43066-105">說明</span><span class="sxs-lookup"><span data-stu-id="43066-105">DESCRIPTION</span></span>
<span data-ttu-id="43066-106">**載入 AzureRmDelegation** Cmdlet 會將服務委派新增至 Azure 子網。</span><span class="sxs-lookup"><span data-stu-id="43066-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="43066-107">示例</span><span class="sxs-lookup"><span data-stu-id="43066-107">EXAMPLES</span></span>

### <span data-ttu-id="43066-108">1：新增委派</span><span class="sxs-lookup"><span data-stu-id="43066-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="43066-109">第一個命令會檢索子網所在的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="43066-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="43066-110">第二個命令會將感興趣的子網上隔離（您要委派的子網）。</span><span class="sxs-lookup"><span data-stu-id="43066-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="43066-111">第三個命令會將委派新增到子網中。</span><span class="sxs-lookup"><span data-stu-id="43066-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="43066-112">當您想要讓 SQL 在這個子網上建立介面端點時，這個特殊的範例會很有用。</span><span class="sxs-lookup"><span data-stu-id="43066-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="43066-113">最後一個命令會將更新的子網傳送至伺服器，以實際更新您的子網。</span><span class="sxs-lookup"><span data-stu-id="43066-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="43066-114">參數</span><span class="sxs-lookup"><span data-stu-id="43066-114">PARAMETERS</span></span>

### <span data-ttu-id="43066-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43066-115">-DefaultProfile</span></span>
<span data-ttu-id="43066-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43066-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43066-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="43066-117">-Name</span></span>
<span data-ttu-id="43066-118">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="43066-118">The name of the delegation</span></span>

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

### <span data-ttu-id="43066-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43066-119">-ServiceName</span></span>
<span data-ttu-id="43066-120">應該委派子網之服務的名稱</span><span class="sxs-lookup"><span data-stu-id="43066-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="43066-121">-子網</span><span class="sxs-lookup"><span data-stu-id="43066-121">-Subnet</span></span>
<span data-ttu-id="43066-122">子網上</span><span class="sxs-lookup"><span data-stu-id="43066-122">The subnet</span></span>

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

### <span data-ttu-id="43066-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43066-123">CommonParameters</span></span>
<span data-ttu-id="43066-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43066-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="43066-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43066-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43066-126">輸入</span><span class="sxs-lookup"><span data-stu-id="43066-126">INPUTS</span></span>

### <span data-ttu-id="43066-127">System.object</span><span class="sxs-lookup"><span data-stu-id="43066-127">System.String</span></span>

### <span data-ttu-id="43066-128">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43066-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="43066-129">輸出</span><span class="sxs-lookup"><span data-stu-id="43066-129">OUTPUTS</span></span>

### <span data-ttu-id="43066-130">PSSubnet 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="43066-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="43066-131">筆記</span><span class="sxs-lookup"><span data-stu-id="43066-131">NOTES</span></span>

## <span data-ttu-id="43066-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="43066-132">RELATED LINKS</span></span>
<span data-ttu-id="43066-133">[AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
[AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="43066-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
