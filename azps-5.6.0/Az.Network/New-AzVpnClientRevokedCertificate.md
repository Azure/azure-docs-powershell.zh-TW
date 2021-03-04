---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 85a35fe4c6b988ce6f5320d308582fb722cc5791
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904946"
---
# <span data-ttu-id="6a79f-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6a79f-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6a79f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a79f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a79f-103">建立新的 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="6a79f-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="6a79f-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a79f-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a79f-105">描述</span><span class="sxs-lookup"><span data-stu-id="6a79f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a79f-106">**New-Az VpnClientRevokedCertificate Cmdlet** 會建立新的虛擬私人網路 (VPN) 用戶端吊銷憑證，以用於虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6a79f-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="6a79f-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="6a79f-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="6a79f-108">此 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。</span><span class="sxs-lookup"><span data-stu-id="6a79f-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="6a79f-109">相反地 **，New-Az VpnClientRevokedCertificate** 所建立憑證在建立新閘道時，會與 New-AzVirtualNetworkGateway Cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="6a79f-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="6a79f-110">例如，假設您建立新憑證，然後儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6a79f-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="6a79f-111">然後，您可以在建立新虛擬閘道時使用該憑證物件。</span><span class="sxs-lookup"><span data-stu-id="6a79f-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="6a79f-112">例如， `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="6a79f-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="6a79f-113">詳細資訊請參閱 Cmdlet New-AzVirtualNetworkGateway檔。</span><span class="sxs-lookup"><span data-stu-id="6a79f-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="6a79f-114">例子</span><span class="sxs-lookup"><span data-stu-id="6a79f-114">EXAMPLES</span></span>

### <span data-ttu-id="6a79f-115">範例 1：建立新的用戶端撤銷憑證</span><span class="sxs-lookup"><span data-stu-id="6a79f-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="6a79f-116">此命令會建立新的用戶端撤銷憑證，並且將憑證物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="6a79f-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="6a79f-117">**New-AzVirtualNetworkGateway** Cmdlet 接著可以使用這個變數，將憑證新增到新的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6a79f-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="6a79f-118">參數</span><span class="sxs-lookup"><span data-stu-id="6a79f-118">PARAMETERS</span></span>

### <span data-ttu-id="6a79f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a79f-119">-DefaultProfile</span></span>
<span data-ttu-id="6a79f-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a79f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a79f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a79f-121">-Name</span></span>
<span data-ttu-id="6a79f-122">指定新的用戶端吊銷憑證的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="6a79f-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a79f-123">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="6a79f-123">-Thumbprint</span></span>
<span data-ttu-id="6a79f-124">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a79f-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="6a79f-125">您可以使用類似以下的 Windows PowerShell 命令，針對憑證返回指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="6a79f-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="6a79f-126">上一個命令會針對根憑證存放區中找到的所有 Local Computer 憑證，會返回資訊。</span><span class="sxs-lookup"><span data-stu-id="6a79f-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a79f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a79f-127">CommonParameters</span></span>
<span data-ttu-id="6a79f-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a79f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a79f-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6a79f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a79f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6a79f-130">INPUTS</span></span>

### <span data-ttu-id="6a79f-131">沒有</span><span class="sxs-lookup"><span data-stu-id="6a79f-131">None</span></span>

## <span data-ttu-id="6a79f-132">輸出</span><span class="sxs-lookup"><span data-stu-id="6a79f-132">OUTPUTS</span></span>

### <span data-ttu-id="6a79f-133">Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6a79f-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="6a79f-134">筆記</span><span class="sxs-lookup"><span data-stu-id="6a79f-134">NOTES</span></span>

## <span data-ttu-id="6a79f-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a79f-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a79f-136">Add-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6a79f-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6a79f-137">Get-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6a79f-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="6a79f-138">Remove-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="6a79f-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


