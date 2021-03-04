---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B9409AD6-F761-4B80-8E08-DBB2356F567D
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectivenetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveNetworkSecurityGroup.md
ms.openlocfilehash: 38f7d6780b598606d0a0938178309ed67e602315
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905902"
---
# <span data-ttu-id="a1430-101">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1430-101">Get-AzEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="a1430-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1430-102">SYNOPSIS</span></span>
<span data-ttu-id="a1430-103">獲得網路介面的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1430-103">Gets the effective network security group of a network interface.</span></span>

## <span data-ttu-id="a1430-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1430-104">SYNTAX</span></span>

```
Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1430-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1430-105">DESCRIPTION</span></span>
<span data-ttu-id="a1430-106">**Get-AzEffectiveNetworkSecurityGroup** Cmdlet 會返回網路介面上所適用的有效網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="a1430-106">The **Get-AzEffectiveNetworkSecurityGroup** cmdlet returns the effective network security group that is applied on a network interface.</span></span>

## <span data-ttu-id="a1430-107">例子</span><span class="sxs-lookup"><span data-stu-id="a1430-107">EXAMPLES</span></span>

### <span data-ttu-id="a1430-108">範例 1：在網路介面上取得有效的網路安全性群組</span><span class="sxs-lookup"><span data-stu-id="a1430-108">Example 1: Get the effective network security group on a network interface</span></span>
```
PS C:\>Get-AzEffectiveNetworkSecurityGroup -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="a1430-109">此命令會獲得與名為 myResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的所有有效網路安全性規則。</span><span class="sxs-lookup"><span data-stu-id="a1430-109">This command gets all of the effective network security rules associated with the network interface named MyNetworkInterface in the resource group named myResourceGroup.</span></span>

## <span data-ttu-id="a1430-110">參數</span><span class="sxs-lookup"><span data-stu-id="a1430-110">PARAMETERS</span></span>

### <span data-ttu-id="a1430-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1430-111">-DefaultProfile</span></span>
<span data-ttu-id="a1430-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1430-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1430-113">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a1430-113">-NetworkInterfaceName</span></span>
<span data-ttu-id="a1430-114">指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1430-114">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="a1430-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1430-115">-ResourceGroupName</span></span>
<span data-ttu-id="a1430-116">指定網路介面的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a1430-116">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="a1430-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1430-117">CommonParameters</span></span>
<span data-ttu-id="a1430-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1430-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1430-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1430-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1430-120">輸入</span><span class="sxs-lookup"><span data-stu-id="a1430-120">INPUTS</span></span>

### <span data-ttu-id="a1430-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a1430-121">System.String</span></span>

## <span data-ttu-id="a1430-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a1430-122">OUTPUTS</span></span>

### <span data-ttu-id="a1430-123">Microsoft.Azure.Commands.Network.models.PSEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a1430-123">Microsoft.Azure.Commands.Network.Models.PSEffectiveNetworkSecurityGroup</span></span>

## <span data-ttu-id="a1430-124">筆記</span><span class="sxs-lookup"><span data-stu-id="a1430-124">NOTES</span></span>

## <span data-ttu-id="a1430-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1430-125">RELATED LINKS</span></span>

[<span data-ttu-id="a1430-126">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a1430-126">Get-AzEffectiveRouteTable</span></span>](./Get-AzEffectiveRouteTable.md)


