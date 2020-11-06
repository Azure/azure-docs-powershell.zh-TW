---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: e73409edf07402dd44cb5f29a6e878d29d7bfede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446643"
---
# <span data-ttu-id="a29f4-101">Get-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a29f4-101">Get-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="a29f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a29f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a29f4-103">取得或列出 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="a29f4-103">Gets or lists Azure SQL Server Virtual Network Rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a29f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="a29f4-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerVirtualNetworkRule [-VirtualNetworkRuleName <String>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a29f4-105">說明</span><span class="sxs-lookup"><span data-stu-id="a29f4-105">DESCRIPTION</span></span>
<span data-ttu-id="a29f4-106">這個命令會在伺服器上取得特定的 Azure SQL Server 虛擬網路規則或 Azure SQL Server 虛擬網路規則清單。</span><span class="sxs-lookup"><span data-stu-id="a29f4-106">This command gets a specific Azure SQL Server Virtual Network Rule or a list of Azure SQL Server Virtual Network Rules under a server.</span></span>

## <span data-ttu-id="a29f4-107">示例</span><span class="sxs-lookup"><span data-stu-id="a29f4-107">EXAMPLES</span></span>

### <span data-ttu-id="a29f4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a29f4-108">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName
```

<span data-ttu-id="a29f4-109">取得單一 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="a29f4-109">Gets an single Azure SQL Server virtual network rule</span></span>

### <span data-ttu-id="a29f4-110">範例2</span><span class="sxs-lookup"><span data-stu-id="a29f4-110">Example 2</span></span>
```
PS C:\> $virtualNetworkRules = Get-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName
```

<span data-ttu-id="a29f4-111">在指定的伺服器下取得 Azure SQL Server 虛擬網路規則清單</span><span class="sxs-lookup"><span data-stu-id="a29f4-111">Gets the list of Azure SQL Server virtual network rules under the specified server</span></span>

## <span data-ttu-id="a29f4-112">參數</span><span class="sxs-lookup"><span data-stu-id="a29f4-112">PARAMETERS</span></span>

### <span data-ttu-id="a29f4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a29f4-113">-ResourceGroupName</span></span>
<span data-ttu-id="a29f4-114">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a29f4-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="a29f4-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a29f4-115">-ServerName</span></span>
<span data-ttu-id="a29f4-116">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="a29f4-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a29f4-117">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="a29f4-117">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="a29f4-118">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="a29f4-118">The Azure Sql Server Virtual Network Rule name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a29f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a29f4-119">-DefaultProfile</span></span>
<span data-ttu-id="a29f4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a29f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a29f4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a29f4-121">CommonParameters</span></span>
<span data-ttu-id="a29f4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a29f4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a29f4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a29f4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a29f4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a29f4-124">INPUTS</span></span>

### <span data-ttu-id="a29f4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="a29f4-125">System.String</span></span>

## <span data-ttu-id="a29f4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a29f4-126">OUTPUTS</span></span>

### <span data-ttu-id="a29f4-127">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="a29f4-127">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="a29f4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="a29f4-128">NOTES</span></span>

## <span data-ttu-id="a29f4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="a29f4-129">RELATED LINKS</span></span>

