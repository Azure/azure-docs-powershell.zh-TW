---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: ef0ad91d0294f0ac1a4a466a79ce436a7719af5a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435001"
---
# <span data-ttu-id="e8cb8-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="e8cb8-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="e8cb8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8cb8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8cb8-103">移除 Azure SQL 虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="e8cb8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8cb8-104">SYNTAX</span></span>

### <span data-ttu-id="e8cb8-105">RemoveVirtualClusterFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="e8cb8-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8cb8-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="e8cb8-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8cb8-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="e8cb8-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8cb8-108">說明</span><span class="sxs-lookup"><span data-stu-id="e8cb8-108">DESCRIPTION</span></span>
<span data-ttu-id="e8cb8-109">**AzSqlVirtualCluster** Cmdlet 會移除 Azure SQL 虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="e8cb8-110">示例</span><span class="sxs-lookup"><span data-stu-id="e8cb8-110">EXAMPLES</span></span>

### <span data-ttu-id="e8cb8-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e8cb8-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="e8cb8-112">這個命令會從指派給資源群組 ResourceGroup01 的名為 VirtualCluster1 的虛擬叢集中移除。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="e8cb8-113">參數</span><span class="sxs-lookup"><span data-stu-id="e8cb8-113">PARAMETERS</span></span>

### <span data-ttu-id="e8cb8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8cb8-114">-AsJob</span></span>
<span data-ttu-id="e8cb8-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e8cb8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8cb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8cb8-116">-DefaultProfile</span></span>
<span data-ttu-id="e8cb8-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8cb8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8cb8-118">-InputObject</span></span>
<span data-ttu-id="e8cb8-119">要移除的實例物件</span><span class="sxs-lookup"><span data-stu-id="e8cb8-119">The instance object to remove</span></span>

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

### <span data-ttu-id="e8cb8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8cb8-120">-Name</span></span>
<span data-ttu-id="e8cb8-121">虛擬叢集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="e8cb8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8cb8-122">-ResourceGroupName</span></span>
<span data-ttu-id="e8cb8-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8cb8-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8cb8-124">-ResourceId</span></span>
<span data-ttu-id="e8cb8-125">要移除之實例物件的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e8cb8-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="e8cb8-126">-確認</span><span class="sxs-lookup"><span data-stu-id="e8cb8-126">-Confirm</span></span>
<span data-ttu-id="e8cb8-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8cb8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8cb8-128">-WhatIf</span></span>
<span data-ttu-id="e8cb8-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8cb8-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8cb8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8cb8-131">CommonParameters</span></span>
<span data-ttu-id="e8cb8-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8cb8-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e8cb8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8cb8-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e8cb8-134">INPUTS</span></span>

### <span data-ttu-id="e8cb8-135">AzureSqlVirtualClusterModel 中的 [VirtualCluster]</span><span class="sxs-lookup"><span data-stu-id="e8cb8-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="e8cb8-136">System.object</span><span class="sxs-lookup"><span data-stu-id="e8cb8-136">System.String</span></span>

## <span data-ttu-id="e8cb8-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e8cb8-137">OUTPUTS</span></span>

### <span data-ttu-id="e8cb8-138">AzureSqlVirtualClusterModel 中的 [VirtualCluster]</span><span class="sxs-lookup"><span data-stu-id="e8cb8-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="e8cb8-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e8cb8-139">NOTES</span></span>

## <span data-ttu-id="e8cb8-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8cb8-140">RELATED LINKS</span></span>
