---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 5f5c8c193a352738f64d595188247bf0564bea43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971065"
---
# <span data-ttu-id="4977c-101">Set-AzHDInsightGatewayCredential</span><span class="sxs-lookup"><span data-stu-id="4977c-101">Set-AzHDInsightGatewayCredential</span></span>

## <span data-ttu-id="4977c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4977c-102">SYNOPSIS</span></span>
<span data-ttu-id="4977c-103">設定 Azure HDInsight 群集的閘道 HTTP 認證。</span><span class="sxs-lookup"><span data-stu-id="4977c-103">Sets the gateway HTTP credentials of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4977c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4977c-104">SYNTAX</span></span>

### <span data-ttu-id="4977c-105">SetByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4977c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4977c-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4977c-106">SetByInputObjectParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4977c-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4977c-107">SetByResourceIdParameterSet</span></span>
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4977c-108">說明</span><span class="sxs-lookup"><span data-stu-id="4977c-108">DESCRIPTION</span></span>
<span data-ttu-id="4977c-109">**AzHDInsightGatewayCredential** Cmdlet 會設定 Azure HDInsight 群集的閘道認證。</span><span class="sxs-lookup"><span data-stu-id="4977c-109">The **Set-AzHDInsightGatewayCredential** cmdlet sets gateway credential of an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="4977c-110">示例</span><span class="sxs-lookup"><span data-stu-id="4977c-110">EXAMPLES</span></span>

### <span data-ttu-id="4977c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4977c-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4977c-112">這個命令會根據名稱參數集，設定名為 [hadoop-001] 的群集閘道認證。</span><span class="sxs-lookup"><span data-stu-id="4977c-112">This command sets gateway credential of the cluster named your-hadoop-001 by name parameter set.</span></span>

### <span data-ttu-id="4977c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4977c-113">Example 2</span></span>
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4977c-114">這個命令會將名為 [您的-hadoop-001] 的群集閘道認證設定為 [ResourceId] 參數集。</span><span class="sxs-lookup"><span data-stu-id="4977c-114">This command sets gateway credential of the cluster named your-hadoop-001 by ResourceId parameter set.</span></span>

### <span data-ttu-id="4977c-115">範例3</span><span class="sxs-lookup"><span data-stu-id="4977c-115">Example 3</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

<span data-ttu-id="4977c-116">這個命令會根據 InputObject 參數集，設定名為 "hadoop-001" 的群集閘道認證。</span><span class="sxs-lookup"><span data-stu-id="4977c-116">This command sets gateway credential of the cluster named your-hadoop-001 by InputObject parameter set.</span></span>

## <span data-ttu-id="4977c-117">參數</span><span class="sxs-lookup"><span data-stu-id="4977c-117">PARAMETERS</span></span>

### <span data-ttu-id="4977c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4977c-118">-AsJob</span></span>
<span data-ttu-id="4977c-119">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4977c-119">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="4977c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4977c-120">-DefaultProfile</span></span>
<span data-ttu-id="4977c-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4977c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4977c-122">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4977c-122">-HttpCredential</span></span>
<span data-ttu-id="4977c-123">取得或設定群集使用者的登入。</span><span class="sxs-lookup"><span data-stu-id="4977c-123">Gets or sets the login for the cluster's user.</span></span>

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

### <span data-ttu-id="4977c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4977c-124">-InputObject</span></span>
<span data-ttu-id="4977c-125">取得或設定輸入物件。</span><span class="sxs-lookup"><span data-stu-id="4977c-125">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="4977c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="4977c-126">-Name</span></span>
<span data-ttu-id="4977c-127">取得或設定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="4977c-127">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4977c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4977c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4977c-129">取得或設定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4977c-129">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="4977c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4977c-130">-ResourceId</span></span>
<span data-ttu-id="4977c-131">取得或設定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4977c-131">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="4977c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4977c-132">-Confirm</span></span>
<span data-ttu-id="4977c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4977c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4977c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4977c-134">-WhatIf</span></span>
<span data-ttu-id="4977c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4977c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4977c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4977c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4977c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4977c-137">CommonParameters</span></span>
<span data-ttu-id="4977c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4977c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4977c-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4977c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4977c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4977c-140">INPUTS</span></span>

### <span data-ttu-id="4977c-141">所有</span><span class="sxs-lookup"><span data-stu-id="4977c-141">None</span></span>

## <span data-ttu-id="4977c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4977c-142">OUTPUTS</span></span>

### <span data-ttu-id="4977c-143">AzureHDInsightGatewaySettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4977c-143">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightGatewaySettings</span></span>

## <span data-ttu-id="4977c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4977c-144">NOTES</span></span>

## <span data-ttu-id="4977c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4977c-145">RELATED LINKS</span></span>
