---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionikesa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionIkeSa.md
ms.openlocfilehash: 6b0eb456c2134e6ed64d8e6c441db041776fcf39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128918"
---
# <span data-ttu-id="eb566-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span><span class="sxs-lookup"><span data-stu-id="eb566-101">Get-AzVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="eb566-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb566-102">SYNOPSIS</span></span>
<span data-ttu-id="eb566-103">取得虛擬網路閘道連線的 IKE 安全關聯</span><span class="sxs-lookup"><span data-stu-id="eb566-103">Get IKE Security Associations of a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="eb566-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb566-104">SYNTAX</span></span>

### <span data-ttu-id="eb566-105">ByName</span><span class="sxs-lookup"><span data-stu-id="eb566-105">ByName</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-Name <String>] -ResourceGroupName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb566-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb566-106">ByInputObject</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa -InputObject <PSVirtualNetworkGatewayConnection> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb566-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb566-107">ByResourceId</span></span>
```
Get-AzVirtualNetworkGatewayConnectionIkeSa [-ResourceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb566-108">說明</span><span class="sxs-lookup"><span data-stu-id="eb566-108">DESCRIPTION</span></span>
<span data-ttu-id="eb566-109">**AzVirtualNetworkGatewayConnectionIkeSa** Cmdlet 會根據連接名稱和資源群組名稱，傳回連線的 IKE 安全關聯。</span><span class="sxs-lookup"><span data-stu-id="eb566-109">The **Get-AzVirtualNetworkGatewayConnectionIkeSa** cmdlet returns the IKE Security Associations of your connection based on the Connection Name and Resource Group Name.</span></span>
<span data-ttu-id="eb566-110">如果未指定-Name 參數就發出 **AzVirtualNetworkGatewayConnection** Cmdlet，則輸出將不會顯示 IKE 安全關聯。</span><span class="sxs-lookup"><span data-stu-id="eb566-110">If the **Get-AzVirtualNetworkGatewayConnection** cmdlet is issued without specifying the -Name parameter, the output will not show the IKE Security Associations.</span></span>

## <span data-ttu-id="eb566-111">示例</span><span class="sxs-lookup"><span data-stu-id="eb566-111">EXAMPLES</span></span>

### <span data-ttu-id="eb566-112">範例1</span><span class="sxs-lookup"><span data-stu-id="eb566-112">Example 1</span></span>
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

<span data-ttu-id="eb566-113">針對資源群組 "myRG" 中的名稱 "myTunnel"，傳回虛擬網路閘道連線的 IKE 安全關聯</span><span class="sxs-lookup"><span data-stu-id="eb566-113">Returns the IKE Security Associations for the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="eb566-114">參數</span><span class="sxs-lookup"><span data-stu-id="eb566-114">PARAMETERS</span></span>

### <span data-ttu-id="eb566-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb566-115">-AsJob</span></span>
<span data-ttu-id="eb566-116">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb566-116">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="eb566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb566-117">-DefaultProfile</span></span>
<span data-ttu-id="eb566-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb566-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb566-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb566-119">-InputObject</span></span>
<span data-ttu-id="eb566-120">需要取得 IKE SAs 的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="eb566-120">The virtual network gateway connection object for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="eb566-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb566-121">-Name</span></span>
<span data-ttu-id="eb566-122">需要取得 IKE SAs 的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="eb566-122">The virtual network gateway connection name for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="eb566-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb566-123">-ResourceGroupName</span></span>
<span data-ttu-id="eb566-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb566-124">The resource group name.</span></span>

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

### <span data-ttu-id="eb566-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb566-125">-ResourceId</span></span>
<span data-ttu-id="eb566-126">需要取得 IKE SAs 之虛擬網路閘道連線的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb566-126">The Azure resource ID of the Virtual Network Gateway Connection for which IKE SAs needs to be fetched.</span></span>

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

### <span data-ttu-id="eb566-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb566-127">CommonParameters</span></span>
<span data-ttu-id="eb566-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb566-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb566-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb566-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb566-130">輸入</span><span class="sxs-lookup"><span data-stu-id="eb566-130">INPUTS</span></span>

### <span data-ttu-id="eb566-131">System.object</span><span class="sxs-lookup"><span data-stu-id="eb566-131">System.String</span></span>

## <span data-ttu-id="eb566-132">輸出</span><span class="sxs-lookup"><span data-stu-id="eb566-132">OUTPUTS</span></span>

### <span data-ttu-id="eb566-133">PSVirtualNetworkGatewayConnectionIkeSa 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eb566-133">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnectionIkeSa</span></span>

## <span data-ttu-id="eb566-134">筆記</span><span class="sxs-lookup"><span data-stu-id="eb566-134">NOTES</span></span>

## <span data-ttu-id="eb566-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb566-135">RELATED LINKS</span></span>
