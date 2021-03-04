---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRootCertificate.md
ms.openlocfilehash: f83a0f34e23822d5d6ff7c55236fdb81065b7f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915930"
---
# <span data-ttu-id="4bfcb-101">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4bfcb-101">Remove-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="4bfcb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4bfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="4bfcb-103">移除現有的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-103">Removes an existing VPN client root certificate.</span></span>

## <span data-ttu-id="4bfcb-104">語法</span><span class="sxs-lookup"><span data-stu-id="4bfcb-104">SYNTAX</span></span>

```
Remove-AzVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bfcb-105">描述</span><span class="sxs-lookup"><span data-stu-id="4bfcb-105">DESCRIPTION</span></span>
<span data-ttu-id="4bfcb-106">**Remove-Az VpnClientRootCertificate** Cmdlet 會從虛擬網路閘道移除指定的根憑證。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-106">The **Remove-AzVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="4bfcb-107">根憑證是 X.509 憑證，可識別您的根憑證授權單位憑證授權單位機關：閘道中使用的所有其他憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="4bfcb-108">如果您移除的根憑證電腦若將憑證用於驗證用途，就無法再連接到閘道。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>
<span data-ttu-id="4bfcb-109">當您使用 **Remove-Az VpnClientRootCertificate** 時，您必須同時提供憑證名稱和憑證資料的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-109">When you use **Remove-AzVpnClientRootCertificate**, you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="4bfcb-110">有關憑證的文字表示方式詳細資訊，請參閱 *PublicCertData* 參數描述。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="4bfcb-111">例子</span><span class="sxs-lookup"><span data-stu-id="4bfcb-111">EXAMPLES</span></span>

### <span data-ttu-id="4bfcb-112">範例 1：從虛擬網路閘道移除用戶端根憑證</span><span class="sxs-lookup"><span data-stu-id="4bfcb-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```powershell
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="4bfcb-113">此範例會從虛擬網路閘道 ContosoVirtualGateway 移除名為 ContosoRootCertificate 的用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>
<span data-ttu-id="4bfcb-114">第一個命令使用 **Get-Content** Cmdlet 取得先前匯出之憑證的文字標記法;此文字標記法會儲存在名為 $Text 的$Text。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>
<span data-ttu-id="4bfcb-115">接著，第二個命令會使用 for loop 來解壓縮$Text除了第一行和最後一行以外。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="4bfcb-116">此解壓縮的文字會儲存在名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-116">This extracted text is stored in a variable named $CertificateText.</span></span>
<span data-ttu-id="4bfcb-117">第三個命令會使用 $CertificateText 變數中儲存的資訊以及 **Remove-Az VpnClientRootCertificate** Cmdlet，以從閘道移除憑證。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="4bfcb-118">參數</span><span class="sxs-lookup"><span data-stu-id="4bfcb-118">PARAMETERS</span></span>

### <span data-ttu-id="4bfcb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bfcb-119">-DefaultProfile</span></span>
<span data-ttu-id="4bfcb-120">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bfcb-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="4bfcb-121">-PublicCertData</span></span>
<span data-ttu-id="4bfcb-122">指定要移除之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="4bfcb-123">若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64) 編碼，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="4bfcb-124">您應該會看到類似下列輸出 (請注意，實際輸出包含的文字行數會比此處顯示的縮寫範例更多) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW8343NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="4bfcb-125">您可以使用類似以下的 Windows PowerShell 命令來取回 PublicCertData：$Text = Get-Content -Path "C：\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1;$i -lt $Text.Length -1 ;$i++) {$Text$i \[ \] }</span><span class="sxs-lookup"><span data-stu-id="4bfcb-125">You can retrieve the PublicCertData using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="4bfcb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bfcb-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bfcb-127">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-127">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="4bfcb-128">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-128">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="4bfcb-129">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="4bfcb-129">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="4bfcb-130">指定從中移除憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-130">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="4bfcb-131">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="4bfcb-131">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="4bfcb-132">指定此 Cmdlet 移除的用戶端根憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-132">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4bfcb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bfcb-133">CommonParameters</span></span>
<span data-ttu-id="4bfcb-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bfcb-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4bfcb-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bfcb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4bfcb-136">INPUTS</span></span>

### <span data-ttu-id="4bfcb-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4bfcb-137">System.String</span></span>

## <span data-ttu-id="4bfcb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4bfcb-138">OUTPUTS</span></span>

### <span data-ttu-id="4bfcb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4bfcb-139">System.Boolean</span></span>

## <span data-ttu-id="4bfcb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4bfcb-140">NOTES</span></span>

## <span data-ttu-id="4bfcb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4bfcb-141">RELATED LINKS</span></span>

[<span data-ttu-id="4bfcb-142">Add-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4bfcb-142">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4bfcb-143">Get-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4bfcb-143">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="4bfcb-144">New-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4bfcb-144">New-AzVpnClientRootCertificate</span></span>](./New-AzVpnClientRootCertificate.md)


