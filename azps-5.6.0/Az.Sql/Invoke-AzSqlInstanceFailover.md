---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-AzSqlInstanceFailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlInstanceFailover.md
ms.openlocfilehash: cde8f48ebef73e3669a82f05c2ba91a4a4e4c582
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907294"
---
# <span data-ttu-id="c0ea6-101">Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="c0ea6-101">Invoke-AzSqlInstanceFailover</span></span>

## <span data-ttu-id="c0ea6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c0ea6-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ea6-103">容錯移轉 Azure SQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-103">Failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="c0ea6-104">語法</span><span class="sxs-lookup"><span data-stu-id="c0ea6-104">SYNTAX</span></span>

```
Invoke-AzSqlInstanceFailover [-Name] <String> [-AsJob] [-PassThru] [-Force] [-ReadableSecondary]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ea6-105">描述</span><span class="sxs-lookup"><span data-stu-id="c0ea6-105">DESCRIPTION</span></span>
<span data-ttu-id="c0ea6-106">**Invoke-AzSqlInstanceFailover** Cmdlet 容錯移轉 Azure SQL Managed 實例。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-106">The **Invoke-AzSqlInstanceFailover** cmdlet failovers an Azure SQL Managed Instance.</span></span>

## <span data-ttu-id="c0ea6-107">例子</span><span class="sxs-lookup"><span data-stu-id="c0ea6-107">EXAMPLES</span></span>

### <span data-ttu-id="c0ea6-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c0ea6-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01"
```

<span data-ttu-id="c0ea6-109">此命令將會容錯移轉名為「ManagedInstance01」實例的主要複本。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-109">This command will failover the primary replica of the instance named "ManagedInstance01".</span></span>

### <span data-ttu-id="c0ea6-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="c0ea6-110">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlInstanceFailover -ResourceGroupName "ResourceGroup01" -Name "ManagedInstance01" -ReadableSecondary
```

<span data-ttu-id="c0ea6-111">此命令將會容錯移轉受管理實例「ManagedInstance01」的可讀取次要複本。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-111">This command will failover the readable secondary replica of the managed instance "ManagedInstance01".</span></span>

## <span data-ttu-id="c0ea6-112">參數</span><span class="sxs-lookup"><span data-stu-id="c0ea6-112">PARAMETERS</span></span>

### <span data-ttu-id="c0ea6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0ea6-113">-AsJob</span></span>
<span data-ttu-id="c0ea6-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c0ea6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0ea6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ea6-115">-DefaultProfile</span></span>
<span data-ttu-id="c0ea6-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ea6-117">-強制</span><span class="sxs-lookup"><span data-stu-id="c0ea6-117">-Force</span></span>
<span data-ttu-id="c0ea6-118">跳過執行動作的確認訊息</span><span class="sxs-lookup"><span data-stu-id="c0ea6-118">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c0ea6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c0ea6-119">-Name</span></span>
<span data-ttu-id="c0ea6-120">要移除的 Azure SQL 實例名稱。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-120">The name of the Azure SQL instance to remove.</span></span>

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

### <span data-ttu-id="c0ea6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0ea6-121">-PassThru</span></span>
<span data-ttu-id="c0ea6-122">成功執行時，會返回 True。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="c0ea6-123">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0ea6-124">-可讀取的秒</span><span class="sxs-lookup"><span data-stu-id="c0ea6-124">-ReadableSecondary</span></span>
<span data-ttu-id="c0ea6-125">容錯移轉可讀取的次要複本，而非預設的主複本</span><span class="sxs-lookup"><span data-stu-id="c0ea6-125">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="c0ea6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ea6-126">-ResourceGroupName</span></span>
<span data-ttu-id="c0ea6-127">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c0ea6-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c0ea6-128">-Confirm</span></span>
<span data-ttu-id="c0ea6-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ea6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ea6-130">-WhatIf</span></span>
<span data-ttu-id="c0ea6-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0ea6-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ea6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ea6-133">CommonParameters</span></span>
<span data-ttu-id="c0ea6-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c0ea6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ea6-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0ea6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ea6-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c0ea6-136">INPUTS</span></span>

### <span data-ttu-id="c0ea6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c0ea6-137">System.String</span></span>

## <span data-ttu-id="c0ea6-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c0ea6-138">OUTPUTS</span></span>

## <span data-ttu-id="c0ea6-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c0ea6-139">NOTES</span></span>

## <span data-ttu-id="c0ea6-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c0ea6-140">RELATED LINKS</span></span>
