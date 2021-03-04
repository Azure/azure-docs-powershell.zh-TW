---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 818C2250-DE43-409E-AC68-B4A7E945401E
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: d7665d490979ca15189650572c083a94efb6c123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915342"
---
# <span data-ttu-id="00f77-101">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="00f77-101">Remove-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="00f77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="00f77-102">SYNOPSIS</span></span>
<span data-ttu-id="00f77-103">移除 VPN 用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="00f77-103">Removes a VPN client-revocation certificate.</span></span>

## <span data-ttu-id="00f77-104">語法</span><span class="sxs-lookup"><span data-stu-id="00f77-104">SYNTAX</span></span>

```
Remove-AzVpnClientRevokedCertificate -VpnClientRevokedCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00f77-105">描述</span><span class="sxs-lookup"><span data-stu-id="00f77-105">DESCRIPTION</span></span>
<span data-ttu-id="00f77-106">**Remove-Az VpnClientRevokedCertificate Cmdlet** 會從虛擬網路閘道移除用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="00f77-106">The **Remove-AzVpnClientRevokedCertificate** cmdlet removes a client-revocation certificate from a virtual network gateway.</span></span>
<span data-ttu-id="00f77-107">用戶端吊銷憑證可防止用戶端電腦使用指定的憑證進行驗證。</span><span class="sxs-lookup"><span data-stu-id="00f77-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>
<span data-ttu-id="00f77-108">如果您移除用戶端吊銷憑證，用戶端電腦就可以使用先前禁止的憑證，讓虛擬私人網路 (VPN) 連接。</span><span class="sxs-lookup"><span data-stu-id="00f77-108">If you remove a client-revocation certificate client computers can then use the previously-banned certificate to make a virtual private network (VPN) connection.</span></span>

## <span data-ttu-id="00f77-109">例子</span><span class="sxs-lookup"><span data-stu-id="00f77-109">EXAMPLES</span></span>

### <span data-ttu-id="00f77-110">範例 1：從虛擬網路閘道移除用戶端吊銷憑證</span><span class="sxs-lookup"><span data-stu-id="00f77-110">Example 1: Remove a client-revocation certificate from a virtual network gateway</span></span>
```powershell
PS C:\>Remove-AzVpnClientRevokedCertificate -VirtualNetworkGatewayName "ContosoVirtualNetwork" -ResourceGroupName"ContosoResourceGroup" -VpnClientRevokedCertificateName "ContosoRevokedClientCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="00f77-111">此命令會從名為 ContosoVirtualNetwork 的虛擬網路閘道移除用戶端吊銷憑證。</span><span class="sxs-lookup"><span data-stu-id="00f77-111">This command removes a client-revocation certificate from a virtual network gateway named ContosoVirtualNetwork.</span></span>
<span data-ttu-id="00f77-112">若要移除用戶端吊銷憑證，您必須同時指定憑證名稱和憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="00f77-112">In order to remove a client-revocation certificate, you must specify both the certificate name and the certificate thumbprint.</span></span>

## <span data-ttu-id="00f77-113">參數</span><span class="sxs-lookup"><span data-stu-id="00f77-113">PARAMETERS</span></span>

### <span data-ttu-id="00f77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f77-114">-DefaultProfile</span></span>
<span data-ttu-id="00f77-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="00f77-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00f77-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f77-116">-ResourceGroupName</span></span>
<span data-ttu-id="00f77-117">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="00f77-117">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="00f77-118">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="00f77-118">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="00f77-119">-拇指列印</span><span class="sxs-lookup"><span data-stu-id="00f77-119">-Thumbprint</span></span>
<span data-ttu-id="00f77-120">指定要移除之憑證的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="00f77-120">Specifies the unique identifier of the certificate being removed.</span></span>
<span data-ttu-id="00f77-121">您可以使用類似以下的 Windows PowerShell 命令，針對憑證返回指紋資訊： `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span><span class="sxs-lookup"><span data-stu-id="00f77-121">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this: `Get-ChildItem -Path "Cert:\LocalMachine\Root"`</span></span>
<span data-ttu-id="00f77-122">上一個命令會針對根憑證存放區中找到的所有 Local Computer 憑證，會返回資訊。</span><span class="sxs-lookup"><span data-stu-id="00f77-122">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="00f77-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="00f77-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="00f77-124">指定憑證指派給的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="00f77-124">Specifies the name of the virtual network gateway that the certificate is assigned to.</span></span>

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

### <span data-ttu-id="00f77-125">-VpnClientRevokedCertificateName</span><span class="sxs-lookup"><span data-stu-id="00f77-125">-VpnClientRevokedCertificateName</span></span>
<span data-ttu-id="00f77-126">指定要移除的 VPN 用戶端憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="00f77-126">Specifies the name of the VPN client certificate being removed.</span></span>

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

### <span data-ttu-id="00f77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f77-127">CommonParameters</span></span>
<span data-ttu-id="00f77-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="00f77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f77-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="00f77-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f77-130">輸入</span><span class="sxs-lookup"><span data-stu-id="00f77-130">INPUTS</span></span>

### <span data-ttu-id="00f77-131">System.String</span><span class="sxs-lookup"><span data-stu-id="00f77-131">System.String</span></span>

## <span data-ttu-id="00f77-132">輸出</span><span class="sxs-lookup"><span data-stu-id="00f77-132">OUTPUTS</span></span>

### <span data-ttu-id="00f77-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00f77-133">System.Boolean</span></span>

## <span data-ttu-id="00f77-134">筆記</span><span class="sxs-lookup"><span data-stu-id="00f77-134">NOTES</span></span>

## <span data-ttu-id="00f77-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="00f77-135">RELATED LINKS</span></span>

[<span data-ttu-id="00f77-136">Add-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="00f77-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="00f77-137">Get-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="00f77-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="00f77-138">New-Az VpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="00f77-138">New-AzVpnClientRevokedCertificate</span></span>](./New-AzVpnClientRevokedCertificate.md)


