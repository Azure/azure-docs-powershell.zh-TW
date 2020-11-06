---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: 861ea7bcfbfbe8a713934e2dc80a4448a2a98c48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621535"
---
# <span data-ttu-id="37010-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="37010-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="37010-102">摘要</span><span class="sxs-lookup"><span data-stu-id="37010-102">SYNOPSIS</span></span>
<span data-ttu-id="37010-103">移除 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="37010-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="37010-104">句法</span><span class="sxs-lookup"><span data-stu-id="37010-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37010-105">說明</span><span class="sxs-lookup"><span data-stu-id="37010-105">DESCRIPTION</span></span>
<span data-ttu-id="37010-106">**AzVpnClientRevokedCertificate** Cmdlet 會將用戶端吊銷憑證從虛擬網路閘道中移除。</span><span class="sxs-lookup"><span data-stu-id="37010-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="37010-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="37010-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="37010-108">如果您移除用戶端吊銷憑證用戶端電腦，就可以使用先前禁止的憑證，將虛擬私人網路 (VPN) 連線。</span><span class="sxs-lookup"><span data-stu-id="37010-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="37010-109">示例</span><span class="sxs-lookup"><span data-stu-id="37010-109">EXAMPLES</span></span>

### <span data-ttu-id="37010-110">範例1：從虛擬網路閘道移除用戶端吊銷憑證</span><span class="sxs-lookup"><span data-stu-id="37010-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate"-Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="37010-111">這個命令會從名為 ContosoVirtualNetwork 的虛擬網路閘道中移除用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="37010-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="37010-112">若要移除用戶端吊銷憑證，您必須指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="37010-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="37010-113">參數</span><span class="sxs-lookup"><span data-stu-id="37010-113">PARAMETERS</span></span>

### <span data-ttu-id="37010-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37010-114">-DefaultProfile</span></span>
<span data-ttu-id="37010-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="37010-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37010-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37010-116">-ResourceGroupName</span></span>
<span data-ttu-id="37010-117">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="37010-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="37010-118">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="37010-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="37010-119">-指紋</span><span class="sxs-lookup"><span data-stu-id="37010-119">-Thumbprint</span></span>
<span data-ttu-id="37010-120">指定要移除之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="37010-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="37010-121">您可以使用類似以下的 Windows PowerShell 命令，傳回憑證的指紋資訊： `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="37010-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="37010-122">上述命令會傳回在根憑證存放區中找到之所有本機電腦憑證的資訊。</span><span class="sxs-lookup"><span data-stu-id="37010-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="37010-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="37010-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="37010-124">指定指派憑證的虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="37010-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="37010-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="37010-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="37010-126">指定要移除之 VPN 用戶端憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="37010-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="37010-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37010-127">CommonParameters</span></span>
<span data-ttu-id="37010-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="37010-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37010-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="37010-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37010-130">輸入</span><span class="sxs-lookup"><span data-stu-id="37010-130">INPUTS</span></span>

### <span data-ttu-id="37010-131">System.object</span><span class="sxs-lookup"><span data-stu-id="37010-131">System.String</span></span>

## <span data-ttu-id="37010-132">輸出</span><span class="sxs-lookup"><span data-stu-id="37010-132">OUTPUTS</span></span>

### <span data-ttu-id="37010-133">System.object</span><span class="sxs-lookup"><span data-stu-id="37010-133">System.Boolean</span></span>

## <span data-ttu-id="37010-134">筆記</span><span class="sxs-lookup"><span data-stu-id="37010-134">NOTES</span></span>

## <span data-ttu-id="37010-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="37010-135">RELATED LINKS</span></span>

[<span data-ttu-id="37010-136">附加 AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="37010-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="37010-137">AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="37010-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="37010-138">新-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="37010-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


