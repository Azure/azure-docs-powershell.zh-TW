---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 90FB7B88-844E-4783-A10F-04D7BA47C030
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: b952033bc6f04f2ed1e6d2e257dc68da1a6ec6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908845"
---
# <span data-ttu-id="72190-101">Add-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="72190-101">Add-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="72190-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72190-102">SYNOPSIS</span></span>
<span data-ttu-id="72190-103">新增 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="72190-103">Adds a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="72190-104">語法</span><span class="sxs-lookup"><span data-stu-id="72190-104">SYNTAX</span></span>

```
Add-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72190-105">描述</span><span class="sxs-lookup"><span data-stu-id="72190-105">DESCRIPTION</span></span>
<span data-ttu-id="72190-106">**Add-Az VpnClientRevokedCertificate** Cmdlet 會指派用戶端吊銷憑證給虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="72190-106">The **Add-AzVpnClientRevokedCertificate** cmdlet assigns a client-revocation certificate to a virtual network gateway.</span></span>
<span data-ttu-id="72190-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="72190-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="72190-108">您必須同時指定憑證名稱和憑證指紋，以使用此 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72190-108">You need to specify both the certificate name and the certificate thumbprint to use this cmdlet.</span></span>

## <span data-ttu-id="72190-109">例子</span><span class="sxs-lookup"><span data-stu-id="72190-109">EXAMPLES</span></span>

### <span data-ttu-id="72190-110">範例 1：新增用戶端吊銷憑證至虛擬網路閘道</span><span class="sxs-lookup"><span data-stu-id="72190-110">Example 1: Add a new client-revocation certificate to a virtual network gateway</span></span>
```powershell
PS C:\>Add-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName "ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="72190-111">此命令會將新的用戶端吊銷憑證新增到名為 ContosoVirtualNetwork 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="72190-111">This command adds a new client-revocation certificate to the virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="72190-112">若要新增憑證，您必須同時指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="72190-112">In order to add the certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="72190-113">參數</span><span class="sxs-lookup"><span data-stu-id="72190-113">PARAMETERS</span></span>

### <span data-ttu-id="72190-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72190-114">-DefaultProfile</span></span>
<span data-ttu-id="72190-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72190-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72190-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72190-116">-ResourceGroupName</span></span>
<span data-ttu-id="72190-117">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="72190-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="72190-118">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="72190-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="72190-119">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="72190-119">-Thumbprint</span></span>
<span data-ttu-id="72190-120">指定要新增之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="72190-120">Specifies the unique identifier of the certificate being added.</span></span>
<span data-ttu-id="72190-121">例如：-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" 您可以使用類似以下的 Windows PowerShell 命令取得憑證的指紋 `Get-ChildItem -Path Cert:\LocalMachine\Root` 資訊。</span><span class="sxs-lookup"><span data-stu-id="72190-121">For example: -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" You can get thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path Cert:\LocalMachine\Root`.</span></span>
<span data-ttu-id="72190-122">上述命令會獲得根憑證存放區中所有找到之本地電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="72190-122">The preceding command gets information for all the local computer certificates found in the root certificate store.</span></span>

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

### <span data-ttu-id="72190-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="72190-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="72190-124">指定應新增憑證的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="72190-124">Specifies the name of the virtual network gateway where the certificate should be added.</span></span>

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

### <span data-ttu-id="72190-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="72190-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="72190-126">指定要新增的 VPN 用戶端憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="72190-126">Specifies the name of the VPN client certificate to be added.</span></span>

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

### <span data-ttu-id="72190-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72190-127">CommonParameters</span></span>
<span data-ttu-id="72190-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72190-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72190-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="72190-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72190-130">輸入</span><span class="sxs-lookup"><span data-stu-id="72190-130">INPUTS</span></span>

### <span data-ttu-id="72190-131">System.String</span><span class="sxs-lookup"><span data-stu-id="72190-131">System.String</span></span>

## <span data-ttu-id="72190-132">輸出</span><span class="sxs-lookup"><span data-stu-id="72190-132">OUTPUTS</span></span>

### <span data-ttu-id="72190-133">Microsoft.Azure.Commands.Network.models.PS VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="72190-133">Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="72190-134">筆記</span><span class="sxs-lookup"><span data-stu-id="72190-134">NOTES</span></span>

## <span data-ttu-id="72190-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="72190-135">RELATED LINKS</span></span>

[<span data-ttu-id="72190-136">Get-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="72190-136">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="72190-137">New-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="72190-137">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="72190-138">Remove-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="72190-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


