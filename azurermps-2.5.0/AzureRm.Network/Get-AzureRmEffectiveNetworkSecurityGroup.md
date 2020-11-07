---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectivenetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 214ab7f91791fa05453e2f4ef4238440d9c78a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800470"
---
# <span data-ttu-id="07eb4-101">Get-AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="07eb4-101">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="07eb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="07eb4-103">取得網路介面的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="07eb4-103">Gets the effective network security group of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07eb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="07eb4-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07eb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="07eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="07eb4-106">**AzureRmEffectiveNetworkSecurityGroup** Cmdlet 會傳回在網路介面上套用的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="07eb4-106">The **Get-AzureRmEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="07eb4-107">示例</span><span class="sxs-lookup"><span data-stu-id="07eb4-107">EXAMPLES</span></span>

### <span data-ttu-id="07eb4-108">範例1：在網路介面上取得有效的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="07eb4-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="07eb4-109">這個命令會取得與名為 myResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的所有有效網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="07eb4-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="07eb4-110">參數</span><span class="sxs-lookup"><span data-stu-id="07eb4-110">PARAMETERS</span></span>

### <span data-ttu-id="07eb4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07eb4-111">-DefaultProfile</span></span>
<span data-ttu-id="07eb4-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="07eb4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07eb4-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="07eb4-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="07eb4-114">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="07eb4-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="07eb4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07eb4-115">-ResourceGroupName</span></span>
<span data-ttu-id="07eb4-116">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="07eb4-116">Specifies the resource group of a network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07eb4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07eb4-117">CommonParameters</span></span>
<span data-ttu-id="07eb4-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07eb4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07eb4-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07eb4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07eb4-120">輸入</span><span class="sxs-lookup"><span data-stu-id="07eb4-120">INPUTS</span></span>

## <span data-ttu-id="07eb4-121">輸出</span><span class="sxs-lookup"><span data-stu-id="07eb4-121">OUTPUTS</span></span>

### <span data-ttu-id="07eb4-122">PSEffectiveNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="07eb4-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="07eb4-123">筆記</span><span class="sxs-lookup"><span data-stu-id="07eb4-123">NOTES</span></span>

## <span data-ttu-id="07eb4-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="07eb4-124">RELATED LINKS</span></span>

[<span data-ttu-id="07eb4-125">AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="07eb4-125">Get-AzureRmEffectiveRouteTable</span></span>](./Get-AzureRmEffectiveRouteTable.md)


