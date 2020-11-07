---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
ms.openlocfilehash: 403a3d37418e022032988d5d7fccb40a1e79f449
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800469"
---
# <span data-ttu-id="5be14-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="5be14-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="5be14-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5be14-102">SYNOPSIS</span></span>
<span data-ttu-id="5be14-103">取得網路介面的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="5be14-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5be14-104">句法</span><span class="sxs-lookup"><span data-stu-id="5be14-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5be14-105">說明</span><span class="sxs-lookup"><span data-stu-id="5be14-105">DESCRIPTION</span></span>
<span data-ttu-id="5be14-106">**AzureRmEffectiveRouteTable** Cmdlet 會傳回在網路介面上套用的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="5be14-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="5be14-107">示例</span><span class="sxs-lookup"><span data-stu-id="5be14-107">EXAMPLES</span></span>

### <span data-ttu-id="5be14-108">範例1：在網路介面上取得有效路由資料表</span><span class="sxs-lookup"><span data-stu-id="5be14-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="5be14-109">這個命令會取得與名為 MyResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="5be14-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="5be14-110">參數</span><span class="sxs-lookup"><span data-stu-id="5be14-110">PARAMETERS</span></span>

### <span data-ttu-id="5be14-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5be14-111">-AsJob</span></span>
<span data-ttu-id="5be14-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="5be14-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5be14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be14-113">-DefaultProfile</span></span>
<span data-ttu-id="5be14-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5be14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5be14-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="5be14-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="5be14-116">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="5be14-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="5be14-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be14-117">-ResourceGroupName</span></span>
<span data-ttu-id="5be14-118">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="5be14-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="5be14-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be14-119">CommonParameters</span></span>
<span data-ttu-id="5be14-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5be14-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be14-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5be14-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be14-122">輸入</span><span class="sxs-lookup"><span data-stu-id="5be14-122">INPUTS</span></span>

## <span data-ttu-id="5be14-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5be14-123">OUTPUTS</span></span>

### <span data-ttu-id="5be14-124">PSEffectiveRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5be14-124">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="5be14-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5be14-125">NOTES</span></span>

## <span data-ttu-id="5be14-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5be14-126">RELATED LINKS</span></span>

[<span data-ttu-id="5be14-127">AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5be14-127">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


