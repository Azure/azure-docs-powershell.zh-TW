---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: e864e963e91df9599642c763a151325dd68d65a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910493"
---
# <span data-ttu-id="68ebb-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="68ebb-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="68ebb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="68ebb-102">SYNOPSIS</span></span>
<span data-ttu-id="68ebb-103">設定 Azure HDInsight 套件的閘道 HTTP 認證。</span><span class="sxs-lookup"><span data-stu-id="68ebb-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="68ebb-104">語法</span><span class="sxs-lookup"><span data-stu-id="68ebb-104">SYNTAX</span></span>

### <span data-ttu-id="68ebb-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="68ebb-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential [-Name] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68ebb-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ebb-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68ebb-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68ebb-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68ebb-108">描述</span><span class="sxs-lookup"><span data-stu-id="68ebb-108">DESCRIPTION</span></span>
<span data-ttu-id="68ebb-109">**Set-AzHDInsightGatewayCredential Cmdlet** 會設定 Azure HDInsight 套件的閘道認證。</span><span class="sxs-lookup"><span data-stu-id="68ebb-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="68ebb-110">例子</span><span class="sxs-lookup"><span data-stu-id="68ebb-110">EXAMPLES</span></span>

### <span data-ttu-id="68ebb-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="68ebb-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="68ebb-112">此命令會根據名稱參數集，設定名為 your-hadoop-001 的組組閘道認證。</span><span class="sxs-lookup"><span data-stu-id="68ebb-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="68ebb-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="68ebb-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="68ebb-114">此命令會根據 ResourceId 參數集設定名為 your-hadoop-001 的該組組閘道認證。</span><span class="sxs-lookup"><span data-stu-id="68ebb-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="68ebb-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="68ebb-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="68ebb-116">此命令會根據 InputObject 參數集，設定名為 your-hadoop-001 的組組閘道認證。</span><span class="sxs-lookup"><span data-stu-id="68ebb-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="68ebb-117">參數</span><span class="sxs-lookup"><span data-stu-id="68ebb-117">PARAMETERS</span></span>

### <span data-ttu-id="68ebb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68ebb-118">-AsJob</span></span>
<span data-ttu-id="68ebb-119">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68ebb-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="68ebb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ebb-120">-DefaultProfile</span></span>
<span data-ttu-id="68ebb-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="68ebb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ebb-122">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="68ebb-122">-HttpCredential</span></span>
<span data-ttu-id="68ebb-123">為組群使用者獲取或設定登入。</span><span class="sxs-lookup"><span data-stu-id="68ebb-123">Gets or sets the login for the cluster's user.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ebb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ebb-124">-InputObject</span></span>
<span data-ttu-id="68ebb-125">獲取或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="68ebb-125">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68ebb-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="68ebb-126">-Name</span></span>
<span data-ttu-id="68ebb-127">獲取或設定組名。</span><span class="sxs-lookup"><span data-stu-id="68ebb-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ebb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ebb-128">-ResourceGroupName</span></span>
<span data-ttu-id="68ebb-129">獲取或設定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ebb-129">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ebb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68ebb-130">-ResourceId</span></span>
<span data-ttu-id="68ebb-131">獲取或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="68ebb-131">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ebb-132">-確認</span><span class="sxs-lookup"><span data-stu-id="68ebb-132">-Confirm</span></span>
<span data-ttu-id="68ebb-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="68ebb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ebb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ebb-134">-WhatIf</span></span>
<span data-ttu-id="68ebb-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68ebb-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68ebb-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68ebb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ebb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ebb-137">CommonParameters</span></span>
<span data-ttu-id="68ebb-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="68ebb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ebb-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68ebb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ebb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="68ebb-140">INPUTS</span></span>

### <span data-ttu-id="68ebb-141">沒有</span><span class="sxs-lookup"><span data-stu-id="68ebb-141">None</span></span>

## <span data-ttu-id="68ebb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="68ebb-142">OUTPUTS</span></span>

### <span data-ttu-id="68ebb-143">Microsoft.Azure.Commands.HDInsight.models.management.AzureHDInsightGatewaySettings</span><span class="sxs-lookup"><span data-stu-id="68ebb-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="68ebb-144">筆記</span><span class="sxs-lookup"><span data-stu-id="68ebb-144">NOTES</span></span>

## <span data-ttu-id="68ebb-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="68ebb-145">RELATED LINKS</span></span>
