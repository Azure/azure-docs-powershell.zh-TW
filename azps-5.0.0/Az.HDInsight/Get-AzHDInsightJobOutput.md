---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 2489da10ebf1d346b147e252d6d347635efb1aff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136813"
---
# <span data-ttu-id="75a70-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="75a70-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="75a70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="75a70-102">SYNOPSIS</span></span>
<span data-ttu-id="75a70-103">從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="75a70-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="75a70-104">句法</span><span class="sxs-lookup"><span data-stu-id="75a70-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a70-105">說明</span><span class="sxs-lookup"><span data-stu-id="75a70-105">DESCRIPTION</span></span>
<span data-ttu-id="75a70-106">**AzHDInsightJobOutput** Cmdlet 會從與 Azure HDInsight 群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="75a70-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="75a70-107">示例</span><span class="sxs-lookup"><span data-stu-id="75a70-107">EXAMPLES</span></span>

### <span data-ttu-id="75a70-108">範例1：取得作業的記錄輸出</span><span class="sxs-lookup"><span data-stu-id="75a70-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="75a70-109">這個命令會從名為 [您的 hadoop-001] 的群集中取得記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="75a70-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="75a70-110">參數</span><span class="sxs-lookup"><span data-stu-id="75a70-110">PARAMETERS</span></span>

### <span data-ttu-id="75a70-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="75a70-111">-ClusterName</span></span>
<span data-ttu-id="75a70-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a70-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="75a70-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="75a70-113">-DefaultContainer</span></span>
<span data-ttu-id="75a70-114">指定預設容器名稱。</span><span class="sxs-lookup"><span data-stu-id="75a70-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="75a70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a70-115">-DefaultProfile</span></span>
<span data-ttu-id="75a70-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="75a70-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75a70-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="75a70-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="75a70-118">指定預設儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="75a70-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="75a70-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="75a70-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="75a70-120">指定預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="75a70-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="75a70-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="75a70-121">-DisplayOutputType</span></span>
<span data-ttu-id="75a70-122">指定要要求的作業輸出類型。</span><span class="sxs-lookup"><span data-stu-id="75a70-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="75a70-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="75a70-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="75a70-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="75a70-124">StandardOutput</span></span>
- <span data-ttu-id="75a70-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="75a70-125">StandardError</span></span>

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

### <span data-ttu-id="75a70-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="75a70-126">-HttpCredential</span></span>
<span data-ttu-id="75a70-127">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="75a70-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="75a70-128">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="75a70-128">-JobId</span></span>
<span data-ttu-id="75a70-129">指定將回遷輸出的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="75a70-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="75a70-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a70-130">-ResourceGroupName</span></span>
<span data-ttu-id="75a70-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="75a70-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="75a70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a70-132">CommonParameters</span></span>
<span data-ttu-id="75a70-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="75a70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a70-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="75a70-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a70-135">輸入</span><span class="sxs-lookup"><span data-stu-id="75a70-135">INPUTS</span></span>

### <span data-ttu-id="75a70-136">所有</span><span class="sxs-lookup"><span data-stu-id="75a70-136">None</span></span>

## <span data-ttu-id="75a70-137">輸出</span><span class="sxs-lookup"><span data-stu-id="75a70-137">OUTPUTS</span></span>

### <span data-ttu-id="75a70-138">System.object</span><span class="sxs-lookup"><span data-stu-id="75a70-138">System.String</span></span>

## <span data-ttu-id="75a70-139">筆記</span><span class="sxs-lookup"><span data-stu-id="75a70-139">NOTES</span></span>

## <span data-ttu-id="75a70-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="75a70-140">RELATED LINKS</span></span>

[<span data-ttu-id="75a70-141">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="75a70-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="75a70-142">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="75a70-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)

