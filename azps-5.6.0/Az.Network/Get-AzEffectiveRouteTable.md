---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: 28ec38b9f2dfbb658203aa46fe0d8225aca08a5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905901"
---
# <span data-ttu-id="a00a7-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a00a7-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="a00a7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a00a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a00a7-103">獲得網路介面的有效路由資料表。</span><span class="sxs-lookup"><span data-stu-id="a00a7-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="a00a7-104">語法</span><span class="sxs-lookup"><span data-stu-id="a00a7-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a00a7-105">描述</span><span class="sxs-lookup"><span data-stu-id="a00a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a00a7-106">**Get-AzEffectiveRouteTable** Cmdlet 會返回網路介面上所適用的有效路由資料表。</span><span class="sxs-lookup"><span data-stu-id="a00a7-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="a00a7-107">例子</span><span class="sxs-lookup"><span data-stu-id="a00a7-107">EXAMPLES</span></span>

### <span data-ttu-id="a00a7-108">範例 1：取得網路介面上的有效路由資料表</span><span class="sxs-lookup"><span data-stu-id="a00a7-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a00a7-109">此命令會獲得與名為 MyResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的有效路由資料表。</span><span class="sxs-lookup"><span data-stu-id="a00a7-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="a00a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="a00a7-110">PARAMETERS</span></span>

### <span data-ttu-id="a00a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a00a7-111">-AsJob</span></span>
<span data-ttu-id="a00a7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a00a7-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a00a7-113">-DefaultProfile</span></span>
<span data-ttu-id="a00a7-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a00a7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a00a7-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="a00a7-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="a00a7-116">指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="a00a7-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="a00a7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a00a7-117">-ResourceGroupName</span></span>
<span data-ttu-id="a00a7-118">指定網路介面的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a00a7-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="a00a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00a7-119">CommonParameters</span></span>
<span data-ttu-id="a00a7-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a00a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00a7-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a00a7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00a7-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a00a7-122">INPUTS</span></span>

### <span data-ttu-id="a00a7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a00a7-123">System.String</span></span>

## <span data-ttu-id="a00a7-124">輸出</span><span class="sxs-lookup"><span data-stu-id="a00a7-124">OUTPUTS</span></span>

### <span data-ttu-id="a00a7-125">Microsoft.Azure.Commands.Network.models.PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="a00a7-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="a00a7-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a00a7-126">NOTES</span></span>

## <span data-ttu-id="a00a7-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a00a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="a00a7-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a00a7-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


