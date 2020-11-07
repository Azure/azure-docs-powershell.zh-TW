---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8f1c81dbfb3d8c42b359464ce33a0053fdc25143
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625886"
---
# <span data-ttu-id="893bf-101">Add-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="893bf-101">Add-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="893bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="893bf-102">SYNOPSIS</span></span>
<span data-ttu-id="893bf-103">新增 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="893bf-103">Adds a VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="893bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="893bf-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="893bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="893bf-105">DESCRIPTION</span></span>
<span data-ttu-id="893bf-106">**AzureRmVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證指派給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="893bf-106">The **Add-AzureRmVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="893bf-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="893bf-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="893bf-108">您必須指定憑證名稱和憑證指紋，才能使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="893bf-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="893bf-109">示例</span><span class="sxs-lookup"><span data-stu-id="893bf-109">EXAMPLES</span></span>

### <span data-ttu-id="893bf-110">範例1：將新的用戶端吊銷憑證新增至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="893bf-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```
PS C:\>Add-AzureRmVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="893bf-111">這個命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="893bf-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="893bf-112">若要新增憑證，您必須指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="893bf-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="893bf-113">參數</span><span class="sxs-lookup"><span data-stu-id="893bf-113">PARAMETERS</span></span>

### <span data-ttu-id="893bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893bf-114">-DefaultProfile</span></span>
<span data-ttu-id="893bf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="893bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893bf-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893bf-116">-ResourceGroupName</span></span>
<span data-ttu-id="893bf-117">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="893bf-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="893bf-118">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="893bf-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="893bf-119">-指紋</span><span class="sxs-lookup"><span data-stu-id="893bf-119">-Thumbprint</span></span>
<span data-ttu-id="893bf-120">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="893bf-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="893bf-121">例如：</span><span class="sxs-lookup"><span data-stu-id="893bf-121">For example:</span></span>

<span data-ttu-id="893bf-122">-指紋 "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span><span class="sxs-lookup"><span data-stu-id="893bf-122">-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"</span></span>

<span data-ttu-id="893bf-123">您可以使用類似以下的 Windows PowerShell 命令來取得憑證的指紋資訊： `Get-ChildItem -Path Cert:\LocalMachine\Root` 。</span><span class="sxs-lookup"><span data-stu-id="893bf-123">You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>

<span data-ttu-id="893bf-124">上述命令會取得在根憑證存放區中找到之所有本機電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="893bf-124">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="893bf-125">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="893bf-125">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="893bf-126">指定要新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="893bf-126">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="893bf-127">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="893bf-127">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="893bf-128">指定要新增之 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="893bf-128">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="893bf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893bf-129">CommonParameters</span></span>
<span data-ttu-id="893bf-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="893bf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893bf-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="893bf-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893bf-132">輸入</span><span class="sxs-lookup"><span data-stu-id="893bf-132">INPUTS</span></span>

### <span data-ttu-id="893bf-133">所有</span><span class="sxs-lookup"><span data-stu-id="893bf-133">None</span></span>
<span data-ttu-id="893bf-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="893bf-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="893bf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="893bf-135">OUTPUTS</span></span>

### <span data-ttu-id="893bf-136">PSVpnClientRevokedCertificate 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="893bf-136">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="893bf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="893bf-137">NOTES</span></span>

## <span data-ttu-id="893bf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="893bf-138">RELATED LINKS</span></span>

[<span data-ttu-id="893bf-139">AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="893bf-139">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="893bf-140">新-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="893bf-140">New-AzureRmVpnClientRevokedCertificate</span></span>](./New-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="893bf-141">移除-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="893bf-141">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)


