---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: c73f65866b2a23527540319744854e50f6639268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625137"
---
# <span data-ttu-id="ac041-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ac041-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ac041-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac041-102">SYNOPSIS</span></span>
<span data-ttu-id="ac041-103">新增 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="ac041-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac041-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac041-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac041-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac041-105">DESCRIPTION</span></span>
<span data-ttu-id="ac041-106">**AzureRmVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證指派給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="ac041-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="ac041-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="ac041-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="ac041-108">您必須指定憑證名稱和憑證指紋，才能使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac041-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="ac041-109">示例</span><span class="sxs-lookup"><span data-stu-id="ac041-109">EXAMPLES</span></span>

### <span data-ttu-id="ac041-110">範例1：將新的用戶端吊銷憑證新增至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="ac041-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="ac041-111">這個命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="ac041-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="ac041-112">若要新增憑證，您必須指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="ac041-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="ac041-113">參數</span><span class="sxs-lookup"><span data-stu-id="ac041-113">PARAMETERS</span></span>

### <span data-ttu-id="ac041-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac041-114">-ResourceGroupName</span></span>
<span data-ttu-id="ac041-115">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac041-115">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="ac041-116">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="ac041-116">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="ac041-117">-指紋</span><span class="sxs-lookup"><span data-stu-id="ac041-117">-Thumbprint</span></span>
<span data-ttu-id="ac041-118">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac041-118">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="ac041-119">例如：</span><span class="sxs-lookup"><span data-stu-id="ac041-119">For example:</span></span>

<span data-ttu-id="ac041-120">-指紋 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="ac041-120">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="ac041-121">您可以使用類似以下的 Windows PowerShell 命令來取得憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root` 。</span><span class="sxs-lookup"><span data-stu-id="ac041-121">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="ac041-122">上述命令會取得在根憑證存放區中找到之所有本機電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="ac041-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="ac041-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="ac041-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="ac041-124">指定要新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="ac041-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="ac041-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="ac041-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="ac041-126">指定要新增之 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac041-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="ac041-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac041-127">-DefaultProfile</span></span>
<span data-ttu-id="ac041-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac041-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac041-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac041-129">CommonParameters</span></span>
<span data-ttu-id="ac041-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac041-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac041-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac041-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac041-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ac041-132">INPUTS</span></span>

## <span data-ttu-id="ac041-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ac041-133">OUTPUTS</span></span>

### <span data-ttu-id="ac041-134">PSVpnClientRevokedCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ac041-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="ac041-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ac041-135">NOTES</span></span>

## <span data-ttu-id="ac041-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac041-136">RELATED LINKS</span></span>

[<span data-ttu-id="ac041-137">AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ac041-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="ac041-138">新-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ac041-138">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="ac041-139">移除-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="ac041-139">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


