---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: 779793bcc3df7ae62cc7ae7cc900ed863e8f4ee8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910701"
---
# <span data-ttu-id="49f78-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="49f78-101">Add-AzDelegation</span></span>

## <span data-ttu-id="49f78-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49f78-102">SYNOPSIS</span></span>
<span data-ttu-id="49f78-103">新增委派至子網。</span><span class="sxs-lookup"><span data-stu-id="49f78-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="49f78-104">語法</span><span class="sxs-lookup"><span data-stu-id="49f78-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49f78-105">描述</span><span class="sxs-lookup"><span data-stu-id="49f78-105">DESCRIPTION</span></span>
<span data-ttu-id="49f78-106">**Add-AzDelegation** Cmdlet 會將服務委派新增到 Azure 子網。</span><span class="sxs-lookup"><span data-stu-id="49f78-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="49f78-107">例子</span><span class="sxs-lookup"><span data-stu-id="49f78-107">EXAMPLES</span></span>

### <span data-ttu-id="49f78-108">範例 1：新增委派</span><span class="sxs-lookup"><span data-stu-id="49f78-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="49f78-109">第一個命令會取回子網所位於的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="49f78-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="49f78-110">第二個命令會隔離您想要委派的子網。</span><span class="sxs-lookup"><span data-stu-id="49f78-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="49f78-111">第三個命令會新增委派至子網。</span><span class="sxs-lookup"><span data-stu-id="49f78-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="49f78-112">當您想要啟用 SQL 在此子網中建立介面端點時，這個特定範例會很有用。</span><span class="sxs-lookup"><span data-stu-id="49f78-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="49f78-113">最後一個命令會傳送更新的子網至伺服器，以實際更新您的子網。</span><span class="sxs-lookup"><span data-stu-id="49f78-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="49f78-114">參數</span><span class="sxs-lookup"><span data-stu-id="49f78-114">PARAMETERS</span></span>

### <span data-ttu-id="49f78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49f78-115">-DefaultProfile</span></span>
<span data-ttu-id="49f78-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49f78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49f78-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="49f78-117">-Name</span></span>
<span data-ttu-id="49f78-118">委派的名稱</span><span class="sxs-lookup"><span data-stu-id="49f78-118">The name of the delegation</span></span>

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

### <span data-ttu-id="49f78-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49f78-119">-ServiceName</span></span>
<span data-ttu-id="49f78-120">應委派子網的服務名稱</span><span class="sxs-lookup"><span data-stu-id="49f78-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="49f78-121">-子網</span><span class="sxs-lookup"><span data-stu-id="49f78-121">-Subnet</span></span>
<span data-ttu-id="49f78-122">子網</span><span class="sxs-lookup"><span data-stu-id="49f78-122">The subnet</span></span>

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

### <span data-ttu-id="49f78-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49f78-123">CommonParameters</span></span>
<span data-ttu-id="49f78-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49f78-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49f78-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="49f78-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49f78-126">輸入</span><span class="sxs-lookup"><span data-stu-id="49f78-126">INPUTS</span></span>

### <span data-ttu-id="49f78-127">System.String</span><span class="sxs-lookup"><span data-stu-id="49f78-127">System.String</span></span>

### <span data-ttu-id="49f78-128">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="49f78-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="49f78-129">輸出</span><span class="sxs-lookup"><span data-stu-id="49f78-129">OUTPUTS</span></span>

### <span data-ttu-id="49f78-130">Microsoft.Azure.Commands.Network.models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="49f78-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="49f78-131">筆記</span><span class="sxs-lookup"><span data-stu-id="49f78-131">NOTES</span></span>

## <span data-ttu-id="49f78-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="49f78-132">RELATED LINKS</span></span>

<span data-ttu-id="49f78-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="49f78-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>