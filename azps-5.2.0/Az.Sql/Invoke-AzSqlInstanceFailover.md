---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: ae92a4fa28f0715c7a2517f062113afb01a359cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281871"
---
# <span data-ttu-id="6524d-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="6524d-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="6524d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6524d-102">SYNOPSIS</span></span>
<span data-ttu-id="6524d-103">已容錯移轉 Azure SQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="6524d-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6524d-104">句法</span><span class="sxs-lookup"><span data-stu-id="6524d-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6524d-105">說明</span><span class="sxs-lookup"><span data-stu-id="6524d-105">DESCRIPTION</span></span>
<span data-ttu-id="6524d-106">**AzSqlInstanceFailover** Cmdlet 會針對 Azure SQL Managed 實例進行容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="6524d-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="6524d-107">示例</span><span class="sxs-lookup"><span data-stu-id="6524d-107">EXAMPLES</span></span>

### <span data-ttu-id="6524d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6524d-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="6524d-109">這個命令會將名為 "ManagedInstance01" 的實例的主要複本容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="6524d-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="6524d-110">範例2</span><span class="sxs-lookup"><span data-stu-id="6524d-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="6524d-111">這個命令會自動容錯移轉受管理實例 "ManagedInstance01" 的可讀取次要複本。</span><span class="sxs-lookup"><span data-stu-id="6524d-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="6524d-112">參數</span><span class="sxs-lookup"><span data-stu-id="6524d-112">PARAMETERS</span></span>

### <span data-ttu-id="6524d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6524d-113">-AsJob</span></span>
<span data-ttu-id="6524d-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6524d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6524d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6524d-115">-DefaultProfile</span></span>
<span data-ttu-id="6524d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6524d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6524d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6524d-117">-Force</span></span>
<span data-ttu-id="6524d-118">略過確認訊息以執行動作</span><span class="sxs-lookup"><span data-stu-id="6524d-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6524d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="6524d-119">-Name</span></span>
<span data-ttu-id="6524d-120">要移除之 Azure SQL 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="6524d-120">The name of the Azure SQL instance to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6524d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6524d-121">-PassThru</span></span>
<span data-ttu-id="6524d-122">成功執行時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="6524d-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="6524d-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6524d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6524d-124">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="6524d-124">-ReadableSecondary</span></span>
<span data-ttu-id="6524d-125">容錯移轉可讀取的次要複本，而不是預設的主要複本</span><span class="sxs-lookup"><span data-stu-id="6524d-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="6524d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6524d-126">-ResourceGroupName</span></span>
<span data-ttu-id="6524d-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6524d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="6524d-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6524d-128">-Confirm</span></span>
<span data-ttu-id="6524d-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6524d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6524d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6524d-130">-WhatIf</span></span>
<span data-ttu-id="6524d-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6524d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6524d-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6524d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6524d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6524d-133">CommonParameters</span></span>
<span data-ttu-id="6524d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6524d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6524d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6524d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6524d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6524d-136">INPUTS</span></span>

### <span data-ttu-id="6524d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="6524d-137">System.String</span></span>

## <span data-ttu-id="6524d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6524d-138">OUTPUTS</span></span>

## <span data-ttu-id="6524d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6524d-139">NOTES</span></span>

## <span data-ttu-id="6524d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="6524d-140">RELATED LINKS</span></span>
