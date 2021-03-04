---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlVirtualCluster.md
ms.openlocfilehash: f18cb699df3bd96a6b5705e09f6cb9ea924f3f62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913069"
---
# <span data-ttu-id="f1a12-101">Remove-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f1a12-101">Remove-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f1a12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f1a12-102">SYNOPSIS</span></span>
<span data-ttu-id="f1a12-103">移除 Azure SQL 虛擬組組。</span><span class="sxs-lookup"><span data-stu-id="f1a12-103">Removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f1a12-104">語法</span><span class="sxs-lookup"><span data-stu-id="f1a12-104">SYNTAX</span></span>

### <span data-ttu-id="f1a12-105">RemoveVirtualClusterFromInputParameters (預設) </span><span class="sxs-lookup"><span data-stu-id="f1a12-105">RemoveVirtualClusterFromInputParameters (Default)</span></span>
```
Remove-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a12-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span><span class="sxs-lookup"><span data-stu-id="f1a12-106">RemoveVirtualClusterFromAzureSqlVirtualClusterModelDefinition</span></span>
```
Remove-AzSqlVirtualCluster [-InputObject] <AzureSqlVirtualClusterModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1a12-107">RemoveVirtualClusterFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a12-107">RemoveVirtualClusterFromAzureResourceId</span></span>
```
Remove-AzSqlVirtualCluster -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1a12-108">描述</span><span class="sxs-lookup"><span data-stu-id="f1a12-108">DESCRIPTION</span></span>
<span data-ttu-id="f1a12-109">**Remove-AzSqlVirtualCludlet Cmdlet** 會移除 Azure SQL 虛擬叢集。</span><span class="sxs-lookup"><span data-stu-id="f1a12-109">The **Remove-AzSqlVirtualCluster** cmdlet removes an Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f1a12-110">例子</span><span class="sxs-lookup"><span data-stu-id="f1a12-110">EXAMPLES</span></span>

### <span data-ttu-id="f1a12-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f1a12-111">Example 1</span></span>
```powershell
PS C:> Remove-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01
```

<span data-ttu-id="f1a12-112">此命令會移除指派給資源群組 ResourceGroup01 的虛擬叢集 VirtualCluster1。</span><span class="sxs-lookup"><span data-stu-id="f1a12-112">This command removes the virtual cluster named VirtualCluster1 assigned to the resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f1a12-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1a12-113">PARAMETERS</span></span>

### <span data-ttu-id="f1a12-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1a12-114">-AsJob</span></span>
<span data-ttu-id="f1a12-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f1a12-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f1a12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1a12-116">-DefaultProfile</span></span>
<span data-ttu-id="f1a12-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1a12-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1a12-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1a12-118">-InputObject</span></span>
<span data-ttu-id="f1a12-119">要移除的實例物件</span><span class="sxs-lookup"><span data-stu-id="f1a12-119">The instance object to remove</span></span>

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

### <span data-ttu-id="f1a12-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f1a12-120">-Name</span></span>
<span data-ttu-id="f1a12-121">虛擬組名。</span><span class="sxs-lookup"><span data-stu-id="f1a12-121">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="f1a12-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1a12-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1a12-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1a12-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="f1a12-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1a12-124">-ResourceId</span></span>
<span data-ttu-id="f1a12-125">要移除的實例物件資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f1a12-125">The resource id of instance object to remove</span></span>

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

### <span data-ttu-id="f1a12-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f1a12-126">-Confirm</span></span>
<span data-ttu-id="f1a12-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f1a12-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1a12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1a12-128">-WhatIf</span></span>
<span data-ttu-id="f1a12-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1a12-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1a12-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1a12-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1a12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1a12-131">CommonParameters</span></span>
<span data-ttu-id="f1a12-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f1a12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1a12-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1a12-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1a12-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f1a12-134">INPUTS</span></span>

### <span data-ttu-id="f1a12-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f1a12-135">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

### <span data-ttu-id="f1a12-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f1a12-136">System.String</span></span>

## <span data-ttu-id="f1a12-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f1a12-137">OUTPUTS</span></span>

### <span data-ttu-id="f1a12-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f1a12-138">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f1a12-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f1a12-139">NOTES</span></span>

## <span data-ttu-id="f1a12-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1a12-140">RELATED LINKS</span></span>
