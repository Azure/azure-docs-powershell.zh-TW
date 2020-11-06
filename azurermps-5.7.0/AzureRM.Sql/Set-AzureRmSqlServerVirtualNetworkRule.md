---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 07b0f4aa0bcf5dd052256cdc020f6bff2c50193d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445948"
---
# <span data-ttu-id="d38c5-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d38c5-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="d38c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d38c5-102">SYNOPSIS</span></span>
<span data-ttu-id="d38c5-103">修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="d38c5-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d38c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d38c5-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d38c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d38c5-105">DESCRIPTION</span></span>
<span data-ttu-id="d38c5-106">這個命令會修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="d38c5-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="d38c5-107">若要控制伺服器中的一組虛擬網路規則，請改用 [Add-AzureRmSqlServerVirtualNetworkRule] 和 [Remove-AzureRmSqlServerVirtualNetworkRule]。</span><span class="sxs-lookup"><span data-stu-id="d38c5-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="d38c5-108">示例</span><span class="sxs-lookup"><span data-stu-id="d38c5-108">EXAMPLES</span></span>

### <span data-ttu-id="d38c5-109">範例1</span><span class="sxs-lookup"><span data-stu-id="d38c5-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="d38c5-110">使用新的虛擬網路子網 id （包含新虛擬網路的相關資訊）來修改現有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="d38c5-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="d38c5-111">參數</span><span class="sxs-lookup"><span data-stu-id="d38c5-111">PARAMETERS</span></span>

### <span data-ttu-id="d38c5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d38c5-112">-AsJob</span></span>
<span data-ttu-id="d38c5-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d38c5-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="d38c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38c5-114">-DefaultProfile</span></span>
<span data-ttu-id="d38c5-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d38c5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d38c5-116">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d38c5-116">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="d38c5-117">在虛擬網路啟用 vnet 服務端點之前，請先建立防火牆規則。</span><span class="sxs-lookup"><span data-stu-id="d38c5-117">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="d38c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d38c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="d38c5-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d38c5-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d38c5-120">-ServerName</span></span>
<span data-ttu-id="d38c5-121">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="d38c5-121">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-122">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="d38c5-122">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="d38c5-123">Azure Sql Server 虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="d38c5-123">The name of the Azure Sql Server Virtual Network Rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-124">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="d38c5-124">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="d38c5-125">規則的虛擬網路子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="d38c5-125">The Virtual Network Subnet Id for the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="d38c5-126">-Confirm</span></span>
<span data-ttu-id="d38c5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d38c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d38c5-128">-WhatIf</span></span>
<span data-ttu-id="d38c5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d38c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d38c5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d38c5-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38c5-131">CommonParameters</span></span>
<span data-ttu-id="d38c5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d38c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38c5-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d38c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38c5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="d38c5-134">INPUTS</span></span>

### <span data-ttu-id="d38c5-135">System.object</span><span class="sxs-lookup"><span data-stu-id="d38c5-135">System.String</span></span>

## <span data-ttu-id="d38c5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="d38c5-136">OUTPUTS</span></span>

### <span data-ttu-id="d38c5-137">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="d38c5-137">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="d38c5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="d38c5-138">NOTES</span></span>

## <span data-ttu-id="d38c5-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="d38c5-139">RELATED LINKS</span></span>
