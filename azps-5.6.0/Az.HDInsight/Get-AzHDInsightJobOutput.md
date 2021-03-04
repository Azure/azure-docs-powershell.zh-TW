---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: d36f49110cb3c3f4d51c9223e2a7ab150eb779ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912393"
---
# <span data-ttu-id="0e629-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="0e629-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="0e629-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0e629-102">SYNOPSIS</span></span>
<span data-ttu-id="0e629-103">從與指定組群相關聯的儲存空間帳戶，獲得工作的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="0e629-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="0e629-104">語法</span><span class="sxs-lookup"><span data-stu-id="0e629-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e629-105">描述</span><span class="sxs-lookup"><span data-stu-id="0e629-105">DESCRIPTION</span></span>
<span data-ttu-id="0e629-106">**Get-AzHDInsightJobOutput** Cmdlet 會從與 Azure HDInsight 集區關聯的儲存空間帳戶取得工作的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="0e629-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="0e629-107">例子</span><span class="sxs-lookup"><span data-stu-id="0e629-107">EXAMPLES</span></span>

### <span data-ttu-id="0e629-108">範例 1：取得工作的記錄輸出</span><span class="sxs-lookup"><span data-stu-id="0e629-108">Example 1: Get the log output for a job</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "<status folder>"
PS C:\> $query = "<query here>"

PS C:\> New-AzHDInsightHiveJobDefinition -StatusFolder $statusFolder `
            -Query $query `
        | Start-AzHDInsightJob `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds `
        | Get-AzHDInsightJobOutput `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="0e629-109">此命令會從名為 your-hadoop-001 的組集中獲得記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="0e629-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="0e629-110">參數</span><span class="sxs-lookup"><span data-stu-id="0e629-110">PARAMETERS</span></span>

### <span data-ttu-id="0e629-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0e629-111">-ClusterName</span></span>
<span data-ttu-id="0e629-112">指定組名。</span><span class="sxs-lookup"><span data-stu-id="0e629-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="0e629-113">-DefaultContainer</span></span>
<span data-ttu-id="0e629-114">指定預設的容器名稱。</span><span class="sxs-lookup"><span data-stu-id="0e629-114">Specifies the default container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e629-115">-DefaultProfile</span></span>
<span data-ttu-id="0e629-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0e629-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e629-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0e629-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="0e629-118">指定預設的儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="0e629-118">Specifies the default Storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e629-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="0e629-120">指定預設的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0e629-120">Specifies the default Storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="0e629-121">-DisplayOutputType</span></span>
<span data-ttu-id="0e629-122">指定要求的工作輸出類型。</span><span class="sxs-lookup"><span data-stu-id="0e629-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="0e629-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0e629-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0e629-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="0e629-124">StandardOutput</span></span>
- <span data-ttu-id="0e629-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="0e629-125">StandardError</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Job.JobDisplayOutputType
Parameter Sets: (All)
Aliases:
Accepted values: StandardOutput, StandardError

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-126">-HTTPCredential</span><span class="sxs-lookup"><span data-stu-id="0e629-126">-HttpCredential</span></span>
<span data-ttu-id="0e629-127">指定該組 (HTTP) 組認證。</span><span class="sxs-lookup"><span data-stu-id="0e629-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-128">-JobId</span><span class="sxs-lookup"><span data-stu-id="0e629-128">-JobId</span></span>
<span data-ttu-id="0e629-129">指定要抓取輸出之工作的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e629-129">Specifies the job ID of the job whose output will be fetched.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e629-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e629-130">-ResourceGroupName</span></span>
<span data-ttu-id="0e629-131">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e629-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0e629-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e629-132">CommonParameters</span></span>
<span data-ttu-id="0e629-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0e629-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e629-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e629-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e629-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0e629-135">INPUTS</span></span>

### <span data-ttu-id="0e629-136">沒有</span><span class="sxs-lookup"><span data-stu-id="0e629-136">None</span></span>

## <span data-ttu-id="0e629-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0e629-137">OUTPUTS</span></span>

### <span data-ttu-id="0e629-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0e629-138">System.String</span></span>

## <span data-ttu-id="0e629-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0e629-139">NOTES</span></span>

## <span data-ttu-id="0e629-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0e629-140">RELATED LINKS</span></span>

[<span data-ttu-id="0e629-141">New-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="0e629-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="0e629-142">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="0e629-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


