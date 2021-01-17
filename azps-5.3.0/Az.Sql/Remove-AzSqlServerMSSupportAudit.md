---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Remove-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 1e9586f6a16562217f4c5d9eb7778ba6ec887a68
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435009"
---
# <span data-ttu-id="e6a89-101">Remove-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="e6a89-101">Remove-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="e6a89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6a89-102">SYNOPSIS</span></span>
<span data-ttu-id="e6a89-103">移除 Azure SQL server 的 Microsoft 支援作業審核設定。</span><span class="sxs-lookup"><span data-stu-id="e6a89-103">Removes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="e6a89-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6a89-104">SYNTAX</span></span>

### <span data-ttu-id="e6a89-105">ServerParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e6a89-105">ServerParameterSet (Default)</span></span>
```
Remove-AzSqlServerMSSupportAudit [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6a89-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6a89-106">ServerObjectParameterSet</span></span>
```
Remove-AzSqlServerMSSupportAudit -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6a89-107">說明</span><span class="sxs-lookup"><span data-stu-id="e6a89-107">DESCRIPTION</span></span>
<span data-ttu-id="e6a89-108">**AzSqlServerMSSupportAudit** Cmdlet 會移除 Azure SQL Server 的 Microsoft 支援作業審核設定。</span><span class="sxs-lookup"><span data-stu-id="e6a89-108">The **Remove-AzSqlServerMSSupportAudit** cmdlet removes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="e6a89-109">若要使用 Cmdlet，請使用 *ResourceGroupName* 和 *ServerName* 參數來識別伺服器。</span><span class="sxs-lookup"><span data-stu-id="e6a89-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>

## <span data-ttu-id="e6a89-110">示例</span><span class="sxs-lookup"><span data-stu-id="e6a89-110">EXAMPLES</span></span>

### <span data-ttu-id="e6a89-111">範例1：移除 Azure SQL server 的 Microsoft 支援作業審核設定</span><span class="sxs-lookup"><span data-stu-id="e6a89-111">Example 1: Remove the Microsoft support operations auditing settings of an Azure SQL server</span></span>
```powershell
PS C:\>Remove-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="e6a89-112">範例2：在管道中移除 Azure SQL server 的 Microsoft 支援審核設定</span><span class="sxs-lookup"><span data-stu-id="e6a89-112">Example 2: Remove, through pipeline, the Microsoft support auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Remove-AzSqlServerMSSupportAudit
```

## <span data-ttu-id="e6a89-113">參數</span><span class="sxs-lookup"><span data-stu-id="e6a89-113">PARAMETERS</span></span>

### <span data-ttu-id="e6a89-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6a89-114">-AsJob</span></span>
<span data-ttu-id="e6a89-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e6a89-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6a89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6a89-116">-DefaultProfile</span></span>
<span data-ttu-id="e6a89-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6a89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a89-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6a89-118">-ResourceGroupName</span></span>
<span data-ttu-id="e6a89-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6a89-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a89-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6a89-120">-ServerName</span></span>
<span data-ttu-id="e6a89-121">SQL server 名稱。</span><span class="sxs-lookup"><span data-stu-id="e6a89-121">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6a89-122">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="e6a89-122">-ServerObject</span></span>
<span data-ttu-id="e6a89-123">伺服器物件來管理其審核原則。</span><span class="sxs-lookup"><span data-stu-id="e6a89-123">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6a89-124">-確認</span><span class="sxs-lookup"><span data-stu-id="e6a89-124">-Confirm</span></span>
<span data-ttu-id="e6a89-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6a89-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6a89-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6a89-126">-WhatIf</span></span>
<span data-ttu-id="e6a89-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6a89-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6a89-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6a89-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6a89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6a89-129">CommonParameters</span></span>
<span data-ttu-id="e6a89-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6a89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6a89-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e6a89-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6a89-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e6a89-132">INPUTS</span></span>

### <span data-ttu-id="e6a89-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e6a89-133">System.String</span></span>

### <span data-ttu-id="e6a89-134">AzureSqlServerModel 的 [.Sql] 命令</span><span class="sxs-lookup"><span data-stu-id="e6a89-134">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="e6a89-135">輸出</span><span class="sxs-lookup"><span data-stu-id="e6a89-135">OUTPUTS</span></span>

### <span data-ttu-id="e6a89-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e6a89-136">System.Boolean</span></span>

## <span data-ttu-id="e6a89-137">筆記</span><span class="sxs-lookup"><span data-stu-id="e6a89-137">NOTES</span></span>

## <span data-ttu-id="e6a89-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6a89-138">RELATED LINKS</span></span>
