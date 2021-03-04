---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 0f5cedd29b7dcc296494519fe40f8ea7e0edb445
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904985"
---
# <span data-ttu-id="2a3d4-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="2a3d4-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="2a3d4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a3d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2a3d4-103">取得虛擬網路閘道連接的 IKE 安全性關聯</span><span class="sxs-lookup"><span data-stu-id="2a3d4-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="2a3d4-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a3d4-104">SYNTAX</span></span>

### <span data-ttu-id="2a3d4-105">ByName</span><span class="sxs-lookup"><span data-stu-id="2a3d4-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3d4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a3d4-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a3d4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a3d4-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a3d4-108">描述</span><span class="sxs-lookup"><span data-stu-id="2a3d4-108">DESCRIPTION</span></span>
<span data-ttu-id="2a3d4-109">**Get-AzVirtualNetworkGatewayConnectionConnectionConnEctionSa** Cmdlet 會根據連接名稱和資源組名，會以您的連接之 IKE 安全性關聯為基礎。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="2a3d4-110">如果 **Get-AzVirtualNetworkGatewayConnection** Cmdlet 在未指定 -Name 參數的情況下發行，輸出將不會顯示 IKE 安全性關聯。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="2a3d4-111">例子</span><span class="sxs-lookup"><span data-stu-id="2a3d4-111">EXAMPLES</span></span>

### <span data-ttu-id="2a3d4-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2a3d4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualNetworkGatewayConnectionIkeSa -ResourceGroupName myRG -Name myTunnel
localEndpoint              : 52.180.160.154
remoteEndpoint             : 104.208.54.1
initiatorCookie            : 5490733703579933026
responderCookie            : 15460013388959380535
localUdpEncapsulationPort  : 0
remoteUdpEncapsulationPort : 0
encryption                 : AES256
integrity                  : SHA1
dhGroup                    : DHGroup2
lifeTimeSeconds            : 28800
isSaInitiator              : True
elapsedTimeInseconds       : 23092
quickModeSa                : {}
```

<span data-ttu-id="2a3d4-113">在資源群組 "myRG" 中，以名稱 "myTuntun" 為虛擬網路閘道連接的 IKE 安全性關聯</span><span class="sxs-lookup"><span data-stu-id="2a3d4-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="2a3d4-114">參數</span><span class="sxs-lookup"><span data-stu-id="2a3d4-114">PARAMETERS</span></span>

### <span data-ttu-id="2a3d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a3d4-115">-AsJob</span></span>
<span data-ttu-id="2a3d4-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-116">Run cmdlet in the background.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a3d4-117">-DefaultProfile</span></span>
<span data-ttu-id="2a3d4-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a3d4-119">-InputObject</span></span>
<span data-ttu-id="2a3d4-120">需要抓取 IKE SAs 的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a3d4-121">-Name</span></span>
<span data-ttu-id="2a3d4-122">需要取取 IKE SAS 的虛擬網路閘道連接名稱。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a3d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="2a3d4-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a3d4-125">-ResourceId</span></span>
<span data-ttu-id="2a3d4-126">需要抓取 IKE SAS 之虛擬網路閘道連接的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a3d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a3d4-127">CommonParameters</span></span>
<span data-ttu-id="2a3d4-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a3d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a3d4-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a3d4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a3d4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2a3d4-130">INPUTS</span></span>

### <span data-ttu-id="2a3d4-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2a3d4-131">System.String</span></span>

## <span data-ttu-id="2a3d4-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2a3d4-132">OUTPUTS</span></span>

### <span data-ttu-id="2a3d4-133">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnectionWorkSa</span><span class="sxs-lookup"><span data-stu-id="2a3d4-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="2a3d4-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2a3d4-134">NOTES</span></span>

## <span data-ttu-id="2a3d4-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a3d4-135">RELATED LINKS</span></span>
