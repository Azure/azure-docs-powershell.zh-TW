---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2B4A3E2A-1868-492F-9F77-932319D2CE6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientPackage.md
ms.openlocfilehash: ec91fecd41138238bc4d89fa81d77bae4730c770
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407602"
---
# <span data-ttu-id="bc699-101">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="bc699-101">Get-AzVpnClientPackage</span></span>

## <span data-ttu-id="bc699-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bc699-102">SYNOPSIS</span></span>
<span data-ttu-id="bc699-103">獲得 VPN 用戶端套件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc699-103">Gets information about a VPN client package.</span></span>

## <span data-ttu-id="bc699-104">語法</span><span class="sxs-lookup"><span data-stu-id="bc699-104">SYNTAX</span></span>

```
Get-AzVpnClientPackage -ResourceGroupName <String> -VirtualNetworkGatewayName <String>
 -ProcessorArchitecture <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc699-105">描述</span><span class="sxs-lookup"><span data-stu-id="bc699-105">DESCRIPTION</span></span>
<span data-ttu-id="bc699-106">**Get-Az VpnClientPackage Cmdlet** 會取得來自虛擬網路閘道的 VPN 用戶端套件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc699-106">The **Get-AzVpnClientPackage** cmdlet gets information about the VPN client packages available from a virtual network gateway.</span></span>
<span data-ttu-id="bc699-107">用戶端套件包含可讓用戶端電腦進行 Azure 虛擬網路的 VPN 連接之組配置資料;用戶端電腦必須安裝正確的組組套件，才能建立 VPN 連接。</span><span class="sxs-lookup"><span data-stu-id="bc699-107">Client packages contain configuration data that enable a client computer to make a VPN connection to an Azure virtual network; client computers must have the correct configuration package installed in order to make a VPN connection.</span></span>
<span data-ttu-id="bc699-108">根據用戶端電腦的 Windows (版本提供不同的組組套件，例如 Windows 7 或 Windows 10) ，以及用戶端電腦的處理器架構 (AMD64 或 x86) 。</span><span class="sxs-lookup"><span data-stu-id="bc699-108">Different configuration packages are available based on the client computer's version of Windows (for example, Windows 7 or Windows 10) and on the client computer's processor architecture (AMD64 or x86).</span></span>
<span data-ttu-id="bc699-109">您必須先指定架構類型，才能進行 **Get-Az VpnClientPackage。**</span><span class="sxs-lookup"><span data-stu-id="bc699-109">You must specify the architecture type when running **Get-AzVpnClientPackage**.</span></span>

## <span data-ttu-id="bc699-110">例子</span><span class="sxs-lookup"><span data-stu-id="bc699-110">EXAMPLES</span></span>

### <span data-ttu-id="bc699-111">範例 1：取得有關處理器架構 VPN 用戶端套件的資訊</span><span class="sxs-lookup"><span data-stu-id="bc699-111">Example 1: Get information about a processor architecture VPN client package</span></span>
```
PS C:\>Get-AzVpnClientPackage -ProcessorArchitecture -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -ProcessorArchitecture "Amd64"
```

<span data-ttu-id="bc699-112">此命令會獲得儲存在名為 ContosoVirtualNetworkGateway 之虛擬網路閘道上的 AMD64 VPN 用戶端套件相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bc699-112">This command gets information about the AMD64 VPN client packages stored on the virtual network gateway named ContosoVirtualNetworkGateway.</span></span>
<span data-ttu-id="bc699-113">若要取得 x86 用戶端套件相關資訊，請設定 *處理器Architecture* 參數的值為 x86。</span><span class="sxs-lookup"><span data-stu-id="bc699-113">To get information about the x86 client packages, set the value of the *ProcessorArchitecture* parameter to x86.</span></span>

## <span data-ttu-id="bc699-114">參數</span><span class="sxs-lookup"><span data-stu-id="bc699-114">PARAMETERS</span></span>

### <span data-ttu-id="bc699-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc699-115">-DefaultProfile</span></span>
<span data-ttu-id="bc699-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc699-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc699-117">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="bc699-117">-ProcessorArchitecture</span></span>
<span data-ttu-id="bc699-118">指定用戶端套件所設計的 CPU 架構類型。</span><span class="sxs-lookup"><span data-stu-id="bc699-118">Specifies the type of CPU architecture that the client package is designed for.</span></span>
<span data-ttu-id="bc699-119">有效的值為Amd64 和 X86。</span><span class="sxs-lookup"><span data-stu-id="bc699-119">Valid values are Amd64 and X86.</span></span>

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

### <span data-ttu-id="bc699-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc699-120">-ResourceGroupName</span></span>
<span data-ttu-id="bc699-121">指定指派給虛擬網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="bc699-121">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>
<span data-ttu-id="bc699-122">資源群組會分類專案，協助簡化庫存管理和一般 Azure 系統管理。</span><span class="sxs-lookup"><span data-stu-id="bc699-122">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="bc699-123">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="bc699-123">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="bc699-124">指定儲存用戶端套件資訊的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="bc699-124">Specifies the name of the virtual network gateway where the client package information is stored.</span></span>

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

### <span data-ttu-id="bc699-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc699-125">CommonParameters</span></span>
<span data-ttu-id="bc699-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bc699-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc699-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc699-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc699-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bc699-128">INPUTS</span></span>

### <span data-ttu-id="bc699-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bc699-129">System.String</span></span>

## <span data-ttu-id="bc699-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bc699-130">OUTPUTS</span></span>

### <span data-ttu-id="bc699-131">System.String</span><span class="sxs-lookup"><span data-stu-id="bc699-131">System.String</span></span>

## <span data-ttu-id="bc699-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bc699-132">NOTES</span></span>

## <span data-ttu-id="bc699-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc699-133">RELATED LINKS</span></span>

[<span data-ttu-id="bc699-134">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bc699-134">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)



