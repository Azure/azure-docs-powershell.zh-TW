---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 05626BF7-F886-4C76-8FC2-DDF783DEB539
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: c5ceef5ec70ac337180c8e2fcf6bb567c68391a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901974"
---
# <span data-ttu-id="16bd8-101">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="16bd8-101">Get-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="16bd8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="16bd8-103">獲得 VPN 用戶端吊銷憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16bd8-103">Gets information about VPN client-revocation certificates.</span></span>

## <span data-ttu-id="16bd8-104">語法</span><span class="sxs-lookup"><span data-stu-id="16bd8-104">SYNTAX</span></span>

```
Get-AzVpnClientRevokedCertificate [-VpnClientRevokedCertificateName <String>]
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16bd8-105">描述</span><span class="sxs-lookup"><span data-stu-id="16bd8-105">DESCRIPTION</span></span>
<span data-ttu-id="16bd8-106">**Get-Az VpnClientRevokedCertificate** Cmdlet 會返回指派給虛擬網路閘道的用戶端吊銷憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16bd8-106">The **Get-AzVpnClientRevokedCertificate** cmdlet returns information about the client-revocation certificates assigned to a virtual network gateway.</span></span>
<span data-ttu-id="16bd8-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="16bd8-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="16bd8-108">**Get-Az VpnClientRevokedCertificate** 可讓您返回閘道上所有用戶端吊銷憑證的資訊，或使用 *VpnClientRevokedCertificateName* 參數取得單一憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="16bd8-108">**Get-AzVpnClientRevokedCertificate** enables you to return information about all the client-revocation certificates on the gateway or, by using the *VpnClientRevokedCertificateName* parameter, to get information about a single certificate.</span></span>

## <span data-ttu-id="16bd8-109">例子</span><span class="sxs-lookup"><span data-stu-id="16bd8-109">EXAMPLES</span></span>

### <span data-ttu-id="16bd8-110">範例 1：取得所有用戶端吊銷憑證的資訊</span><span class="sxs-lookup"><span data-stu-id="16bd8-110">Example 1: Get information about all client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="16bd8-111">此命令會獲得與名為 ContosoVirtualNetworkGateway 之虛擬網路閘道相關聯的所有用戶端吊銷憑證相關資訊。</span><span class="sxs-lookup"><span data-stu-id="16bd8-111">This command gets information about all the client-revocation certificates associated with the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>

### <span data-ttu-id="16bd8-112">範例 2：取得特定用戶端吊銷憑證的資訊</span><span class="sxs-lookup"><span data-stu-id="16bd8-112">Example 2: Get information about specific client-revocation certificates</span></span>
```
PS C:\>Get-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"
```

<span data-ttu-id="16bd8-113">此命令是範例 1 中顯示的命令變化。</span><span class="sxs-lookup"><span data-stu-id="16bd8-113">This command is a variation of the command shown in Example 1.</span></span>
<span data-ttu-id="16bd8-114">不過，在此案例中 *，VpnClientRevokedCertificateName* 參數是用來將所退回的資料限制為特定的用戶端撤銷憑證：名稱為 ContosoRevokedClientCertificate 的憑證。</span><span class="sxs-lookup"><span data-stu-id="16bd8-114">In this case, however, the *VpnClientRevokedCertificateName* parameter is used to limit the returned data to a specific client-revoked certificate: the certificate with the name ContosoRevokedClientCertificate.</span></span>

## <span data-ttu-id="16bd8-115">參數</span><span class="sxs-lookup"><span data-stu-id="16bd8-115">PARAMETERS</span></span>

### <span data-ttu-id="16bd8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16bd8-116">-DefaultProfile</span></span>
<span data-ttu-id="16bd8-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16bd8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16bd8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16bd8-118">-ResourceGroupName</span></span>
<span data-ttu-id="16bd8-119">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="16bd8-119">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="16bd8-120">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="16bd8-120">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="16bd8-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="16bd8-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="16bd8-122">指定指派已撤銷憑證資訊的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="16bd8-122">Specifies the name of the virtual network gateway where the revoked certificate information is assigned.</span></span>

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

### <span data-ttu-id="16bd8-123">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="16bd8-123">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="16bd8-124">指定此 Cmdlet 所獲得 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="16bd8-124">Specifies the name of the VPN client certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="16bd8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16bd8-125">CommonParameters</span></span>
<span data-ttu-id="16bd8-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16bd8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16bd8-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16bd8-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16bd8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="16bd8-128">INPUTS</span></span>

### <span data-ttu-id="16bd8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="16bd8-129">System.String</span></span>

## <span data-ttu-id="16bd8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="16bd8-130">OUTPUTS</span></span>

### <span data-ttu-id="16bd8-131">Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="16bd8-131">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="16bd8-132">筆記</span><span class="sxs-lookup"><span data-stu-id="16bd8-132">NOTES</span></span>

## <span data-ttu-id="16bd8-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="16bd8-133">RELATED LINKS</span></span>

[<span data-ttu-id="16bd8-134">Add-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="16bd8-134">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="16bd8-135">New-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="16bd8-135">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="16bd8-136">Remove-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="16bd8-136">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


