---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 355b8fdffd5d1e9e16fe9bfaf504d627a8b9b167
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626474"
---
# <span data-ttu-id="8ab92-101">Set-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8ab92-101">Set-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="8ab92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8ab92-102">SYNOPSIS</span></span>
<span data-ttu-id="8ab92-103">修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="8ab92-103">Modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ab92-104">句法</span><span class="sxs-lookup"><span data-stu-id="8ab92-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ab92-105">說明</span><span class="sxs-lookup"><span data-stu-id="8ab92-105">DESCRIPTION</span></span>
<span data-ttu-id="8ab92-106">這個命令會修改 Azure SQL Server 虛擬網路規則的設定。</span><span class="sxs-lookup"><span data-stu-id="8ab92-106">This command modifies the configuration of an Azure SQL Server Virtual Network Rule.</span></span>


<span data-ttu-id="8ab92-107">若要控制伺服器中的一組虛擬網路規則，請改用 [Add-AzureRmSqlServerVirtualNetworkRule] 和 [Remove-AzureRmSqlServerVirtualNetworkRule]。</span><span class="sxs-lookup"><span data-stu-id="8ab92-107">To control the set of virtual network rules in the server, use 'Add-AzureRmSqlServerVirtualNetworkRule' and 'Remove-AzureRmSqlServerVirtualNetworkRule' instead.</span></span>

## <span data-ttu-id="8ab92-108">示例</span><span class="sxs-lookup"><span data-stu-id="8ab92-108">EXAMPLES</span></span>

### <span data-ttu-id="8ab92-109">範例1</span><span class="sxs-lookup"><span data-stu-id="8ab92-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Set-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="8ab92-110">使用新的虛擬網路子網 id （包含新虛擬網路的相關資訊）來修改現有的虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="8ab92-110">Modifies an existing virtual network rule with the new virtual network subnet id which contains information about the new virtual network</span></span>

## <span data-ttu-id="8ab92-111">參數</span><span class="sxs-lookup"><span data-stu-id="8ab92-111">PARAMETERS</span></span>

### <span data-ttu-id="8ab92-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ab92-112">-ResourceGroupName</span></span>
<span data-ttu-id="8ab92-113">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab92-113">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8ab92-114">-ServerName</span></span>
<span data-ttu-id="8ab92-115">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab92-115">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="8ab92-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="8ab92-117">Azure Sql Server 虛擬網路規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ab92-117">The name of the Azure Sql Server Virtual Network Rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="8ab92-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="8ab92-119">規則的虛擬網路子網識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ab92-119">The Virtual Network Subnet Id for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-120">-確認</span><span class="sxs-lookup"><span data-stu-id="8ab92-120">-Confirm</span></span>
<span data-ttu-id="8ab92-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8ab92-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ab92-122">-WhatIf</span></span>
<span data-ttu-id="8ab92-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ab92-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ab92-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ab92-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ab92-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ab92-125">-DefaultProfile</span></span>
<span data-ttu-id="8ab92-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ab92-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ab92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ab92-127">CommonParameters</span></span>
<span data-ttu-id="8ab92-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8ab92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ab92-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8ab92-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ab92-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8ab92-130">INPUTS</span></span>

### <span data-ttu-id="8ab92-131">System.object</span><span class="sxs-lookup"><span data-stu-id="8ab92-131">System.String</span></span>

## <span data-ttu-id="8ab92-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8ab92-132">OUTPUTS</span></span>

### <span data-ttu-id="8ab92-133">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="8ab92-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="8ab92-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8ab92-134">NOTES</span></span>

## <span data-ttu-id="8ab92-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ab92-135">RELATED LINKS</span></span>

