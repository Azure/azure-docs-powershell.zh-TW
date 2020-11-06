---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: d4c69457b9932f76d002e3941af3015225345c8f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614759"
---
# <span data-ttu-id="97a79-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="97a79-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="97a79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97a79-102">SYNOPSIS</span></span>
<span data-ttu-id="97a79-103">移除 Azure SQL 虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="97a79-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="97a79-104">句法</span><span class="sxs-lookup"><span data-stu-id="97a79-104">SYNTAX</span></span>

### <span data-ttu-id="97a79-105">RemoveVirtualClusterFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="97a79-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a79-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="97a79-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a79-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="97a79-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a79-108">說明</span><span class="sxs-lookup"><span data-stu-id="97a79-108">DESCRIPTION</span></span>
<span data-ttu-id="97a79-109">**AzSqlVirtualCluster** Cmdlet 會移除 Azure SQL 虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="97a79-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="97a79-110">示例</span><span class="sxs-lookup"><span data-stu-id="97a79-110">EXAMPLES</span></span>

### <span data-ttu-id="97a79-111">範例1</span><span class="sxs-lookup"><span data-stu-id="97a79-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="97a79-112">這個命令會從指派給資源群組 ResourceGroup01 的名為 VirtualCluster1 的虛擬叢集中移除。</span><span class="sxs-lookup"><span data-stu-id="97a79-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="97a79-113">參數</span><span class="sxs-lookup"><span data-stu-id="97a79-113">PARAMETERS</span></span>

### <span data-ttu-id="97a79-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97a79-114">-AsJob</span></span>
<span data-ttu-id="97a79-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="97a79-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="97a79-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a79-116">-DefaultProfile</span></span>
<span data-ttu-id="97a79-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97a79-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97a79-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97a79-118">-InputObject</span></span>
<span data-ttu-id="97a79-119">要移除的實例物件</span><span class="sxs-lookup"><span data-stu-id="97a79-119">The instance object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel
Parameter Sets: RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition
Aliases: VirtualCluster

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a79-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="97a79-120">-Name</span></span>
<span data-ttu-id="97a79-121">虛擬叢集的名稱。</span><span class="sxs-lookup"><span data-stu-id="97a79-121">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a79-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a79-122">-ResourceGroupName</span></span>
<span data-ttu-id="97a79-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97a79-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a79-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="97a79-124">-ResourceId</span></span>
<span data-ttu-id="97a79-125">要移除之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="97a79-125">The resource id of instance object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveVirtualClusterFromAzureResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a79-126">-確認</span><span class="sxs-lookup"><span data-stu-id="97a79-126">-Confirm</span></span>
<span data-ttu-id="97a79-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97a79-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97a79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a79-128">-WhatIf</span></span>
<span data-ttu-id="97a79-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97a79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a79-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97a79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97a79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a79-131">CommonParameters</span></span>
<span data-ttu-id="97a79-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97a79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a79-133">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="97a79-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a79-134">輸入</span><span class="sxs-lookup"><span data-stu-id="97a79-134">INPUTS</span></span>

### <span data-ttu-id="97a79-135">AzureSqlVirtualClusterModel 中的 [VirtualCluster]</span><span class="sxs-lookup"><span data-stu-id="97a79-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="97a79-136">System.object</span><span class="sxs-lookup"><span data-stu-id="97a79-136">System.String</span></span>

## <span data-ttu-id="97a79-137">輸出</span><span class="sxs-lookup"><span data-stu-id="97a79-137">OUTPUTS</span></span>

### <span data-ttu-id="97a79-138">AzureSqlVirtualClusterModel 中的 [VirtualCluster]</span><span class="sxs-lookup"><span data-stu-id="97a79-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="97a79-139">筆記</span><span class="sxs-lookup"><span data-stu-id="97a79-139">NOTES</span></span>

## <span data-ttu-id="97a79-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="97a79-140">RELATED LINKS</span></span>
