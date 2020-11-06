---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: f42e378bb0bb5202f9f955dea1b844e343a0e037
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449991"
---
# <span data-ttu-id="f2ca9-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="f2ca9-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="f2ca9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ca9-103">取得網路介面的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2ca9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2ca9-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2ca9-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="f2ca9-106">**AzureRmEffectiveRouteTable** Cmdlet 會傳回在網路介面上套用的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="f2ca9-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="f2ca9-108">範例1：在網路介面上取得有效路由資料表</span><span class="sxs-lookup"><span data-stu-id="f2ca9-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f2ca9-109">這個命令會取得與名為 MyResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f2ca9-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="f2ca9-111">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="f2ca9-111">-NetworkInterfaceName</span></span>
<span data-ttu-id="f2ca9-112">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-112">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="f2ca9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ca9-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2ca9-114">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-114">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="f2ca9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ca9-115">-DefaultProfile</span></span>
<span data-ttu-id="f2ca9-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ca9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ca9-117">CommonParameters</span></span>
<span data-ttu-id="f2ca9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ca9-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2ca9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ca9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f2ca9-120">INPUTS</span></span>

## <span data-ttu-id="f2ca9-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f2ca9-121">OUTPUTS</span></span>

### <span data-ttu-id="f2ca9-122">PSEffectiveRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f2ca9-122">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="f2ca9-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f2ca9-123">NOTES</span></span>

## <span data-ttu-id="f2ca9-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2ca9-124">RELATED LINKS</span></span>

[<span data-ttu-id="f2ca9-125">AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="f2ca9-125">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


