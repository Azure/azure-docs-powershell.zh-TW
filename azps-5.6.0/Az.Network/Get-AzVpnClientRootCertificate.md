---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: 6211b422e9dfc16358303d766edecf437b44240d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917973"
---
# <span data-ttu-id="83d41-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="83d41-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="83d41-102">簡介</span><span class="sxs-lookup"><span data-stu-id="83d41-102">SYNOPSIS</span></span>
<span data-ttu-id="83d41-103">獲得 VPN 根憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83d41-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="83d41-104">語法</span><span class="sxs-lookup"><span data-stu-id="83d41-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>] -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d41-105">描述</span><span class="sxs-lookup"><span data-stu-id="83d41-105">DESCRIPTION</span></span>
<span data-ttu-id="83d41-106">**Get-Az VpnClientRootCertificate** Cmdlet 會返回指派給虛擬網路閘道的根憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83d41-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="83d41-107">根憑證是 X.509 憑證，可識別您的根憑證授權單位憑證授權單位機關：閘道中使用的所有其他憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="83d41-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="83d41-108">根據預設 **，Get-Az VpnClientRootCertificate** 會返回指派給閘道的所有根憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="83d41-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="83d41-109"> (閘道可以有一個根憑證。) 不過，您可以包含 **VpnClientRootCertificateName** 參數，將所退回的資料限制為特定的憑證。</span><span class="sxs-lookup"><span data-stu-id="83d41-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="83d41-110">例子</span><span class="sxs-lookup"><span data-stu-id="83d41-110">EXAMPLES</span></span>

### <span data-ttu-id="83d41-111">範例 1：取得所有根憑證的資訊</span><span class="sxs-lookup"><span data-stu-id="83d41-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="83d41-112">此命令會獲得指派給名為 ContosoVirtualNetwork 之虛擬網路閘道之所有根憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="83d41-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="83d41-113">範例 2：取得特定根憑證的資訊</span><span class="sxs-lookup"><span data-stu-id="83d41-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="83d41-114">此命令是範例 1 中顯示的命令變化。</span><span class="sxs-lookup"><span data-stu-id="83d41-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="83d41-115">不過，在此案例中，會包含 *VpnClientRootCertificateName* 參數，以將所返回的資料限制為特定的根憑證：ContosoRootClientCertificate。</span><span class="sxs-lookup"><span data-stu-id="83d41-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="83d41-116">參數</span><span class="sxs-lookup"><span data-stu-id="83d41-116">PARAMETERS</span></span>

### <span data-ttu-id="83d41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d41-117">-DefaultProfile</span></span>
<span data-ttu-id="83d41-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="83d41-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d41-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d41-119">-ResourceGroupName</span></span>
<span data-ttu-id="83d41-120">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="83d41-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="83d41-121">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="83d41-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="83d41-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="83d41-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="83d41-123">指定指派根憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="83d41-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="83d41-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="83d41-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="83d41-125">指定此 Cmdlet 所獲取的用戶端根憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="83d41-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83d41-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d41-126">CommonParameters</span></span>
<span data-ttu-id="83d41-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="83d41-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d41-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83d41-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d41-129">輸入</span><span class="sxs-lookup"><span data-stu-id="83d41-129">INPUTS</span></span>

### <span data-ttu-id="83d41-130">System.String</span><span class="sxs-lookup"><span data-stu-id="83d41-130">System.String</span></span>

## <span data-ttu-id="83d41-131">輸出</span><span class="sxs-lookup"><span data-stu-id="83d41-131">OUTPUTS</span></span>

### <span data-ttu-id="83d41-132">Microsoft.Azure.Commands.Network.models.PS VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="83d41-132">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="83d41-133">筆記</span><span class="sxs-lookup"><span data-stu-id="83d41-133">NOTES</span></span>

## <span data-ttu-id="83d41-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="83d41-134">RELATED LINKS</span></span>

[<span data-ttu-id="83d41-135">Add-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="83d41-135">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="83d41-136">New-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="83d41-136">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="83d41-137">Remove-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="83d41-137">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


