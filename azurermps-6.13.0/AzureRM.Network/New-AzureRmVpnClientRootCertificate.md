---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 18d634650248ea03c43b8ea24ec15aa3a2b79528
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448339"
---
# <span data-ttu-id="b5c2e-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c2e-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="b5c2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5c2e-102">SYNOPSIS</span></span>
<span data-ttu-id="b5c2e-103">建立新的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5c2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5c2e-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5c2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b5c2e-105">DESCRIPTION</span></span>
<span data-ttu-id="b5c2e-106">**新的-AzureRmVpnClientRootCertificate** Cmdlet 會建立新的 VPN 根憑證，以用於虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="b5c2e-107">根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="b5c2e-108">這個 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="b5c2e-109">相反地，由 **New-AzureRmVpnClientRootCertificate** 建立的憑證會與建立新閘道時的 New-AzureRmVirtualNetworkGateway Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="b5c2e-110">例如，假設您建立新的憑證，並將它儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="b5c2e-111">在建立新的虛擬閘道時，您可以使用該憑證物件。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="b5c2e-112">例如， `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="b5c2e-112">For instance, `New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="b5c2e-113">如需詳細資訊，請參閱 New-AzureRmVirtualNetworkGateway Cmdlet 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="b5c2e-114">示例</span><span class="sxs-lookup"><span data-stu-id="b5c2e-114">EXAMPLES</span></span>

### <span data-ttu-id="b5c2e-115">範例1：建立 aclient 根憑證</span><span class="sxs-lookup"><span data-stu-id="b5c2e-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="b5c2e-116">這個範例會建立一個用戶端根憑證，並將憑證物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="b5c2e-117">這個變數可以由 **新的-AzureRmVirtualNetworkGateway** Cmdlet 使用，以將根憑證新增至新的虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="b5c2e-118">第一個命令使用 **取得內容** Cmdlet 來取得根憑證先前匯出的文字標記法;該文字資料會儲存在名為 $Text 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="b5c2e-119">然後，第二個命令會使用 for 迴圈來提取除了第一行和最後一行以外的所有文字，並將提取的文字儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="b5c2e-120">第三個命令使用 **AzureRmVpnClientRootCertificate** Cmdlet 來建立證書，並將建立的物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="b5c2e-121">參數</span><span class="sxs-lookup"><span data-stu-id="b5c2e-121">PARAMETERS</span></span>

### <span data-ttu-id="b5c2e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5c2e-122">-DefaultProfile</span></span>
<span data-ttu-id="b5c2e-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5c2e-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5c2e-124">-Name</span></span>
<span data-ttu-id="b5c2e-125">指定新用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="b5c2e-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="b5c2e-126">-PublicCertData</span></span>
<span data-ttu-id="b5c2e-127">指定要新增之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="b5c2e-128">若要取得文字標記法，請 (使用 Base64 編碼) 將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="b5c2e-129">您應該會看到類似這個 (的輸出，請注意，實際的輸出將包含的文字行數超過) 以下所示的縮寫範例：-----開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----結束憑證-----PublicCertData 是由第一列之間的所有行所組成 (-----開始憑證-----) ，而最後一行 (-----在檔案中-----最終憑證 ) 。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="b5c2e-130">您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData： $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="b5c2e-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="b5c2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5c2e-131">CommonParameters</span></span>
<span data-ttu-id="b5c2e-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5c2e-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5c2e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5c2e-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b5c2e-134">INPUTS</span></span>

### <span data-ttu-id="b5c2e-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b5c2e-135">System.String</span></span>

## <span data-ttu-id="b5c2e-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b5c2e-136">OUTPUTS</span></span>

### <span data-ttu-id="b5c2e-137">PSVpnClientRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="b5c2e-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="b5c2e-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b5c2e-138">NOTES</span></span>

## <span data-ttu-id="b5c2e-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5c2e-139">RELATED LINKS</span></span>

[<span data-ttu-id="b5c2e-140">附加 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c2e-140">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="b5c2e-141">AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c2e-141">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="b5c2e-142">移除-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="b5c2e-142">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


