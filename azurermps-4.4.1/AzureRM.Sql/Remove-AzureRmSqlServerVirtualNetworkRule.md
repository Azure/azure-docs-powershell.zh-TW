---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 8c680cf87deedf5fc4bd8671a60db4329a1f68ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626488"
---
# <span data-ttu-id="25a38-101">Remove-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="25a38-101">Remove-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="25a38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25a38-102">SYNOPSIS</span></span>
<span data-ttu-id="25a38-103">刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="25a38-103">Deletes an Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25a38-104">句法</span><span class="sxs-lookup"><span data-stu-id="25a38-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25a38-105">說明</span><span class="sxs-lookup"><span data-stu-id="25a38-105">DESCRIPTION</span></span>
<span data-ttu-id="25a38-106">這個命令會刪除 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="25a38-106">This command deletes an Azure SQL Server Virtual Network Rule.</span></span>

## <span data-ttu-id="25a38-107">示例</span><span class="sxs-lookup"><span data-stu-id="25a38-107">EXAMPLES</span></span>

### <span data-ttu-id="25a38-108">範例1</span><span class="sxs-lookup"><span data-stu-id="25a38-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Remove-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="25a38-109">刪除現有的 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="25a38-109">Deletes an existing Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="25a38-110">參數</span><span class="sxs-lookup"><span data-stu-id="25a38-110">PARAMETERS</span></span>

### <span data-ttu-id="25a38-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25a38-111">-ResourceGroupName</span></span>
<span data-ttu-id="25a38-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25a38-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="25a38-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25a38-113">-ServerName</span></span>
<span data-ttu-id="25a38-114">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="25a38-114">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="25a38-115">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="25a38-115">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="25a38-116">Azure Sql Server 虛擬網路規則名稱</span><span class="sxs-lookup"><span data-stu-id="25a38-116">Azure Sql Server Virtual Network Rule name</span></span>

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

### <span data-ttu-id="25a38-117">-確認</span><span class="sxs-lookup"><span data-stu-id="25a38-117">-Confirm</span></span>
<span data-ttu-id="25a38-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25a38-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25a38-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25a38-119">-WhatIf</span></span>
<span data-ttu-id="25a38-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25a38-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25a38-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25a38-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25a38-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25a38-122">-DefaultProfile</span></span>
<span data-ttu-id="25a38-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25a38-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25a38-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25a38-124">CommonParameters</span></span>
<span data-ttu-id="25a38-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25a38-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25a38-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="25a38-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25a38-127">輸入</span><span class="sxs-lookup"><span data-stu-id="25a38-127">INPUTS</span></span>

### <span data-ttu-id="25a38-128">System.object</span><span class="sxs-lookup"><span data-stu-id="25a38-128">System.String</span></span>

## <span data-ttu-id="25a38-129">輸出</span><span class="sxs-lookup"><span data-stu-id="25a38-129">OUTPUTS</span></span>

### <span data-ttu-id="25a38-130">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="25a38-130">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="25a38-131">筆記</span><span class="sxs-lookup"><span data-stu-id="25a38-131">NOTES</span></span>

## <span data-ttu-id="25a38-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="25a38-132">RELATED LINKS</span></span>

