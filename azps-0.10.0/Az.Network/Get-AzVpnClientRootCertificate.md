---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 16754F70-9619-4F68-86E9-5C8B27812707
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientRootCertificate.md
ms.openlocfilehash: c55fb1af95b1c0f85e2b36732f6235ad0c6c78d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794327"
---
# <span data-ttu-id="2f3dc-101">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3dc-101">Get-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="2f3dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="2f3dc-103">取得 VPN 根憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-103">Gets information about VPN root certificates.</span></span>

## <span data-ttu-id="2f3dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f3dc-104">SYNTAX</span></span>

```
Get-AzVpnClientRootCertificate [-VpnClientRootCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f3dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="2f3dc-105">DESCRIPTION</span></span>
<span data-ttu-id="2f3dc-106">**AzVpnClientRootCertificate** Cmdlet 會傳回指派給虛擬網路閘道之根憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-106">The **Get-AzVpnClientRootCertificate** cmdlet returns information about the root certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="2f3dc-107">根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="2f3dc-108">根據預設， **AzVpnClientRootCertificate** 會傳回指派給閘道的所有根憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-108">By default, **Get-AzVpnClientRootCertificate** returns information about all the root certificates assigned to a gateway.</span></span>
<span data-ttu-id="2f3dc-109"> (閘道可以有一個以上的根憑證。 ) 不過，透過包括 **VpnClientRootCertificateName** 參數，您可以將傳回的資料限制為特定的憑證。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-109">(Gateways can have more than one root certificate.) However, by including the **VpnClientRootCertificateName** parameter you can limit the returned data to a specific certificate.</span></span>

## <span data-ttu-id="2f3dc-110">示例</span><span class="sxs-lookup"><span data-stu-id="2f3dc-110">EXAMPLES</span></span>

### <span data-ttu-id="2f3dc-111">範例1：取得所有根憑證的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2f3dc-111">Example 1: Get information about all root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2f3dc-112">這個命令會取得指派給名為 ContosoVirtualNetwork 的虛擬網路閘道所有根憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-112">This command gets information about all the root certificates assigned to a virtual network gateway named ContosoVirtualNetwork.</span></span>

### <span data-ttu-id="2f3dc-113">範例2：取得特定根憑證的相關資訊</span><span class="sxs-lookup"><span data-stu-id="2f3dc-113">Example 2: Get information about specific root certificates</span></span>
```
PS C:\>Get-AzVpnClientRootCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRootCertificateName "ContosoRootClientCertificate"
```

<span data-ttu-id="2f3dc-114">這個命令是範例1中所示命令的變化。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-114">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="2f3dc-115">但在此情況下，會包含 *VpnClientRootCertificateName* 參數，以便將傳回的資料限制為特定的根憑證： ContosoRootClientCertificate。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-115">In this case, however, the *VpnClientRootCertificateName* parameter is included in order to limit the returned data to a specific root certificate: ContosoRootClientCertificate.</span></span>

## <span data-ttu-id="2f3dc-116">參數</span><span class="sxs-lookup"><span data-stu-id="2f3dc-116">PARAMETERS</span></span>

### <span data-ttu-id="2f3dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f3dc-117">-DefaultProfile</span></span>
<span data-ttu-id="2f3dc-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f3dc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f3dc-119">-ResourceGroupName</span></span>
<span data-ttu-id="2f3dc-120">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-120">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="2f3dc-121">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-121">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="2f3dc-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="2f3dc-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="2f3dc-123">指定指派根憑證之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-123">Specifies the name of the virtual network gateway where the root certificate is assigned.</span></span>

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

### <span data-ttu-id="2f3dc-124">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="2f3dc-124">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="2f3dc-125">指定此 Cmdlet 所取得之用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-125">Specifies the name of the client root certificate that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f3dc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f3dc-126">CommonParameters</span></span>
<span data-ttu-id="2f3dc-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f3dc-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f3dc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2f3dc-129">INPUTS</span></span>

## <span data-ttu-id="2f3dc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2f3dc-130">OUTPUTS</span></span>

###  
<span data-ttu-id="2f3dc-131">**AzVpnClientRootCertificate** 會取得 PSVpnClientRootCertificate 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** 物件）。</span><span class="sxs-lookup"><span data-stu-id="2f3dc-131">**Get-AzVpnClientRootCertificate** gets instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="2f3dc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2f3dc-132">NOTES</span></span>

## <span data-ttu-id="2f3dc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f3dc-133">RELATED LINKS</span></span>

[<span data-ttu-id="2f3dc-134">附加 AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3dc-134">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="2f3dc-135">新-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3dc-135">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="2f3dc-136">移除-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2f3dc-136">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


