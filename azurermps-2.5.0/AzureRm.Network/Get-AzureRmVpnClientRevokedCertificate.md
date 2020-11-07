---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientrevokedcertificate
schema: 2.0.0
ms.openlocfilehash: 62fc89cefadc91445a64850d6a0e5ee23d6163f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800829"
---
# <span data-ttu-id="3335c-101">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3335c-101">Get-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="3335c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3335c-102">SYNOPSIS</span></span>
<span data-ttu-id="3335c-103">取得 VPN 用戶端吊銷憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3335c-103">Gets information about VPN client-revocation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3335c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3335c-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3335c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3335c-105">DESCRIPTION</span></span>
<span data-ttu-id="3335c-106">**AzureRmVpnClientRevokedCertificate** Cmdlet 會傳回指派給虛擬網路閘道之用戶端吊銷憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3335c-106">The **Get-AzureRmVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="3335c-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="3335c-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="3335c-108">**AzureRmVpnClientRevokedCertificate** 可讓您傳回閘道上所有用戶端吊銷憑證的相關資訊，或使用 *VpnClientRevokedCertificateName* 參數來取得單一憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3335c-108">**Get-AzureRmVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="3335c-109">示例</span><span class="sxs-lookup"><span data-stu-id="3335c-109">EXAMPLES</span></span>

### <span data-ttu-id="3335c-110">範例1：取得所有用戶端吊銷憑證的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3335c-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="3335c-111">這個命令會取得與名為 ContosoVirtualNetworkGateway 的虛擬網路閘道相關的所有用戶端吊銷證書資訊。</span><span class="sxs-lookup"><span data-stu-id="3335c-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="3335c-112">範例2：取得特定用戶端吊銷憑證的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3335c-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="3335c-113">這個命令是範例1中所示命令的變化。</span><span class="sxs-lookup"><span data-stu-id="3335c-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="3335c-114">但在此情況下， *VpnClientRevokedCertificateName* 參數是用來將傳回的資料限制為特定的用戶端吊銷憑證：名稱為 ContosoRevokedClientCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="3335c-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="3335c-115">參數</span><span class="sxs-lookup"><span data-stu-id="3335c-115">PARAMETERS</span></span>

### <span data-ttu-id="3335c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3335c-116">-DefaultProfile</span></span>
<span data-ttu-id="3335c-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3335c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3335c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3335c-118">-ResourceGroupName</span></span>
<span data-ttu-id="3335c-119">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3335c-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="3335c-120">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="3335c-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="3335c-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="3335c-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="3335c-122">指定指派吊銷的憑證資訊的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="3335c-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="3335c-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="3335c-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="3335c-124">指定此 Cmdlet 所取得之 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="3335c-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3335c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3335c-125">CommonParameters</span></span>
<span data-ttu-id="3335c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3335c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3335c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3335c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3335c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3335c-128">INPUTS</span></span>

## <span data-ttu-id="3335c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3335c-129">OUTPUTS</span></span>

###  
<span data-ttu-id="3335c-130">**AzureRmVpnClientRevokedCertificate** 會傳回 PSVpnClientRevokedCertificate 物件的實例（ **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** 物件）。</span><span class="sxs-lookup"><span data-stu-id="3335c-130">**Get-AzureRmVpnClientRevokedCertificate** returns instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="3335c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3335c-131">NOTES</span></span>

## <span data-ttu-id="3335c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="3335c-132">RELATED LINKS</span></span>

[<span data-ttu-id="3335c-133">附加 AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3335c-133">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="3335c-134">新-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3335c-134">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="3335c-135">移除-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="3335c-135">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


