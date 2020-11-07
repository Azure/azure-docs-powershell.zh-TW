---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b83af7bc0242ddf1c1ed5c182cd0be7c2b7d8a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625874"
---
# <span data-ttu-id="7f9a7-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f9a7-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="7f9a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f9a7-102">SYNOPSIS</span></span>
<span data-ttu-id="7f9a7-103">建立新的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f9a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f9a7-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f9a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f9a7-105">DESCRIPTION</span></span>
<span data-ttu-id="7f9a7-106">**新的-AzureRmVpnClientRootCertificate** Cmdlet 會建立新的 VPN 根憑證，以用於虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="7f9a7-107">根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="7f9a7-108">這個 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="7f9a7-109">相反地，由 **New-AzureRmVpnClientRootCertificate** 建立的憑證會與建立新閘道時的 New-AzureRmVirtualNetworkGateway Cmdlet 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="7f9a7-110">例如，假設您建立新的憑證，並將它儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="7f9a7-111">在建立新的虛擬閘道時，您可以使用該憑證物件。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="7f9a7-112">例如，</span><span class="sxs-lookup"><span data-stu-id="7f9a7-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="7f9a7-113">如需詳細資訊，請參閱 New-AzureRmVirtualNetworkGateway Cmdlet 的相關檔。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="7f9a7-114">示例</span><span class="sxs-lookup"><span data-stu-id="7f9a7-114">EXAMPLES</span></span>

### <span data-ttu-id="7f9a7-115">範例1：建立 aclient 根憑證</span><span class="sxs-lookup"><span data-stu-id="7f9a7-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="7f9a7-116">這個範例會建立一個用戶端根憑證，並將憑證物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="7f9a7-117">這個變數可以由 **新的-AzureRmVirtualNetworkGateway** Cmdlet 使用，以將根憑證新增至新的虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="7f9a7-118">第一個命令使用 **取得內容** Cmdlet 來取得根憑證先前匯出的文字標記法;該文字資料會儲存在名為 $Text 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="7f9a7-119">然後，第二個命令會使用 for 迴圈來提取除了第一行和最後一行以外的所有文字，並將提取的文字儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="7f9a7-120">第三個命令使用 **AzureRmVpnClientRootCertificate** Cmdlet 來建立證書，並將建立的物件儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="7f9a7-121">參數</span><span class="sxs-lookup"><span data-stu-id="7f9a7-121">PARAMETERS</span></span>

### <span data-ttu-id="7f9a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9a7-122">-DefaultProfile</span></span>
<span data-ttu-id="7f9a7-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f9a7-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f9a7-124">-Name</span></span>
<span data-ttu-id="7f9a7-125">指定新用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-125">Specifies a name for the new client root certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a7-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="7f9a7-126">-PublicCertData</span></span>
<span data-ttu-id="7f9a7-127">指定要新增之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="7f9a7-128">若要取得文字標記法，請 (使用 Base64 編碼) 將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="7f9a7-129">您應該會看到類似這個 (的輸出，請注意，實際的輸出會包含許多其他行的文字，而不是此處顯示的縮寫範例) ：</span><span class="sxs-lookup"><span data-stu-id="7f9a7-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="7f9a7-130">-----開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----[結束憑證]-----</span><span class="sxs-lookup"><span data-stu-id="7f9a7-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="7f9a7-131">PublicCertData 是由第一行之間的所有行所 (-----[開始憑證-----) ，而最後一行 (-----在檔案中-----[最終憑證 ) 。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="7f9a7-132">您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData：</span><span class="sxs-lookup"><span data-stu-id="7f9a7-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="7f9a7-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="7f9a7-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="7f9a7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9a7-134">CommonParameters</span></span>
<span data-ttu-id="7f9a7-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9a7-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9a7-137">輸入</span><span class="sxs-lookup"><span data-stu-id="7f9a7-137">INPUTS</span></span>

###  
<span data-ttu-id="7f9a7-138">這個 Cmdlet 不接受流水線輸入。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="7f9a7-139">輸出</span><span class="sxs-lookup"><span data-stu-id="7f9a7-139">OUTPUTS</span></span>

###  
<span data-ttu-id="7f9a7-140">這個 Cmdlet 會建立 PSVpnClientRootCertificate 物件的新實例（ **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** 物件）。</span><span class="sxs-lookup"><span data-stu-id="7f9a7-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="7f9a7-141">筆記</span><span class="sxs-lookup"><span data-stu-id="7f9a7-141">NOTES</span></span>

## <span data-ttu-id="7f9a7-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f9a7-142">RELATED LINKS</span></span>

[<span data-ttu-id="7f9a7-143">附加 AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f9a7-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="7f9a7-144">AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f9a7-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="7f9a7-145">移除-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7f9a7-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


