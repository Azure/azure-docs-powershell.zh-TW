---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: c0f7d2692472316d018d4a11b6843264c8666fe2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966315"
---
# <span data-ttu-id="db4f2-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db4f2-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="db4f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="db4f2-103">取得網路介面的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="db4f2-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="db4f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="db4f2-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="db4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="db4f2-106">**AzEffectiveNetworkSecurityGroup** Cmdlet 會傳回在網路介面上套用的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="db4f2-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="db4f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="db4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="db4f2-108">範例1：在網路介面上取得有效的網路安全群組</span><span class="sxs-lookup"><span data-stu-id="db4f2-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="db4f2-109">這個命令會取得與名為 myResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的所有有效網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="db4f2-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="db4f2-110">參數</span><span class="sxs-lookup"><span data-stu-id="db4f2-110">PARAMETERS</span></span>

### <span data-ttu-id="db4f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4f2-111">-DefaultProfile</span></span>
<span data-ttu-id="db4f2-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db4f2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4f2-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="db4f2-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="db4f2-114">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="db4f2-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="db4f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="db4f2-116">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="db4f2-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="db4f2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4f2-117">CommonParameters</span></span>
<span data-ttu-id="db4f2-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db4f2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4f2-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db4f2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4f2-120">輸入</span><span class="sxs-lookup"><span data-stu-id="db4f2-120">INPUTS</span></span>

### <span data-ttu-id="db4f2-121">System.object</span><span class="sxs-lookup"><span data-stu-id="db4f2-121">System.String</span></span>

## <span data-ttu-id="db4f2-122">輸出</span><span class="sxs-lookup"><span data-stu-id="db4f2-122">OUTPUTS</span></span>

### <span data-ttu-id="db4f2-123">PSEffectiveNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="db4f2-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="db4f2-124">筆記</span><span class="sxs-lookup"><span data-stu-id="db4f2-124">NOTES</span></span>

## <span data-ttu-id="db4f2-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="db4f2-125">RELATED LINKS</span></span>

[<span data-ttu-id="db4f2-126">AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="db4f2-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


