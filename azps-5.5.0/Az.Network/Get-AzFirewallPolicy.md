---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100135947"
---
# <span data-ttu-id="6c1cf-101">Get-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6c1cf-101">Get-AzFirewallPolicy</span></span>

## <span data-ttu-id="6c1cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1cf-103">取得 Azure 防火牆原則</span><span class="sxs-lookup"><span data-stu-id="6c1cf-103">Gets a Azure Firewall Policy</span></span>

## <span data-ttu-id="6c1cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c1cf-104">SYNTAX</span></span>

### <span data-ttu-id="6c1cf-105">GetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c1cf-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c1cf-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c1cf-106">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c1cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="6c1cf-107">DESCRIPTION</span></span>
<span data-ttu-id="6c1cf-108">**AzFirewallPolicy** Cmdlet 會取得資源群組中的一個或多個防火牆</span><span class="sxs-lookup"><span data-stu-id="6c1cf-108">The **Get-AzFirewallPolicy** cmdlet gets one or more Firewalls in a resource group</span></span>

## <span data-ttu-id="6c1cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c1cf-109">EXAMPLES</span></span>

### <span data-ttu-id="6c1cf-110">範例1</span><span class="sxs-lookup"><span data-stu-id="6c1cf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

<span data-ttu-id="6c1cf-111">這個範例會在資源群組 "TestRg" 中取得名為 "firewallPolicy" 的防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-111">This example get a firewall policy named "firewallPolicy" in the resource group "TestRg"</span></span>

## <span data-ttu-id="6c1cf-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c1cf-112">PARAMETERS</span></span>

### <span data-ttu-id="6c1cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1cf-113">-DefaultProfile</span></span>
<span data-ttu-id="6c1cf-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c1cf-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c1cf-115">-Name</span></span>
<span data-ttu-id="6c1cf-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-116">The resource name.</span></span>

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

### <span data-ttu-id="6c1cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="6c1cf-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-118">The resource group name.</span></span>

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

### <span data-ttu-id="6c1cf-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c1cf-119">-ResourceId</span></span>
<span data-ttu-id="6c1cf-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-120">The resource Id.</span></span>

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

### <span data-ttu-id="6c1cf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1cf-121">CommonParameters</span></span>
<span data-ttu-id="6c1cf-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1cf-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c1cf-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1cf-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6c1cf-124">INPUTS</span></span>

### <span data-ttu-id="6c1cf-125">System.object</span><span class="sxs-lookup"><span data-stu-id="6c1cf-125">System.String</span></span>

## <span data-ttu-id="6c1cf-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6c1cf-126">OUTPUTS</span></span>

### <span data-ttu-id="6c1cf-127">PSAzureFirewall 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c1cf-127">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="6c1cf-128">[System.object]. IEnumerable ' 1 [PSAzureFirewall，1.12.0.0，system.object，版本 =，Culture = 中性，PublicKeyToken = null]] （Culture = null）]</span><span class="sxs-lookup"><span data-stu-id="6c1cf-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="6c1cf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="6c1cf-129">NOTES</span></span>

## <span data-ttu-id="6c1cf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c1cf-130">RELATED LINKS</span></span>
