---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 866a3b9ac28de57a71fce5fb84b2fa1144d0ff8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904945"
---
# <span data-ttu-id="dbe60-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe60-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="dbe60-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dbe60-102">SYNOPSIS</span></span>
<span data-ttu-id="dbe60-103">建立新的 VPN 用戶端根憑證。</span><span class="sxs-lookup"><span data-stu-id="dbe60-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="dbe60-104">語法</span><span class="sxs-lookup"><span data-stu-id="dbe60-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbe60-105">描述</span><span class="sxs-lookup"><span data-stu-id="dbe60-105">DESCRIPTION</span></span>
<span data-ttu-id="dbe60-106">**New-Az VpnClientRootCertificate Cmdlet** 會建立新 VPN 根憑證，以用於虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="dbe60-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="dbe60-107">根憑證是 X.509 憑證，可識別您的根憑證授權單位憑證授權單位機關：閘道中使用的所有其他憑證都根信任憑證。</span><span class="sxs-lookup"><span data-stu-id="dbe60-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="dbe60-108">此 Cmdlet 會建立未指派給虛擬閘道的獨立憑證。</span><span class="sxs-lookup"><span data-stu-id="dbe60-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="dbe60-109">相反地 **，New-Az VpnClientRootCertificate** 所建立憑證會與 New-AzVirtualNetworkGateway Cmdlet 一起使用，以建立新閘道。</span><span class="sxs-lookup"><span data-stu-id="dbe60-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="dbe60-110">例如，假設您建立新憑證，然後儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dbe60-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="dbe60-111">接著，您可以在建立新虛擬閘道時使用該憑證物件。</span><span class="sxs-lookup"><span data-stu-id="dbe60-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="dbe60-112">例如， `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="dbe60-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="dbe60-113">詳細資訊請參閱 Cmdlet New-AzVirtualNetworkGateway檔。</span><span class="sxs-lookup"><span data-stu-id="dbe60-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="dbe60-114">例子</span><span class="sxs-lookup"><span data-stu-id="dbe60-114">EXAMPLES</span></span>

### <span data-ttu-id="dbe60-115">範例 1：建立用戶端根憑證</span><span class="sxs-lookup"><span data-stu-id="dbe60-115">Example 1: Create a client root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="dbe60-116">此範例會建立用戶端根憑證，並儲存在名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dbe60-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="dbe60-117">**New-AzVirtualNetworkGateway** Cmdlet 接著可以使用這個變數，將根憑證新增加到新的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="dbe60-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="dbe60-118">第一個命令使用 **Get-Content** Cmdlet 取得先前匯出之根憑證的文字標記法;文字資料會儲存在名為 $Text 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dbe60-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="dbe60-119">接著，第二個命令使用 for loop 來抽選第一行和最後一行以外的所有文字，將解壓縮的文字儲存于名為 $CertificateText 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dbe60-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="dbe60-120">第三個命令使用 **New-Az VpnClientRootCertificate Cmdlet** 建立憑證，將建立的物件儲存于名為 $Certificate 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dbe60-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="dbe60-121">參數</span><span class="sxs-lookup"><span data-stu-id="dbe60-121">PARAMETERS</span></span>

### <span data-ttu-id="dbe60-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbe60-122">-DefaultProfile</span></span>
<span data-ttu-id="dbe60-123">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbe60-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbe60-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="dbe60-124">-Name</span></span>
<span data-ttu-id="dbe60-125">指定新用戶端根憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbe60-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="dbe60-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="dbe60-126">-PublicCertData</span></span>
<span data-ttu-id="dbe60-127">指定要新增之根憑證的文字標記法。</span><span class="sxs-lookup"><span data-stu-id="dbe60-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="dbe60-128">若要取得文字標記法，請以 .cer 格式匯出憑證 (Base64 編碼) ，然後在文字編輯器中開啟產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="dbe60-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="dbe60-129">您應該會看到類似此輸出 (請注意，實際輸出包含的文字行數會比此處顯示的縮寫範例更多) ：----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HgUNEW834 3NMJklo09982VBVFAw8w ----- END 憑證 ----- PublicCertData 是由第一行 (----- BEGIN CERTIFICATE -----) 和檔案中最後一行 (----- END CERTIFICATE -----) 之間的所有行所建立。</span><span class="sxs-lookup"><span data-stu-id="dbe60-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="dbe60-130">您可以使用類似以下的 Windows PowerShell 命令來取回 PublicCertData：$Text = Get-Content -Path "C：\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1;$i -lt $Text.Length -1 ;$i++) {$Text$i \[ \] }</span><span class="sxs-lookup"><span data-stu-id="dbe60-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertificate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="dbe60-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbe60-131">CommonParameters</span></span>
<span data-ttu-id="dbe60-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dbe60-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbe60-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dbe60-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbe60-134">輸入</span><span class="sxs-lookup"><span data-stu-id="dbe60-134">INPUTS</span></span>

### <span data-ttu-id="dbe60-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dbe60-135">System.String</span></span>

## <span data-ttu-id="dbe60-136">輸出</span><span class="sxs-lookup"><span data-stu-id="dbe60-136">OUTPUTS</span></span>

### <span data-ttu-id="dbe60-137">Microsoft.Azure.Commands.Network.models.PS VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe60-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="dbe60-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dbe60-138">NOTES</span></span>

## <span data-ttu-id="dbe60-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbe60-139">RELATED LINKS</span></span>

[<span data-ttu-id="dbe60-140">Add-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe60-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="dbe60-141">Get-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe60-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="dbe60-142">Remove-Az VpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="dbe60-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


