---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmEffectiveRouteTable.md
ms.openlocfilehash: 8095e2ebd1d9e55e8f5bc847f4a72277363e197a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455199"
---
# <span data-ttu-id="2d70e-101">Get-AzureRmEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d70e-101">Get-AzureRmEffectiveRouteTable</span></span>

## <span data-ttu-id="2d70e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d70e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d70e-103">取得網路介面的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="2d70e-103">Gets the effective route table of a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d70e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d70e-104">SYNTAX</span></span>

```
Get-AzureRmEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d70e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2d70e-105">DESCRIPTION</span></span>
<span data-ttu-id="2d70e-106">**AzureRmEffectiveRouteTable** Cmdlet 會傳回在網路介面上套用的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="2d70e-106">The **Get-AzureRmEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="2d70e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2d70e-107">EXAMPLES</span></span>

### <span data-ttu-id="2d70e-108">範例1：在網路介面上取得有效路由資料表</span><span class="sxs-lookup"><span data-stu-id="2d70e-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzureRmEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2d70e-109">這個命令會取得與名為 MyResourceGroup 之資源群組中名為 MyNetworkInterface 的網路介面相關聯的有效路由表。</span><span class="sxs-lookup"><span data-stu-id="2d70e-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2d70e-110">參數</span><span class="sxs-lookup"><span data-stu-id="2d70e-110">PARAMETERS</span></span>

### <span data-ttu-id="2d70e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d70e-111">-AsJob</span></span>
<span data-ttu-id="2d70e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d70e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d70e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d70e-113">-DefaultProfile</span></span>
<span data-ttu-id="2d70e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d70e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d70e-115">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2d70e-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="2d70e-116">已指定網路介面的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d70e-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="2d70e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d70e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2d70e-118">指定網路介面的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="2d70e-118">Specifies the resource group of a network interface.</span></span>

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

### <span data-ttu-id="2d70e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d70e-119">CommonParameters</span></span>
<span data-ttu-id="2d70e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d70e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d70e-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d70e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d70e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="2d70e-122">INPUTS</span></span>

### <span data-ttu-id="2d70e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="2d70e-123">System.String</span></span>

## <span data-ttu-id="2d70e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2d70e-124">OUTPUTS</span></span>

### <span data-ttu-id="2d70e-125">PSEffectiveRoute 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2d70e-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="2d70e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2d70e-126">NOTES</span></span>

## <span data-ttu-id="2d70e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d70e-127">RELATED LINKS</span></span>

[<span data-ttu-id="2d70e-128">AzureRmEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="2d70e-128">Get-AzureRmEffectiveNetworkSecurityGroup</span></span>](./Get-AzureRmEffectiveNetworkSecurityGroup.md)


