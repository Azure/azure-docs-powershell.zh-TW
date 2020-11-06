---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 565d0748104e537f448a40116a48f0cd34ebf16b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446950"
---
# <span data-ttu-id="f7169-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f7169-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f7169-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7169-102">SYNOPSIS</span></span>
<span data-ttu-id="f7169-103">取得網路介面的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="f7169-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7169-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7169-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7169-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7169-105">DESCRIPTION</span></span>
<span data-ttu-id="f7169-106">**AzureRmEffectiveNetworkSecurityGroup** Cmdlet 會傳回在網路介面上套用的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="f7169-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="f7169-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7169-107">EXAMPLES</span></span>

### <span data-ttu-id="f7169-108">範例1：在網路介面上取得有效的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="f7169-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="f7169-109">這個命令會取得與名為 myResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的所有有效網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="f7169-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="f7169-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7169-110">PARAMETERS</span></span>

### <span data-ttu-id="f7169-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7169-111">-DefaultProfile</span></span>
<span data-ttu-id="f7169-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7169-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7169-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f7169-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="f7169-114">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7169-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="f7169-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7169-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7169-116">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f7169-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7169-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7169-117">CommonParameters</span></span>
<span data-ttu-id="f7169-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7169-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7169-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7169-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7169-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f7169-120">INPUTS</span></span>

### <span data-ttu-id="f7169-121">System.object</span><span class="sxs-lookup"><span data-stu-id="f7169-121">System.String</span></span>

## <span data-ttu-id="f7169-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f7169-122">OUTPUTS</span></span>

### <span data-ttu-id="f7169-123">PSEffectiveNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7169-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="f7169-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f7169-124">NOTES</span></span>

## <span data-ttu-id="f7169-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7169-125">RELATED LINKS</span></span>

[<span data-ttu-id="f7169-126">AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f7169-126">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


