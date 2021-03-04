---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: 056a70f6c085f3c0a936f9e144708c7258a3d5c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903154"
---
# <span data-ttu-id="e47ff-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="e47ff-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="e47ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e47ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e47ff-103">獲得 Azure 防火牆政策</span><span class="sxs-lookup"><span data-stu-id="e47ff-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="e47ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="e47ff-104">SYNTAX</span></span>

### <span data-ttu-id="e47ff-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e47ff-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e47ff-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e47ff-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e47ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="e47ff-107">DESCRIPTION</span></span>
<span data-ttu-id="e47ff-108">**Get-AzFirewallPolicy** Cmdlet 在資源群組中取得一或多個防火牆</span><span class="sxs-lookup"><span data-stu-id="e47ff-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="e47ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="e47ff-109">EXAMPLES</span></span>

### <span data-ttu-id="e47ff-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="e47ff-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="e47ff-111">此範例在資源群組 "TestRg" 中取得名為 "firewallPolicy" 的防火牆策略</span><span class="sxs-lookup"><span data-stu-id="e47ff-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="e47ff-112">參數</span><span class="sxs-lookup"><span data-stu-id="e47ff-112">PARAMETERS</span></span>

### <span data-ttu-id="e47ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47ff-113">-DefaultProfile</span></span>
<span data-ttu-id="e47ff-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e47ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47ff-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e47ff-115">-Name</span></span>
<span data-ttu-id="e47ff-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e47ff-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e47ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e47ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="e47ff-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e47ff-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e47ff-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e47ff-119">-ResourceId</span></span>
<span data-ttu-id="e47ff-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e47ff-120">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e47ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47ff-121">CommonParameters</span></span>
<span data-ttu-id="e47ff-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e47ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47ff-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e47ff-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47ff-124">輸入</span><span class="sxs-lookup"><span data-stu-id="e47ff-124">INPUTS</span></span>

### <span data-ttu-id="e47ff-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e47ff-125">System.String</span></span>

## <span data-ttu-id="e47ff-126">輸出</span><span class="sxs-lookup"><span data-stu-id="e47ff-126">OUTPUTS</span></span>

### <span data-ttu-id="e47ff-127">Microsoft.Azure.Commands.Network.models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="e47ff-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="e47ff-128">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e47ff-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e47ff-129">筆記</span><span class="sxs-lookup"><span data-stu-id="e47ff-129">NOTES</span></span>

## <span data-ttu-id="e47ff-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="e47ff-130">RELATED LINKS</span></span>
