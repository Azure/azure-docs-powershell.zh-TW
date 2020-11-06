---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerVirtualNetworkRule.md
ms.openlocfilehash: 08d14217cff370557009167e09cd7e5396df4e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446624"
---
# <span data-ttu-id="4b83e-101">New-AzureRmSqlServerVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b83e-101">New-AzureRmSqlServerVirtualNetworkRule</span></span>

## <span data-ttu-id="4b83e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b83e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b83e-103">建立 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="4b83e-103">Creates an Azure SQL Server Virtual Network Rule.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b83e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b83e-104">SYNTAX</span></span>

```
New-AzureRmSqlServerVirtualNetworkRule -VirtualNetworkRuleName <String> -VirtualNetworkSubnetId <String>
 -ServerName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b83e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b83e-105">DESCRIPTION</span></span>
<span data-ttu-id="4b83e-106">建立 Azure SQL Server 虛擬網路規則。</span><span class="sxs-lookup"><span data-stu-id="4b83e-106">Creates an Azure SQL Server Virtual Network Rule.</span></span> <span data-ttu-id="4b83e-107">虛擬網路規則是用來將 Azure SQL Server 連線至特定的虛擬網路，以限制 Azure SQL Server 上的存取權只在虛擬網路中提供。</span><span class="sxs-lookup"><span data-stu-id="4b83e-107">Virtual Network Rules are used to connect the Azure SQL Server to a specific Virtual Network in order to restrict the access on the Azure SQL Server to only be available within the Virtual Network.</span></span> 

## <span data-ttu-id="4b83e-108">示例</span><span class="sxs-lookup"><span data-stu-id="4b83e-108">EXAMPLES</span></span>

### <span data-ttu-id="4b83e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="4b83e-109">Example 1</span></span>
```
PS C:\> $virtualNetworkRule = New-AzureRmSqlServerVirtualNetworkRule -ResourceGroupName rg -ServerName serverName -VirtualNetworkRuleName virtualNetworkRuleName -VirtualNetworkSubnetId virtualNetworkSubnetId
```

<span data-ttu-id="4b83e-110">建立 Azure SQL Server 虛擬網路規則</span><span class="sxs-lookup"><span data-stu-id="4b83e-110">Creates an Azure SQL Server virtual network rule</span></span>

## <span data-ttu-id="4b83e-111">參數</span><span class="sxs-lookup"><span data-stu-id="4b83e-111">PARAMETERS</span></span>

### <span data-ttu-id="4b83e-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b83e-112">-ResourceGroupName</span></span>
<span data-ttu-id="4b83e-113">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b83e-113">The name of the resource group.</span></span>

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

### <span data-ttu-id="4b83e-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b83e-114">-ServerName</span></span>
<span data-ttu-id="4b83e-115">Azure Sql Server 名稱。</span><span class="sxs-lookup"><span data-stu-id="4b83e-115">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="4b83e-116">-VirtualNetworkRuleName</span><span class="sxs-lookup"><span data-stu-id="4b83e-116">-VirtualNetworkRuleName</span></span>
<span data-ttu-id="4b83e-117">Azure Sql Server 虛擬網路規則名稱。</span><span class="sxs-lookup"><span data-stu-id="4b83e-117">Azure Sql Server Virtual Network Rule Name.</span></span>

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

### <span data-ttu-id="4b83e-118">-VirtualNetworkSubnetId</span><span class="sxs-lookup"><span data-stu-id="4b83e-118">-VirtualNetworkSubnetId</span></span>
<span data-ttu-id="4b83e-119">指定 Microsoft. 網路詳細資料的虛擬網路子網識別碼</span><span class="sxs-lookup"><span data-stu-id="4b83e-119">The Virtual Network Subnet Id that specifies the Microsoft.Network details</span></span>

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

### <span data-ttu-id="4b83e-120">-確認</span><span class="sxs-lookup"><span data-stu-id="4b83e-120">-Confirm</span></span>
<span data-ttu-id="4b83e-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b83e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b83e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b83e-122">-WhatIf</span></span>
<span data-ttu-id="4b83e-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b83e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b83e-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b83e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b83e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b83e-125">-DefaultProfile</span></span>
<span data-ttu-id="4b83e-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b83e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b83e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b83e-127">CommonParameters</span></span>
<span data-ttu-id="4b83e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b83e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b83e-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b83e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b83e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="4b83e-130">INPUTS</span></span>

### <span data-ttu-id="4b83e-131">System.object</span><span class="sxs-lookup"><span data-stu-id="4b83e-131">System.String</span></span>

## <span data-ttu-id="4b83e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="4b83e-132">OUTPUTS</span></span>

### <span data-ttu-id="4b83e-133">AzureSqlServerVirtualNetworkRuleModel 中的 [VirtualNetworkRule]</span><span class="sxs-lookup"><span data-stu-id="4b83e-133">Microsoft.Azure.Commands.Sql.VirtualNetworkRule.Model.AzureSqlServerVirtualNetworkRuleModel</span></span>

## <span data-ttu-id="4b83e-134">筆記</span><span class="sxs-lookup"><span data-stu-id="4b83e-134">NOTES</span></span>

## <span data-ttu-id="4b83e-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b83e-135">RELATED LINKS</span></span>

