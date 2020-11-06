---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 9f20b0540481c40326bc3656e3f65534c22f9b24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448343"
---
# <span data-ttu-id="cded0-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="cded0-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="cded0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cded0-102">SYNOPSIS</span></span>
<span data-ttu-id="cded0-103">建立新的 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="cded0-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cded0-104">句法</span><span class="sxs-lookup"><span data-stu-id="cded0-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cded0-105">說明</span><span class="sxs-lookup"><span data-stu-id="cded0-105">DESCRIPTION</span></span>
<span data-ttu-id="cded0-106">**新的-AzureRmVpnClientRevokedCertificate** Cmdlet 會 (VPN) 用戶端吊銷憑證建立新的虛擬私人網路絡，以在虛擬網路閘道上使用。</span><span class="sxs-lookup"><span data-stu-id="cded0-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="cded0-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="cded0-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="cded0-108">這個 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。</span><span class="sxs-lookup"><span data-stu-id="cded0-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="cded0-109">相反地，由 **New-AzureRmVpnClientRevokedCertificate** 建立的憑證會在建立新的閘道時與 New-AzureRmVirtualNetworkGateway Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cded0-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="cded0-110">例如，假設您建立新的憑證，並將它儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cded0-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="cded0-111">當您建立新的虛擬閘道時，您可以使用該憑證物件。</span><span class="sxs-lookup"><span data-stu-id="cded0-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="cded0-112">例如， `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="cded0-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`</span></span>
<span data-ttu-id="cded0-113">如需詳細資訊，請參閱 New-AzureRmVirtualNetworkGateway Cmdlet 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="cded0-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="cded0-114">示例</span><span class="sxs-lookup"><span data-stu-id="cded0-114">EXAMPLES</span></span>

### <span data-ttu-id="cded0-115">範例1：建立新的用戶端吊銷憑證</span><span class="sxs-lookup"><span data-stu-id="cded0-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="cded0-116">這個命令會建立一個新的用戶端吊銷憑證，並將憑證物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="cded0-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="cded0-117">這個變數可以由 **新的-AzureRmVirtualNetworkGateway** Cmdlet 使用，以將憑證新增到新的虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="cded0-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="cded0-118">參數</span><span class="sxs-lookup"><span data-stu-id="cded0-118">PARAMETERS</span></span>

### <span data-ttu-id="cded0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cded0-119">-DefaultProfile</span></span>
<span data-ttu-id="cded0-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cded0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cded0-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cded0-121">-Name</span></span>
<span data-ttu-id="cded0-122">指定新用戶端吊銷憑證的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="cded0-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="cded0-123">-指紋</span><span class="sxs-lookup"><span data-stu-id="cded0-123">-Thumbprint</span></span>
<span data-ttu-id="cded0-124">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="cded0-124">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="cded0-125">您可以使用類似以下的 Windows PowerShell 命令，傳回憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root`</span><span class="sxs-lookup"><span data-stu-id="cded0-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`</span></span>
<span data-ttu-id="cded0-126">上述命令會傳回在根憑證存放區中找到之所有本機電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="cded0-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="cded0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cded0-127">CommonParameters</span></span>
<span data-ttu-id="cded0-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cded0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cded0-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cded0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cded0-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cded0-130">INPUTS</span></span>

### <span data-ttu-id="cded0-131">所有</span><span class="sxs-lookup"><span data-stu-id="cded0-131">None</span></span>

## <span data-ttu-id="cded0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cded0-132">OUTPUTS</span></span>

### <span data-ttu-id="cded0-133">PSVpnClientRevokedCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cded0-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="cded0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cded0-134">NOTES</span></span>

## <span data-ttu-id="cded0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="cded0-135">RELATED LINKS</span></span>

[<span data-ttu-id="cded0-136">附加 AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="cded0-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="cded0-137">AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="cded0-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="cded0-138">移除-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="cded0-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


