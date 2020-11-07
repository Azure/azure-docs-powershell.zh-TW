---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: d08f91029940d60440d50be406dbdfe3652934a7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794340"
---
# <span data-ttu-id="8e739-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="8e739-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="8e739-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8e739-102">SYNOPSIS</span></span>
<span data-ttu-id="8e739-103">取得 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e739-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="8e739-104">句法</span><span class="sxs-lookup"><span data-stu-id="8e739-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e739-105">說明</span><span class="sxs-lookup"><span data-stu-id="8e739-105">DESCRIPTION</span></span>
<span data-ttu-id="8e739-106">**AzVpnClientPackage** Cmdlet 會取得虛擬網路閘道提供之 VPN 用戶端套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8e739-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="8e739-107">用戶端套件包含可讓用戶端電腦建立 Azure 虛擬網路 VPN 連線的配置資料;用戶端電腦必須安裝正確的 configuration 套件，才能進行 VPN 連線。</span><span class="sxs-lookup"><span data-stu-id="8e739-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="8e739-108">根據用戶端電腦的 Windows 版本，您可以使用不同的配置套件 (例如，Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 。</span><span class="sxs-lookup"><span data-stu-id="8e739-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="8e739-109">在執行 **AzVpnClientPackage** 時，您必須指定架構類型。</span><span class="sxs-lookup"><span data-stu-id="8e739-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="8e739-110">示例</span><span class="sxs-lookup"><span data-stu-id="8e739-110">EXAMPLES</span></span>

### <span data-ttu-id="8e739-111">範例1：取得處理器架構 VPN 用戶端套件的相關資訊</span><span class="sxs-lookup"><span data-stu-id="8e739-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="8e739-112">這個命令會取得 AMD64 VPN 用戶端套件的相關資訊，這些元件儲存在名為 ContosoVirtualNetworkGateway 的虛擬網路閘道。</span><span class="sxs-lookup"><span data-stu-id="8e739-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="8e739-113">若要取得 x86 用戶端套件的相關資訊，請將 *ProcessorArchitecture* 參數的值設定為 x86。</span><span class="sxs-lookup"><span data-stu-id="8e739-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="8e739-114">參數</span><span class="sxs-lookup"><span data-stu-id="8e739-114">PARAMETERS</span></span>

### <span data-ttu-id="8e739-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e739-115">-DefaultProfile</span></span>
<span data-ttu-id="8e739-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8e739-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e739-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8e739-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="8e739-118">指定用戶端套件所設計的 CPU 架構類型。</span><span class="sxs-lookup"><span data-stu-id="8e739-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="8e739-119">有效值為 Amd64 和 X86。</span><span class="sxs-lookup"><span data-stu-id="8e739-119">Valid values are Amd64 and X86.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Amd64, X86

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e739-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e739-120">-ResourceGroupName</span></span>
<span data-ttu-id="8e739-121">指定指派虛擬網路閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e739-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="8e739-122">資源群組會將專案分類，以協助簡化庫存管理和一般 Azure 管理。</span><span class="sxs-lookup"><span data-stu-id="8e739-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e739-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="8e739-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="8e739-124">指定儲存用戶端套件資訊之虛擬網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e739-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e739-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e739-125">CommonParameters</span></span>
<span data-ttu-id="8e739-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8e739-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e739-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8e739-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e739-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8e739-128">INPUTS</span></span>

### <span data-ttu-id="8e739-129">字串</span><span class="sxs-lookup"><span data-stu-id="8e739-129">String</span></span>
<span data-ttu-id="8e739-130">"ResourceGroupName" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="8e739-130">Parameter 'ResourceGroupName' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="8e739-131">字串</span><span class="sxs-lookup"><span data-stu-id="8e739-131">String</span></span>
<span data-ttu-id="8e739-132">"VirtualNetworkGatewayName" 參數從管線接受類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="8e739-132">Parameter 'VirtualNetworkGatewayName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="8e739-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8e739-133">OUTPUTS</span></span>

###  
<span data-ttu-id="8e739-134">**AzVpnClientPackage** 會傳回 system.object 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="8e739-134">**Get-AzVpnClientPackage** returns instances of the System.String object.</span></span>

## <span data-ttu-id="8e739-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8e739-135">NOTES</span></span>

## <span data-ttu-id="8e739-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e739-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e739-137">調整大小-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8e739-137">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="8e739-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="8e739-138">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>](./Set-AzVirtualNetworkGatewayVpnClientConfig.md)


