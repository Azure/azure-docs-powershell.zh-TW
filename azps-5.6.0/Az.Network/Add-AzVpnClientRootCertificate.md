---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRootCertificate.md
ms.openlocfilehash: 38a6abb631a77d41e38026edd3bef5abe9c70c01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908837"
---
# <span data-ttu-id="6ac53-101">Add-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac53-101">Add-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="6ac53-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6ac53-102">SYNOPSIS</span></span>
<span data-ttu-id="6ac53-103">新增 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac53-103">Adds a VPN client root certificate.</span></span>

## <span data-ttu-id="6ac53-104">語法</span><span class="sxs-lookup"><span data-stu-id="6ac53-104">SYNTAX</span></span>

```
Add-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ac53-105">描述</span><span class="sxs-lookup"><span data-stu-id="6ac53-105">DESCRIPTION</span></span>
<span data-ttu-id="6ac53-106">**Add-Az VpnClientRootCertificate** Cmdlet 會將根憑證新增到虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="6ac53-106">The **Add-AzVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="6ac53-107">根憑證是 X.509 憑證，可識別您的根憑證授權單位。</span><span class="sxs-lookup"><span data-stu-id="6ac53-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="6ac53-108">根據設計，閘道上使用的所有憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac53-108">By design, all certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="6ac53-109">此 Cmdlet 會指派現有憑證做為閘道根憑證。</span><span class="sxs-lookup"><span data-stu-id="6ac53-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="6ac53-110">如果您沒有可用的 X.509 憑證，您可以透過公用金鑰基礎結構產生一個憑證，或使用憑證產生器 ，例如 makecert.exe。</span><span class="sxs-lookup"><span data-stu-id="6ac53-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>
<span data-ttu-id="6ac53-111">若要新增根憑證，您必須指定憑證名稱，並提供憑證的純文字表示 (請參閱 *PublicCertData* 參數以) 。</span><span class="sxs-lookup"><span data-stu-id="6ac53-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="6ac53-112">Azure 可讓您將多個根憑證指派給閘道。</span><span class="sxs-lookup"><span data-stu-id="6ac53-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="6ac53-113">多個根憑證通常是由包含多個公司使用者的組織所部署。</span><span class="sxs-lookup"><span data-stu-id="6ac53-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="6ac53-114">例子</span><span class="sxs-lookup"><span data-stu-id="6ac53-114">EXAMPLES</span></span>

### <span data-ttu-id="6ac53-115">範例 1：新增用戶端根憑證至虛擬閘道</span><span class="sxs-lookup"><span data-stu-id="6ac53-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="6ac53-116">此範例會將用戶端根憑證新增到名為 ContosoVirtualGateway 的虛擬閘道。</span><span class="sxs-lookup"><span data-stu-id="6ac53-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="6ac53-117">第一個命令使用 **Get-Content** Cmdlet 取得先前匯出的根憑證文字標記法，並儲存名為 $Text 的變數之文字資料。</span><span class="sxs-lookup"><span data-stu-id="6ac53-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>
<span data-ttu-id="6ac53-118">接著，第二個命令會使用 for loop 來抽選第一行和最後一行以外的所有文字。</span><span class="sxs-lookup"><span data-stu-id="6ac53-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="6ac53-119">解壓縮的文字會儲存在名為 $CertificateText 的$CertificateText。</span><span class="sxs-lookup"><span data-stu-id="6ac53-119">The extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="6ac53-120">接著，第三個命令會使用儲存在 $CertificateText 中的文字與 **Add-Az VpnClientRootCertificate** Cmdlet，將根憑證新增到閘道。</span><span class="sxs-lookup"><span data-stu-id="6ac53-120">The third command then uses the text stored in $CertificateText with the **Add-AzVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="6ac53-121">參數</span><span class="sxs-lookup"><span data-stu-id="6ac53-121">PARAMETERS</span></span>

### <span data-ttu-id="6ac53-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ac53-122">-DefaultProfile</span></span>
<span data-ttu-id="6ac53-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ac53-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ac53-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="6ac53-124">-PublicCertData</span></span>
<span data-ttu-id="6ac53-125">指定要新增之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="6ac53-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="6ac53-126">若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64 編碼) ，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="6ac53-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="6ac53-127">當您這麼做時，會看到類似下列的 (請注意，實際輸出的文字行數會比此處顯示的縮寫範例多出許多行文字) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8 343NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。</span><span class="sxs-lookup"><span data-stu-id="6ac53-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="6ac53-128">您可以使用類似以下的 Windows PowerShell 命令來取回此資料： `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="6ac53-128">You can retrieve this data by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

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

### <span data-ttu-id="6ac53-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ac53-129">-ResourceGroupName</span></span>
<span data-ttu-id="6ac53-130">指定根憑證指派給的資源組名。</span><span class="sxs-lookup"><span data-stu-id="6ac53-130">Specifies the name of the resource group that the root certificate is assigned to.</span></span>
<span data-ttu-id="6ac53-131">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="6ac53-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="6ac53-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6ac53-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6ac53-133">指定新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac53-133">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

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

### <span data-ttu-id="6ac53-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="6ac53-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="6ac53-135">指定此 Cmdlet 新增的用戶端根憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="6ac53-135">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ac53-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ac53-136">CommonParameters</span></span>
<span data-ttu-id="6ac53-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6ac53-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ac53-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6ac53-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ac53-139">輸入</span><span class="sxs-lookup"><span data-stu-id="6ac53-139">INPUTS</span></span>

### <span data-ttu-id="6ac53-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6ac53-140">System.String</span></span>

## <span data-ttu-id="6ac53-141">輸出</span><span class="sxs-lookup"><span data-stu-id="6ac53-141">OUTPUTS</span></span>

### <span data-ttu-id="6ac53-142">Microsoft.Azure.Commands.Network.models.PS VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac53-142">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="6ac53-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6ac53-143">NOTES</span></span>

## <span data-ttu-id="6ac53-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ac53-144">RELATED LINKS</span></span>

[<span data-ttu-id="6ac53-145">Get-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac53-145">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6ac53-146">New-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac53-146">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)

[<span data-ttu-id="6ac53-147">Remove-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6ac53-147">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


