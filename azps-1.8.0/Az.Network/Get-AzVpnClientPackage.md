---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: eb88be102f390d9e94ba938eeb6d116af6a79fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621896"
---
# <span data-ttu-id="337a9-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="337a9-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="337a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="337a9-102">SYNOPSIS</span></span>
<span data-ttu-id="337a9-103">取得 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="337a9-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="337a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="337a9-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="337a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="337a9-105">DESCRIPTION</span></span>
<span data-ttu-id="337a9-106">**AzVpnClientPackage** Cmdlet 會取得虛擬網路閘道提供之 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="337a9-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="337a9-107">用戶端套件包含可讓用戶端電腦建立 Azure 虛擬網路 VPN 連線的配置資料;用戶端電腦必須安裝正確的 configuration 套件，才能進行 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="337a9-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="337a9-108">根據用戶端電腦的 Windows 版本，您可以使用不同的配置套件 (例如，Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 。</span><span class="sxs-lookup"><span data-stu-id="337a9-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="337a9-109">在執行 **AzVpnClientPackage** 時，您必須指定架構類型。</span><span class="sxs-lookup"><span data-stu-id="337a9-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="337a9-110">示例</span><span class="sxs-lookup"><span data-stu-id="337a9-110">EXAMPLES</span></span>

### <span data-ttu-id="337a9-111">範例1：取得處理器架構 VPN 用戶端套件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="337a9-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="337a9-112">這個命令會取得 AMD64 VPN 用戶端套件的相關資訊，這些元件儲存在名為 ContosoVirtualNetworkGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="337a9-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="337a9-113">若要取得 x86 用戶端套件的相關資訊，請將 *ProcessorArchitecture* 參數的值設定為 x86。</span><span class="sxs-lookup"><span data-stu-id="337a9-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="337a9-114">參數</span><span class="sxs-lookup"><span data-stu-id="337a9-114">PARAMETERS</span></span>

### <span data-ttu-id="337a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337a9-115">-DefaultProfile</span></span>
<span data-ttu-id="337a9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="337a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="337a9-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="337a9-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="337a9-118">指定用戶端套件所設計的 CPU 架構類型。</span><span class="sxs-lookup"><span data-stu-id="337a9-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="337a9-119">有效值為 Amd64 和 X86。</span><span class="sxs-lookup"><span data-stu-id="337a9-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="337a9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337a9-120">-ResourceGroupName</span></span>
<span data-ttu-id="337a9-121">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="337a9-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="337a9-122">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="337a9-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="337a9-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="337a9-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="337a9-124">指定儲存用戶端套件資訊之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="337a9-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="337a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337a9-125">CommonParameters</span></span>
<span data-ttu-id="337a9-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="337a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337a9-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="337a9-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337a9-128">輸入</span><span class="sxs-lookup"><span data-stu-id="337a9-128">INPUTS</span></span>

### <span data-ttu-id="337a9-129">System.object</span><span class="sxs-lookup"><span data-stu-id="337a9-129">System.String</span></span>

## <span data-ttu-id="337a9-130">輸出</span><span class="sxs-lookup"><span data-stu-id="337a9-130">OUTPUTS</span></span>

### <span data-ttu-id="337a9-131">System.object</span><span class="sxs-lookup"><span data-stu-id="337a9-131">System.String</span></span>

## <span data-ttu-id="337a9-132">筆記</span><span class="sxs-lookup"><span data-stu-id="337a9-132">NOTES</span></span>

## <span data-ttu-id="337a9-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="337a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="337a9-134">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="337a9-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="337a9-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="337a9-135">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


