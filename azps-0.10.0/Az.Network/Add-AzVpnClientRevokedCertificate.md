---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 384d5b88ce9a52ad5f68c009c7b610610c695ce2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794487"
---
# <span data-ttu-id="9aab8-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9aab8-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9aab8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9aab8-102">SYNOPSIS</span></span>
<span data-ttu-id="9aab8-103">新增 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="9aab8-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="9aab8-104">句法</span><span class="sxs-lookup"><span data-stu-id="9aab8-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aab8-105">說明</span><span class="sxs-lookup"><span data-stu-id="9aab8-105">DESCRIPTION</span></span>
<span data-ttu-id="9aab8-106">**AzVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證指派給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9aab8-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="9aab8-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="9aab8-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="9aab8-108">您必須指定憑證名稱和憑證指紋，才能使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9aab8-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="9aab8-109">示例</span><span class="sxs-lookup"><span data-stu-id="9aab8-109">EXAMPLES</span></span>

### <span data-ttu-id="9aab8-110">範例1：將新的用戶端吊銷憑證新增至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="9aab8-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="9aab8-111">這個命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="9aab8-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="9aab8-112">若要新增憑證，您必須指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="9aab8-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="9aab8-113">參數</span><span class="sxs-lookup"><span data-stu-id="9aab8-113">PARAMETERS</span></span>

### <span data-ttu-id="9aab8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aab8-114">-DefaultProfile</span></span>
<span data-ttu-id="9aab8-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9aab8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aab8-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aab8-116">-ResourceGroupName</span></span>
<span data-ttu-id="9aab8-117">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aab8-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="9aab8-118">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="9aab8-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="9aab8-119">-指紋</span><span class="sxs-lookup"><span data-stu-id="9aab8-119">-Thumbprint</span></span>
<span data-ttu-id="9aab8-120">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="9aab8-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="9aab8-121">例如：</span><span class="sxs-lookup"><span data-stu-id="9aab8-121">For example:</span></span>

<span data-ttu-id="9aab8-122">-指紋 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="9aab8-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="9aab8-123">您可以使用類似以下的 Windows PowerShell 命令來取得憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root` 。</span><span class="sxs-lookup"><span data-stu-id="9aab8-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="9aab8-124">上述命令會取得在根憑證存放區中找到之所有本機電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="9aab8-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="9aab8-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="9aab8-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="9aab8-126">指定要新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="9aab8-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="9aab8-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="9aab8-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="9aab8-128">指定要新增之 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="9aab8-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="9aab8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aab8-129">CommonParameters</span></span>
<span data-ttu-id="9aab8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9aab8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aab8-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9aab8-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aab8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9aab8-132">INPUTS</span></span>

## <span data-ttu-id="9aab8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9aab8-133">OUTPUTS</span></span>

### <span data-ttu-id="9aab8-134">PSVpnClientRevokedCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="9aab8-134">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="9aab8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9aab8-135">NOTES</span></span>

## <span data-ttu-id="9aab8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9aab8-136">RELATED LINKS</span></span>

[<span data-ttu-id="9aab8-137">AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9aab8-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9aab8-138">新-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9aab8-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="9aab8-139">移除-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="9aab8-139">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


