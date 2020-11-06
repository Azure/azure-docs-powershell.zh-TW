---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservervirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 14eb3de52c08c276638c5079a1e64c65da6669f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453987"
---
# <span data-ttu-id="a0e77-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a0e77-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a0e77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0e77-102">SYNOPSIS</span></span>
<span data-ttu-id="a0e77-103">取得或列出 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a0e77-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0e77-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0e77-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0e77-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0e77-105">DESCRIPTION</span></span>
<span data-ttu-id="a0e77-106">這個命令會在伺服器上取得特定的 Azure SQL Server 虛擬網路規則或 Azure SQL Server 虛擬網路規則清單。</span><span class="sxs-lookup"><span data-stu-id="a0e77-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="a0e77-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0e77-107">EXAMPLES</span></span>

### <span data-ttu-id="a0e77-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a0e77-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="a0e77-109">取得單一 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="a0e77-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="a0e77-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a0e77-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="a0e77-111">在指定的伺服器下取得 Azure SQL Server 虛擬網路規則清單</span><span class="sxs-lookup"><span data-stu-id="a0e77-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="a0e77-112">參數</span><span class="sxs-lookup"><span data-stu-id="a0e77-112">PARAMETERS</span></span>

### <span data-ttu-id="a0e77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0e77-113">-DefaultProfile</span></span>
<span data-ttu-id="a0e77-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a0e77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0e77-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0e77-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0e77-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0e77-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="a0e77-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a0e77-117">-ServerName</span></span>
<span data-ttu-id="a0e77-118">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="a0e77-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a0e77-119">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a0e77-119">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a0e77-120">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="a0e77-120">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0e77-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0e77-121">CommonParameters</span></span>
<span data-ttu-id="a0e77-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0e77-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0e77-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0e77-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0e77-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a0e77-124">INPUTS</span></span>

### <span data-ttu-id="a0e77-125">System.object</span><span class="sxs-lookup"><span data-stu-id="a0e77-125">System.String</span></span>

## <span data-ttu-id="a0e77-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a0e77-126">OUTPUTS</span></span>

### <span data-ttu-id="a0e77-127">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="a0e77-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a0e77-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a0e77-128">NOTES</span></span>

## <span data-ttu-id="a0e77-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0e77-129">RELATED LINKS</span></span>
