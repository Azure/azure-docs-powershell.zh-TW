---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientPackage.md
ms.openlocfilehash: fc94bb7de5663995e75f0c4f1fed05fb36b35f40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448370"
---
# <span data-ttu-id="f3e33-101">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f3e33-101">Get-AzureRmVpnClientPackage</span></span>

## <span data-ttu-id="f3e33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f3e33-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e33-103">取得 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3e33-103">Gets information about a VPN client package.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3e33-104">句法</span><span class="sxs-lookup"><span data-stu-id="f3e33-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3e33-105">說明</span><span class="sxs-lookup"><span data-stu-id="f3e33-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e33-106">**AzureRmVpnClientPackage** Cmdlet 會取得虛擬網路閘道提供之 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f3e33-106">The **Get-AzureRmVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="f3e33-107">用戶端套件包含可讓用戶端電腦建立 Azure 虛擬網路 VPN 連線的配置資料;用戶端電腦必須安裝正確的 configuration 套件，才能進行 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="f3e33-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="f3e33-108">根據用戶端電腦的 Windows 版本，您可以使用不同的配置套件 (例如，Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 。</span><span class="sxs-lookup"><span data-stu-id="f3e33-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="f3e33-109">在執行 **AzureRmVpnClientPackage** 時，您必須指定架構類型。</span><span class="sxs-lookup"><span data-stu-id="f3e33-109">You must specify the architecture type when running **Get-AzureRmVpnClientPackage**.</span></span>

## <span data-ttu-id="f3e33-110">示例</span><span class="sxs-lookup"><span data-stu-id="f3e33-110">EXAMPLES</span></span>

### <span data-ttu-id="f3e33-111">範例1：取得處理器架構 VPN 用戶端套件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="f3e33-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzureRmVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="f3e33-112">這個命令會取得 AMD64 VPN 用戶端套件的相關資訊，這些元件儲存在名為 ContosoVirtualNetworkGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="f3e33-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="f3e33-113">若要取得 x86 用戶端套件的相關資訊，請將 *ProcessorArchitecture* 參數的值設定為 x86。</span><span class="sxs-lookup"><span data-stu-id="f3e33-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="f3e33-114">參數</span><span class="sxs-lookup"><span data-stu-id="f3e33-114">PARAMETERS</span></span>

### <span data-ttu-id="f3e33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e33-115">-DefaultProfile</span></span>
<span data-ttu-id="f3e33-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3e33-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e33-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="f3e33-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="f3e33-118">指定用戶端套件所設計的 CPU 架構類型。</span><span class="sxs-lookup"><span data-stu-id="f3e33-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="f3e33-119">有效值為 Amd64 和 X86。</span><span class="sxs-lookup"><span data-stu-id="f3e33-119">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="f3e33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3e33-120">-ResourceGroupName</span></span>
<span data-ttu-id="f3e33-121">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e33-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="f3e33-122">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="f3e33-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="f3e33-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="f3e33-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="f3e33-124">指定儲存用戶端套件資訊之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3e33-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="f3e33-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e33-125">CommonParameters</span></span>
<span data-ttu-id="f3e33-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f3e33-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e33-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f3e33-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e33-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f3e33-128">INPUTS</span></span>

### <span data-ttu-id="f3e33-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f3e33-129">System.String</span></span>
<span data-ttu-id="f3e33-130">參數： ResourceGroupName (ByValue) ，VirtualNetworkGatewayName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="f3e33-130">Parameters: ResourceGroupName (ByValue), VirtualNetworkGatewayName (ByValue)</span></span>

## <span data-ttu-id="f3e33-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f3e33-131">OUTPUTS</span></span>

### <span data-ttu-id="f3e33-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f3e33-132">System.String</span></span>

## <span data-ttu-id="f3e33-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f3e33-133">NOTES</span></span>

## <span data-ttu-id="f3e33-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3e33-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3e33-135">調整大小-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f3e33-135">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f3e33-136">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="f3e33-136">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md)


