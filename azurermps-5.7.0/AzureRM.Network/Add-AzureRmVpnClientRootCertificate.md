---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 11b4d3cca8d7cad8d3fb4cfcc4e256d1934592d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446220"
---
# <span data-ttu-id="0b6e9-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0b6e9-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="0b6e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b6e9-103">新增 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b6e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b6e9-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b6e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="0b6e9-106">**載入 AzureRmVpnClientRootCertificate** Cmdlet 會將根憑證新增至虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="0b6e9-107">根憑證是 x.509 可識別您根憑證授權單位的憑證。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="0b6e9-108">根據設計，在閘道上使用的所有憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="0b6e9-109">這個 Cmdlet 會將現有的憑證指派為閘道根憑證。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="0b6e9-110">如果您沒有可用的 x.509 憑證，您可以透過公開金鑰基礎結構產生一個證書，或使用證書發生器（例如 makecert.exe）。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="0b6e9-111">若要新增根憑證，您必須指定憑證名稱並提供憑證的純文字標記法 (請參閱 *PublicCertData* 參數，以取得詳細資訊) 。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="0b6e9-112">Azure 可讓您將一個以上的根憑證指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="0b6e9-113">多個根憑證通常是由組織加入來自多個公司的使用者所部署。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="0b6e9-114">示例</span><span class="sxs-lookup"><span data-stu-id="0b6e9-114">EXAMPLES</span></span>

### <span data-ttu-id="0b6e9-115">範例1：將用戶端根憑證新增至虛擬閘道</span><span class="sxs-lookup"><span data-stu-id="0b6e9-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="0b6e9-116">這個範例會將用戶端根憑證新增到名為 ContosoVirtualGateway 的虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="0b6e9-117">第一個命令會使用 **取得內容** Cmdlet 來取得根憑證先前匯出的文字標記法，並將該文字資料儲存在名為 $Text 的變數。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="0b6e9-118">然後，第二個命令會使用 for 迴圈來提取除第一行和最後一行以外的所有文字。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="0b6e9-119">解壓縮的文字會儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="0b6e9-120">然後，第三個命令會使用儲存在 $CertificateText 中的文字與 **AzureRmVpnClientRootCertificate** Cmdlet，以將根憑證新增至閘道。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="0b6e9-121">參數</span><span class="sxs-lookup"><span data-stu-id="0b6e9-121">PARAMETERS</span></span>

### <span data-ttu-id="0b6e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b6e9-122">-DefaultProfile</span></span>
<span data-ttu-id="0b6e9-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b6e9-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="0b6e9-124">-PublicCertData</span></span>
<span data-ttu-id="0b6e9-125">指定要新增之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="0b6e9-126">若要取得文字標記法，請 (使用 Base64 編碼) 將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="0b6e9-127">當您這樣做時，您會看到類似下列 (的輸出，請注意，實際的輸出將包含許多行的文字，而不是此處顯示的縮寫範例) ：</span><span class="sxs-lookup"><span data-stu-id="0b6e9-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="0b6e9-128">-----開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----[結束憑證]-----</span><span class="sxs-lookup"><span data-stu-id="0b6e9-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="0b6e9-129">PublicCertData 是由第一行之間的所有行所 (-----[開始憑證-----) ，而最後一行 (-----在檔案中-----[最終憑證 ) 。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="0b6e9-130">您可以使用類似以下的 Windows PowerShell 命令來檢索這個資料： `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="0b6e9-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="0b6e9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b6e9-131">-ResourceGroupName</span></span>
<span data-ttu-id="0b6e9-132">指定指派根憑證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="0b6e9-133">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="0b6e9-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="0b6e9-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="0b6e9-135">指定新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="0b6e9-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="0b6e9-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="0b6e9-137">指定此 Cmdlet 所新增之用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b6e9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b6e9-138">CommonParameters</span></span>
<span data-ttu-id="0b6e9-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b6e9-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b6e9-141">輸入</span><span class="sxs-lookup"><span data-stu-id="0b6e9-141">INPUTS</span></span>

### <span data-ttu-id="0b6e9-142">所有</span><span class="sxs-lookup"><span data-stu-id="0b6e9-142">None</span></span>
<span data-ttu-id="0b6e9-143">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0b6e9-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b6e9-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0b6e9-144">OUTPUTS</span></span>

### <span data-ttu-id="0b6e9-145">PSVpnClientRootCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0b6e9-145">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="0b6e9-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0b6e9-146">NOTES</span></span>

## <span data-ttu-id="0b6e9-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b6e9-147">RELATED LINKS</span></span>

[<span data-ttu-id="0b6e9-148">AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0b6e9-148">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="0b6e9-149">新-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0b6e9-149">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="0b6e9-150">移除-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0b6e9-150">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)

