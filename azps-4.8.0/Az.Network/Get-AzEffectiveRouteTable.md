---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126525"
---
# <span data-ttu-id="ef6a4-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ef6a4-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="ef6a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6a4-103">取得網路介面的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="ef6a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef6a4-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef6a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6a4-106">**AzEffectiveRouteTable** Cmdlet 會傳回在網路介面上套用的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="ef6a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef6a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ef6a4-108">範例1：在網路介面上取得有效路由資料表</span><span class="sxs-lookup"><span data-stu-id="ef6a4-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="ef6a4-109">這個命令會取得與名為 MyResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="ef6a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef6a4-110">PARAMETERS</span></span>

### <span data-ttu-id="ef6a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef6a4-111">-AsJob</span></span>
<span data-ttu-id="ef6a4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef6a4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef6a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6a4-113">-DefaultProfile</span></span>
<span data-ttu-id="ef6a4-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef6a4-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="ef6a4-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="ef6a4-116">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="ef6a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef6a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="ef6a4-118">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="ef6a4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6a4-119">CommonParameters</span></span>
<span data-ttu-id="ef6a4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6a4-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ef6a4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6a4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ef6a4-122">INPUTS</span></span>

### <span data-ttu-id="ef6a4-123">System.object</span><span class="sxs-lookup"><span data-stu-id="ef6a4-123">System.String</span></span>

## <span data-ttu-id="ef6a4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ef6a4-124">OUTPUTS</span></span>

### <span data-ttu-id="ef6a4-125">PSEffectiveRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef6a4-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="ef6a4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ef6a4-126">NOTES</span></span>

## <span data-ttu-id="ef6a4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef6a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef6a4-128">AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ef6a4-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)

