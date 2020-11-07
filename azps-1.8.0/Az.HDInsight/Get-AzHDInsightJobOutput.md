---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5871C962-27D7-4EC8-927E-D4CAE5F23C58
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightJobOutput.md
ms.openlocfilehash: 3d4ffa7a3172921b8aba7d73fc2c468c0e3117f3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787706"
---
# <span data-ttu-id="df62b-101">Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="df62b-101">Get-AzHDInsightJobOutput</span></span>

## <span data-ttu-id="df62b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df62b-102">SYNOPSIS</span></span>
<span data-ttu-id="df62b-103">從與指定群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="df62b-103">Gets the log output for a job from the storage account associated with a specified cluster.</span></span>

## <span data-ttu-id="df62b-104">句法</span><span class="sxs-lookup"><span data-stu-id="df62b-104">SYNTAX</span></span>

```
Get-AzHDInsightJobOutput [-ClusterName] <String> [-JobId] <String> [[-DefaultContainer] <String>]
 [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-DisplayOutputType <JobDisplayOutputType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df62b-105">說明</span><span class="sxs-lookup"><span data-stu-id="df62b-105">DESCRIPTION</span></span>
<span data-ttu-id="df62b-106">**AzHDInsightJobOutput** Cmdlet 會從與 Azure HDInsight 群集相關聯的儲存空間帳戶取得作業的記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="df62b-106">The **Get-AzHDInsightJobOutput** cmdlet gets the log output for a job from the Storage account associated with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="df62b-107">示例</span><span class="sxs-lookup"><span data-stu-id="df62b-107">EXAMPLES</span></span>

### <span data-ttu-id="df62b-108">範例1：取得作業的記錄輸出</span><span class="sxs-lookup"><span data-stu-id="df62b-108">Example 1: Get the log output for a job</span></span>
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

<span data-ttu-id="df62b-109">這個命令會從名為 [您的 hadoop-001] 的群集中取得記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="df62b-109">This command gets the log output from the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="df62b-110">參數</span><span class="sxs-lookup"><span data-stu-id="df62b-110">PARAMETERS</span></span>

### <span data-ttu-id="df62b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="df62b-111">-ClusterName</span></span>
<span data-ttu-id="df62b-112">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="df62b-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="df62b-113">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="df62b-113">-DefaultContainer</span></span>
<span data-ttu-id="df62b-114">指定預設容器名稱。</span><span class="sxs-lookup"><span data-stu-id="df62b-114">Specifies the default container name.</span></span>

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

### <span data-ttu-id="df62b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df62b-115">-DefaultProfile</span></span>
<span data-ttu-id="df62b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="df62b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df62b-117">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="df62b-117">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="df62b-118">指定預設儲存空間帳戶金鑰。</span><span class="sxs-lookup"><span data-stu-id="df62b-118">Specifies the default Storage account key.</span></span>

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

### <span data-ttu-id="df62b-119">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="df62b-119">-DefaultStorageAccountName</span></span>
<span data-ttu-id="df62b-120">指定預設儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="df62b-120">Specifies the default Storage account name.</span></span>

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

### <span data-ttu-id="df62b-121">-DisplayOutputType</span><span class="sxs-lookup"><span data-stu-id="df62b-121">-DisplayOutputType</span></span>
<span data-ttu-id="df62b-122">指定要要求的作業輸出類型。</span><span class="sxs-lookup"><span data-stu-id="df62b-122">Specifies the job output type being requested.</span></span>
<span data-ttu-id="df62b-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="df62b-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df62b-124">StandardOutput</span><span class="sxs-lookup"><span data-stu-id="df62b-124">StandardOutput</span></span>
- <span data-ttu-id="df62b-125">StandardError</span><span class="sxs-lookup"><span data-stu-id="df62b-125">StandardError</span></span>

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

### <span data-ttu-id="df62b-126">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="df62b-126">-HttpCredential</span></span>
<span data-ttu-id="df62b-127">指定群集的群集登入 (HTTP) 認證。</span><span class="sxs-lookup"><span data-stu-id="df62b-127">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="df62b-128">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="df62b-128">-JobId</span></span>
<span data-ttu-id="df62b-129">指定將回遷輸出的作業 ID。</span><span class="sxs-lookup"><span data-stu-id="df62b-129">Specifies the job ID of the job whose output will be fetched.</span></span>

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

### <span data-ttu-id="df62b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df62b-130">-ResourceGroupName</span></span>
<span data-ttu-id="df62b-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="df62b-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="df62b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df62b-132">CommonParameters</span></span>
<span data-ttu-id="df62b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df62b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df62b-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="df62b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df62b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="df62b-135">INPUTS</span></span>

### <span data-ttu-id="df62b-136">所有</span><span class="sxs-lookup"><span data-stu-id="df62b-136">None</span></span>

## <span data-ttu-id="df62b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="df62b-137">OUTPUTS</span></span>

### <span data-ttu-id="df62b-138">System.object</span><span class="sxs-lookup"><span data-stu-id="df62b-138">System.String</span></span>

## <span data-ttu-id="df62b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="df62b-139">NOTES</span></span>

## <span data-ttu-id="df62b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="df62b-140">RELATED LINKS</span></span>

[<span data-ttu-id="df62b-141">新-AzHDInsightHiveJobDefinition</span><span class="sxs-lookup"><span data-stu-id="df62b-141">New-AzHDInsightHiveJobDefinition</span></span>](./New-AzHDInsightHiveJobDefinition.md)

[<span data-ttu-id="df62b-142">開始-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="df62b-142">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


