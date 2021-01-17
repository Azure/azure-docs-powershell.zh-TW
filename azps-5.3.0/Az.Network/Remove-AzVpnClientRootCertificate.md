---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: 5cb4a57994ad8b15048bfc22dadefbbee031aaf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448947"
---
# <span data-ttu-id="026d6-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="026d6-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="026d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="026d6-102">SYNOPSIS</span></span>
<span data-ttu-id="026d6-103">移除現有的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="026d6-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="026d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="026d6-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="026d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="026d6-105">DESCRIPTION</span></span>
<span data-ttu-id="026d6-106">**AzVpnClientRootCertificate** Cmdlet 會將指定的根憑證從虛擬網路閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="026d6-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="026d6-107">根憑證是 x.509 憑證，可識別您的根憑證授權單位：所有其他在閘道使用的憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="026d6-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="026d6-108">如果您移除使用憑證進行驗證的根憑證電腦，將無法再連線至閘道。</span><span class="sxs-lookup"><span data-stu-id="026d6-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="026d6-109">當您使用 **AzVpnClientRootCertificate** 時，您必須同時提供憑證名稱和憑證資料的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="026d6-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="026d6-110">如需有關憑證之文字標記法的詳細資訊，請參閱 *PublicCertData* 參數說明。</span><span class="sxs-lookup"><span data-stu-id="026d6-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="026d6-111">示例</span><span class="sxs-lookup"><span data-stu-id="026d6-111">EXAMPLES</span></span>

### <span data-ttu-id="026d6-112">範例1：從虛擬網路閘道移除用戶端根憑證</span><span class="sxs-lookup"><span data-stu-id="026d6-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="026d6-113">這個範例會從虛擬網路閘道 ContosoVirtualGateway 中移除名為 ContosoRootCertificate 的用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="026d6-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="026d6-114">第一個命令使用 **取得內容** Cmdlet 來取得前一次匯出的憑證文字標記法;此文字標記法儲存在名為 $Text 的變數中。</span><span class="sxs-lookup"><span data-stu-id="026d6-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="026d6-115">然後，第二個命令會使用 for 迴圈來提取 $Text 中除第一行和最後一行以外的所有文字。</span><span class="sxs-lookup"><span data-stu-id="026d6-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="026d6-116">這個提取的文字會儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="026d6-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="026d6-117">第三個命令會使用儲存在 $CertificateText 變數中的資訊，以及 **AzVpnClientRootCertificate** Cmdlet 來移除閘道的憑證。</span><span class="sxs-lookup"><span data-stu-id="026d6-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="026d6-118">參數</span><span class="sxs-lookup"><span data-stu-id="026d6-118">PARAMETERS</span></span>

### <span data-ttu-id="026d6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="026d6-119">-DefaultProfile</span></span>
<span data-ttu-id="026d6-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="026d6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="026d6-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="026d6-121">-PublicCertData</span></span>
<span data-ttu-id="026d6-122">指定要移除之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="026d6-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="026d6-123">若要取得文字標記法，請 (使用 Base64) 編碼將您的憑證匯出為 .cer 格式，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="026d6-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="026d6-124">您應該會看到類似 (如下所示的輸出，請注意，實際輸出會包含的文字行多於以下所示的縮寫範例) ：-----的開始憑證-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----結束憑證----- ( 開始憑證----------，而最後一行 )  ( 在檔案中-----最終憑證-----) 。</span><span class="sxs-lookup"><span data-stu-id="026d6-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="026d6-125">您可以使用類似以下的 Windows PowerShell 命令來檢索 PublicCertData： $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i = 1;$i-lt $Text; Length-1;$i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="026d6-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="026d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="026d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="026d6-127">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="026d6-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="026d6-128">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="026d6-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="026d6-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="026d6-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="026d6-130">指定從中移除憑證的虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="026d6-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="026d6-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="026d6-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="026d6-132">指定此 Cmdlet 移除之用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="026d6-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="026d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="026d6-133">CommonParameters</span></span>
<span data-ttu-id="026d6-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="026d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="026d6-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="026d6-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="026d6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="026d6-136">INPUTS</span></span>

### <span data-ttu-id="026d6-137">System.object</span><span class="sxs-lookup"><span data-stu-id="026d6-137">System.String</span></span>

## <span data-ttu-id="026d6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="026d6-138">OUTPUTS</span></span>

### <span data-ttu-id="026d6-139">System.object</span><span class="sxs-lookup"><span data-stu-id="026d6-139">System.Boolean</span></span>

## <span data-ttu-id="026d6-140">筆記</span><span class="sxs-lookup"><span data-stu-id="026d6-140">NOTES</span></span>

## <span data-ttu-id="026d6-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="026d6-141">RELATED LINKS</span></span>

[<span data-ttu-id="026d6-142">附加 AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="026d6-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="026d6-143">AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="026d6-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="026d6-144">新-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="026d6-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


